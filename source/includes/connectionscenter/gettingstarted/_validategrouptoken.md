## Validate Group Token

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/commonservice/ValidateGroupToken"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ValidateGroupToken xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <groupToken>string</groupToken>
    </ValidateGroupToken>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ValidateGroupTokenResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <ValidateGroupTokenResult>boolean</ValidateGroupTokenResult>
    </ValidateGroupTokenResponse>
  </soap:Body>
</soap:Envelope>
```

Part of the authentication for the Connection Center web services is the information stored in your connections. To retrieve the connection information we need to use our group token that was obtained before.

First we will check and see if our group token is valid.
