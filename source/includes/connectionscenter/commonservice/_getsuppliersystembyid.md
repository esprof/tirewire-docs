## GetSupplierSystemByID

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystemByID"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetSupplierSystemByID xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <key>string</key>
      <id>int</id>
    </GetSupplierSystemByID>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetSupplierSystemByIDResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <GetSupplierSystemByIDResult>
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
        </SupplierSystems>
      </GetSupplierSystemByIDResult>
    </GetSupplierSystemByIDResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves a Supplier System by its ID.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystemByID`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
id | int | The ID of the supplier system

### Response Parameters
A SupplierSystem object.

Parameter | Type | Description
--------- | ---- | -----------
ID | int | Supplier system ID
Name | string | Supplier system name
ImageURL | string | Supplier system logo image URL
CredentialFields | string[] | *(internal)*
CanChangePassword | boolean | *(internal)*
RequiresUserInformation | boolean | *(internal)*
HasTires | boolean | Has tires
HasWheels | boolean | Has wheels
HasMiscProducts | boolean | Has miscellaneous products (accessories, etc)
