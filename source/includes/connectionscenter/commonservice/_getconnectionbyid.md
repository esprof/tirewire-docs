## GetConnectionByID

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionByID"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> SOAP request.xml

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetConnectionByID xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <key>string</key>
      <groupToken>string</groupToken>
      <connectionID>int</connectionID>
    </GetConnectionByID>
  </soap:Body>
</soap:Envelope>
```

> SOAP response.xml

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetConnectionByIDResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <GetConnectionByIDResult>
        <Connections>
          <ConnectionInformation>
            <Name>string</Name>
            <WarehouseName>string</WarehouseName>
            <SupplierSystemID>int</SupplierSystemID>
            <TirewireConnectionID>int</TirewireConnectionID>
            <Credentials xsi:nil="true" />
            <Type>int</Type>
            <HasTires>boolean</HasTires>
            <HasWheels>boolean</HasWheels>
            <HasMiscProducts>boolean</HasMiscProducts>
          </ConnectionInformation>
        </Connections>
      </GetConnectionByIDResult>
    </GetConnectionByIDResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves a Connection by ID.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionByID`

### Input Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)
connectionID | int | [The ID of the connection](#get-connections-by-group-token)
