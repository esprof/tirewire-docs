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
`http://ws.tirewire.com/connectionscenter/commonservice/GetAllMakes`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
