## GetVehicleSubModels

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleSubModels"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/wheelsservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetVehicleSubModels xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <options>
        <ConnectionID>int</ConnectionID>
        <AccessKey>string</AccessKey>
        <GroupToken>string</GroupToken>
        <Year>string</Year>
        <VehicleMake>string</VehicleMake>
        <VehicleModel>string</VehicleModel>
      </options>
    </GetVehicleSubModels>
  </soap:Body>
</soap:Envelope>
```

This method is used to return a list of valid submodels of vehicles by year, make & model. This method is only used if required, some vehicle searches do not require a sub model lookup, however if it's specified that it is required to lookup the sub model before searching wheels by vehicle then this is the last step before searching by vehicle.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleSubModels`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
Year | string | Year to return makes for
VehicleMake | string | Make of vehicle to return models for
VehicleModel | string | Model of vehicle to return submodels for

### Response
Returns [GetVehicleSubModelsResponse](#getvehiclesubmodels-response)