## GetVehicleModels

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleModels"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/wheelsservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetVehicleModels xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <options>
        <ConnectionID>int</ConnectionID>
        <AccessKey>string</AccessKey>
        <GroupToken>string</GroupToken>
        <Year>string</Year>
        <VehicleMake>string</VehicleMake>
      </options>
    </GetVehicleModels>
  </soap:Body>
</soap:Envelope>
```

This method is used to return a list of valid models of vehicles by year & make. This method is used as the third step in the vehicle search process, which typically consists of Year > Make > Model > Results.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleModels`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
Year | string | Year to return makes for
VehicleMake | string | Make of vehicle to return models for

### Response
Returns [GetVehicleModelsResponse](#getvehiclemodels-response)