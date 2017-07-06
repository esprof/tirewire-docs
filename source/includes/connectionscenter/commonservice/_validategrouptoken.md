## ValidateGroupToken

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/ValidateGroupToken"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ValidateGroupToken xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <groupToken>string</groupToken>
    </ValidateGroupToken>
  </soap:Body>
</soap:Envelope>
```

> Response XML

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
`http://ws.tirewire.com/connectionscenter/commonservice/ValidateGroupToken`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
groupToken | string | [The token for the group](#creating-a-group)
