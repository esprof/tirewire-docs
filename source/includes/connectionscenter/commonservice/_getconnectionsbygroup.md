## GetConnectionsByGroup

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionsByGroup"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetConnectionsByGroup xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <key>string</key>
      <groupToken>string</groupToken>
    </GetConnectionsByGroup>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetConnectionsByGroupResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <GetConnectionsByGroupResult>
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
          ...
        </Connections>
      </GetConnectionsByGroupResult>
    </GetConnectionsByGroupResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves all Connections in a given Group.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionsByGroup`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connections](#creating-a-group)

### Response Parameters
An array of ConnectionInformation objects.

Parameter | Type | Description
--------- | ---- | -----------
Name | string | Connection name
WarehouseName | string | Warehouse name (where available)
SupplierSystemID | int | Supplier system ID
TirewireConnectionID | int | Connection ID
Credentials | string[] | *(internal)*
Type | int | Connection type *(internal)*
HasTires | boolean | Has tires
HasWheels | boolean | Has wheels
HasMiscProducts | boolean | Has miscellaneous products (accessories, etc)
