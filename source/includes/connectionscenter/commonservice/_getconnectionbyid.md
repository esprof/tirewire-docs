## GetConnectionByID

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionByID"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> Request XML

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

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetConnectionByIDResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <GetConnectionByIDResult>
        <Connections>
          <ConnectionInformation>
            <Name>string</Name>
            <Active>boolean</Active>
            <WarehouseName>string</WarehouseName>
            <SupplierSystemID>int</SupplierSystemID>
            <TirewireConnectionID>int</TirewireConnectionID>
            <Credentials xsi:nil="true" />
            <Type>int</Type>
            <HasTires>boolean</HasTires>
            <HasWheels>boolean</HasWheels>
            <HasMiscProducts>boolean</HasMiscProducts>
            <MappingPackageID>int</MappingPackageID>
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

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)
connectionID | int | [The ID of the connection](#get-connections-by-group-token)

### Response Parameters
A ConnectionInformation object.

Parameter | Type | Description
--------- | ---- | -----------
Name | string | Connection name
Active | boolean | Has the connection been activated
WarehouseName | string | Warehouse name (where available)
SupplierSystemID | int | Supplier system ID
TirewireConnectionID | int | Connection ID
Credentials | string[] | *(internal)*
Type | int | *(internal)* Connection type
HasTires | boolean | Has tires
HasWheels | boolean | Has wheels
HasMiscProducts | boolean | Has miscellaneous products (accessories, etc)
MappingPackageID | int | Tire Library mapping package ID (-1 if not set or unsupported)
