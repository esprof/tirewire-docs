## GetAllMakes

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetAllMakes"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> SOAP request.xml

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetAllMakes xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <key>string</key>
    </GetAllMakes>
  </soap:Body>
</soap:Envelope>
```

> SOAP response.xml

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetAllMakesResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <GetAllMakesResult>
        <Makes>
          <Make>
            <ID>int</ID>
            <Name>string</Name>
            <EzytireCode>string</EzytireCode>
          </Make>
          <Make>
            <ID>int</ID>
            <Name>string</Name>
            <EzytireCode>string</EzytireCode>
          </Make>
        </Makes>
      </GetAllMakesResult>
    </GetAllMakesResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves all makes from the TireLibrary.

### SOAP Action
http://ws.tirewire.com/connectionscenter/commonservice/GetAllMakes

### Input Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)


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
http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionByID

### Input Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)
connectionID | int | [The ID of the connection](#get-connections-by-group-token)


## GetConnectionsByGroup

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionsByGroup"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> SOAP request.xml

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

> SOAP response.xml

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
      </GetConnectionsByGroupResult>
    </GetConnectionsByGroupResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves all Connections in a given Group.

### SOAP Action
http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionsByGroup

### Input Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connections](#creating-a-group)


## GetSupplierSystemByID

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystemByID"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> SOAP request.xml

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

> SOAP response.xml

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
http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystemByID

### Input Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
id | int | The ID of the supplier system


## GetSupplierSystems

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystems"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> SOAP request.xml

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetSupplierSystems xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <key>string</key>
    </GetSupplierSystems>
  </soap:Body>
</soap:Envelope>
```

> SOAP response.xml

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
      </GetSupplierSystemsResult>
    </GetSupplierSystemsResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves all Supplier Systems.

### SOAP Action
http://ws.tirewire.com/connectionscenter/commonservice/GetSupplierSystems

### Input Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)


## ValidateGroupToken

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/ValidateGroupToken"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> SOAP request.xml

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ValidateGroupToken xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <groupToken>string</groupToken>
    </ValidateGroupToken>
  </soap:Body>
</soap:Envelope>
```

> SOAP response.xml

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ValidateGroupTokenResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <ValidateGroupTokenResult>boolean</ValidateGroupTokenResult>
    </ValidateGroupTokenResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves all Connections in a given Group.

### SOAP Action
http://ws.tirewire.com/connectionscenter/commonservice/ValidateGroupToken

### Input Parameters
Parameter | Type | Description
--------- | ---- | -----------
groupToken | string | [The token for the group](#creating-a-group)
