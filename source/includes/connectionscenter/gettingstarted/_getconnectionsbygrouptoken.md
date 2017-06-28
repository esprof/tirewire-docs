## Get Connections by Group Token

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction:http://ws.tirewire.com/connectionscenter/commonservice/GetConnectionsByGroup"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/commonservice.asmx > response.xml
```

> request.xml

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetConnectionsByGroup xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <key>string</key>
      <groupToken>string</groupToken>
    </GetConnectionsByGroup>
  </soap:Body>
</soap:Envelope>
```

> response.xml

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetConnectionsByGroupResponse xmlns="http://ws.tirewire.com/connectionscenter/commonservice">
      <GetConnectionsByGroupResult>
        <Connections>
          <ConnectionInformation>
            <Name>string</Name>
            <WarehouseName>string</WarehouseName>
            <SupplierSystemID>int</SupplierSystemID>
            <TirewireConnectionID>int</TirewireConnectionID>
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

Now that we know our group token is valid we can go ahead and get the connection information.
