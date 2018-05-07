## GetDeliveryOptions

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/ordersservice/GetDeliveryOptions"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/ordersservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetDeliveryOptions xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <key>string</key>
      <groupToken>string</groupToken>
      <connectionID>int</connectionID>
      <subData>string</subData>
    </GetDeliveryOptions>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetDeliveryOptionsResponse xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <GetDeliveryOptionsResult>
        <DeliveryOptions>
          <DeliveryOption>
            <Code>string</Code>
            <Title>string</Title>
          </DeliveryOption>
          ...
        </DeliveryOptions>
      </GetDeliveryOptionsResult>
    </GetDeliveryOptionsResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves available Delivery Options for a Connection.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/ordersservice/GetDeliveryOptions`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)
connectionID | int | [The ID of the connection](#get-connections-by-group-token)
SubData | string | SubData override

### Response Parameters
An array of DeliveryOption objects.

Parameter | Type | Description
--------- | ---- | -----------
Code | string | Delivery option identifying code
Title | string | Delivery option title
