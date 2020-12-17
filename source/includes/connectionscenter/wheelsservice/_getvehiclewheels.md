## GetVehicleWheels

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleWheels"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/wheelsservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetVehicleWheels xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <options>
        <ConnectionID>int</ConnectionID>
        <AccessKey>string</AccessKey>
        <GroupToken>string</GroupToken>
        <VehicleCode>string</VehicleCode>
      </options>
    </GetVehicleWheels>
  </soap:Body>
</soap:Envelope>
```

This method returns wheels for a vehicle lookup.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/wheelsservice/GetVehicleWheels`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
VehicleCode | string | VehicleCode returned from Model or Submodel lookup.

### Response
Returns [GetVehicleWheelsResponse](#getvehiclewheels-response)