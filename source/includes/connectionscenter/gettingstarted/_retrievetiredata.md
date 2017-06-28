## Retrieve Tire Data

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction:http://ws.tirewire.com/connectionscenter/productsservice/GetTires"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/productsservice.asmx > response.xml
```

> request.xml

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:prod="http://ws.tirewire.com/connectionscenter/productsservice">
  <soap:Header/>
  <soap:Body>
    <prod:GetTires>
      <prod:options>
        <prod:AccessKey>string</prod:AccessKey>
        <prod:GroupToken>string</prod:GroupToken>
        <prod:ConnectionID>int</prod:ConnectionID>
        <prod:Width>string</prod:Width>
        <prod:Aspect>string</prod:Aspect>
        <prod:Rim>string</prod:Rim>
      </prod:options>
    </prod:GetTires>
  </soap:Body>
</soap:Envelope>
```

Finally, knowing the connection ID, we can query it for stock. We'll begin with a simple size search.
