## GetShipToOptions

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/ordersservice/GetShipToOptions"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/ordersservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetShipToOptions xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <key>string</key>
      <groupToken>string</groupToken>
      <connectionID>int</connectionID>
      <subData>string</subData>
    </GetShipToOptions>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetShipToOptionsResponse xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <GetShipToOptionsResult>
        <ShipToOptions>
          <ShipToOption>
            <Code>string</Code>
            <Title>string</Title>
            <AddressLine1>string</AddressLine1>
            <AddressLine2>string</AddressLine2>
            <City>string</City>
            <State>string</State>
            <ZIP>int</ZIP>
          </ShipToOption>
          ...
        </ShipToOptions>
      </GetShipToOptionsResult>
    </GetShipToOptionsResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves available Ship-To Options for a Connection where supported.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/ordersservice/GetShipToOptions`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)
connectionID | int | [The ID of the connection](#get-connections-by-group-token)
SubData | string | SubData override

### Response Parameters
An array of ShipToOption objects.

Parameter | Type | Description
--------- | ---- | -----------
Code | string | Ship-to option identifying code
Title | string | Ship-to option title
AddressLine1 | string | Address line 1
AddressLine2 | string | Address line 2
City | string | City
State | string | State
ZIP | int | ZIP code
