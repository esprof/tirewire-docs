## GetVehicleMakes

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleMakes"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/wheelsservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetVehicleYears xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <options>
        <ConnectionID>int</ConnectionID>
        <AccessKey>string</AccessKey>
        <GroupToken>string</GroupToken>
        <Year>string</Year>
      </options>
    </GetVehicleYears>
  </soap:Body>
</soap:Envelope>
```

This method is used to return a list of valid makes of vehicles by year. This method is used as the second step in the vehicle search process, which typically consists of Year > Make > Model > Results.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleMakes`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
Year | string | Year to return makes for

### Response
Returns [GetVehicleMakesResponse](#getvehiclemakes-response)