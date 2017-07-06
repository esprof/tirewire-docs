## GetSupplierSystems

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystems"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetSupplierSystems xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <key>string</key>
    </GetSupplierSystems>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetSupplierSystemsResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <GetSupplierSystemsResult>
        <SupplierSystems>
          <SupplierSystem>
            <ID>int</ID>
            <Name>string</Name>
            <ImageURL>string</ImageURL>
            <CredentialFields xsi:nil="true" />
            <CanChangePassword>boolean</CanChangePassword>
            <RequiresUserInformation>boolean</RequiresUserInformation>
            <HasTires>boolean</HasTires>
            <HasWheels>boolean</HasWheels>
            <HasMiscProducts>boolean</HasMiscProducts>
          </SupplierSystem>
          ...
        </SupplierSystems>
      </GetSupplierSystemsResult>
    </GetSupplierSystemsResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves all Supplier Systems.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystems`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
