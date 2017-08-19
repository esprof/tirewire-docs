## GetTires (Product Codes)

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/productsservice/GetTires"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/productsservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetTires xmlns="http://ws.tirewire.com/connectionscenter/productsservice">
      <options>
        <AccessKey>string</AccessKey>
        <GroupToken>string</GroupToken>
        <ConnectionID>int</ConnectionID>
        <ProductCodes>
          <string>string</string>
          ...
        </ProductCodes>
      </options>
    </GetTires>
  </soap:Body>
</soap:Envelope>
```

Retrieves tire(s) by product codes.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/productsservice/GetTires`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
ProductCodes | string[] | Manufacturer product codes

### Response
Returns [GetTiresResponse](#gettires-response)
