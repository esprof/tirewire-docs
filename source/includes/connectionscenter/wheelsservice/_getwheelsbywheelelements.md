## GetWheelsByWheelElements

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/wheelsservice/GetWheelsByWheelElements"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/wheelsservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetWheelsByWheelElements xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <options>
        <ConnectionID>int</ConnectionID>
        <AccessKey>string</AccessKey>
        <GroupToken>string</GroupToken>
        <ExcludeZeroStock>boolean</ExcludeZeroStock>
        <InventoryOption>All or Positive or Zero</InventoryOption>
        <Brand>string</Brand>
        <Style>string</Style>
        <ProductCodes>
          <string>string</string>
          <string>string</string>
        </ProductCodes>
        <Size>string</Size>
        <Finish>string</Finish>
        <BoltPattern>string</BoltPattern>
        <Offset>decimal</Offset>
        <OffsetMinimum>decimal</OffsetMinimum>
        <OffsetMaximum>decimal</OffsetMaximum>
        <LoadRating>int</LoadRating>
        <Bore>decimal</Bore>
        <RimDiameter>decimal</RimDiameter>
        <RimWidth>decimal</RimWidth>
        <ProductCodeSearch>boolean</ProductCodeSearch>
        <ProductCodeSearchLikeness>boolean</ProductCodeSearchLikeness>
        <AccountCode>string</AccountCode>
      </options>
    </GetWheelsByWheelElements>
  </soap:Body>
</soap:Envelope>
```

Retrieves wheels by wheel elements. This method should be used after the [GetWheelElements](#getwheelelements) method to ensure the search contains valid wheel criteria for the search.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/wheelsservice/GetWheelsByWheelElements`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
AccessKey | string | [Access Key](#access-keys)
GroupToken | string | [The token for the group containing the connection](#creating-a-group)
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
ExcludeZeroStock | boolean | *(optional)* Excludes items with zero stock
InventoryOption | string | *(optional)* Specify whether to return all, positive or negative inventory. <br>Allowed Values: All, Positive, Negative
Brand | string | *(optional)* Brand of wheel to retrieve
Style | string | *(optional)* Style of wheel to retrieve
ProductCodes | string array | *(optional)* List of product codes to retrieve by, set ProductCodeSearch to true if using ProductCodes parameter.
Size | string | *(optional)* Size of wheels to retrieve by (18x10)
Finish | string | *(optional)* Finish of wheel to retrieve
BoltPattern | string | *(optional)* Bolt Pattern / PCD of wheel (4x114.3)
Offset | decimal | *(optional)* Offset of wheel (20.00)
OffsetMinimum | decimal | *(optional)* Offset range to retrieve wheels by (must include OffsetMaximum if using OffsetMinimum).
OffsetMaximum | decimak | *(optional)* Offset range to retrieve wheels by (must include OffsetMinimum if using OffsetMaximum).
LoadRating | int | *(optional)* Load Rating to retrieve wheels by (1400)
Bore | decimal | *(optional)* Center Bore to retrieve wheels by (80.3)
RimDiameter | decimal | *(optional)* Rim Diameter to retrieve wheels by (18.00)
RimWidth | decimal | *(optional)* Rim Width to retrieve wheels by (10.00)
ProductCodeSearch | boolean | *(optional)* Specify whether this search is a product code search, required if using ProductCodes parameter.
ProductCodeSearchLikeness | boolean | *(optional)* Specify whether the product code search should search product codes by likeness (ABC-% instead of ABC-123 for example)
AccountCode | string | *(optional)* AccountCode to use for search

### Response
Returns [GetWheelsByWheelElementsResponse](#getwheelsbywheelelements-response)
