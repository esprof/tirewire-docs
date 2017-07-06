## GetTires (By Width, Aspect & Rim)

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
        <Width>string</Width>
        <Aspect>string</Aspect>
        <Rim>string</Rim>
      </options>
    </GetTires>
  </soap:Body>
</soap:Envelope>
```

Retrieves tire(s) by size, specified as width, aspect ratio and rim size.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/productsservice/GetTires`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
Width | string | Tire width (eg. 205)
Aspect | string | Tire aspect ratio (eg. 65)
Rim | string | Tire rim size (eg. 15)

### Response
Returns [GetTiresResponse](#gettires-response)
