## GetWheelElements

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/wheelsservice/GetWheelElements"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/wheelsservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetWheelElements xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <options>
        <ConnectionID>int</ConnectionID>
        <AccessKey>string</AccessKey>
        <GroupToken>string</GroupToken>
        <Brand>string</Brand>
        <Style>string</Style>
        <Size>string</Size>
        <Finish>string</Finish>
        <BoltPattern>string</BoltPattern>
        <Offset>decimal</Offset>
        <Bore>decimal</Bore>
        <LoadRating>int</LoadRating>
        <RimDiameter>decimal</RimDiameter>
        <RimWidth>decimal</RimWidth>
        <MinimumOffset>decimal</MinimumOffset>
        <MaximumOffset>decimal</MaximumOffset>
      </options>
    </GetWheelElements>
  </soap:Body>
</soap:Envelope>
```

This method is used to retrieve all available wheel elements (brands, styles, finishes, sizes, etc). On the initial request, to retrieve all elements, you can specify no element properties and it will return all elements available. You can then further filter elements by adding element properties to the request. For example, if you make a request for all elements and then want to only retrieve available elements of wheels that have a rim diameter of 18, you would add RimDiameter 18 to your request which would then return only brands that contained wheels with a Rim Diameter of 18, Rim Widths of wheels that have a diameter of 18, etc.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/wheelsservice/GetWheelElements`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
Brand | string | *(optional)* Wheel Brand (Manufacturer)
Style | string | *(optional)* Wheel Style (Model)
Size | string | *(optional)* Wheel Size (Diameter x Width 18x10)
Finish | string | *(optional)* Wheel Finish
BoltPattern | string | *(optional)* Wheel Bolt Pattern / PCD (4x114.3)
Offset | decimal | *(optional)* Wheel Offset (20.00)
Bore | decimal | *(optional)* Wheel Bore (80.3)
LoadRating | int | *(optional)* Wheel Load Rating (1400)
RimDiameter | decimal | *(optional)* Wheel Rim Diameter (18.00)
RimWidth | decimal | *(optional)* Wheel Rim Width (10.00)
MinimumOffset | decimal | *(optional)* Returns offsets above specified offset, you must specify a maximum offset to use minimum offset. This is used to retrieve an offset range.
MaximumOffset | decimal | *(optional)* Returns offsets below specified offset, you must specify a minimum offset to use maximum offset. This is used to retrieve an offset range.

### Response
Returns [GetWheelElementsResponse](#getwheelelements-response)