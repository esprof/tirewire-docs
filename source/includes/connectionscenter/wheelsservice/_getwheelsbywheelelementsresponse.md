## GetWheelsByWheelElements Response

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetWheelsByWheelElementsResponse xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <GetWheelsByWheelElementsResult>
        <Wheels>
          <Wheel>
            <ID>int</ID>
            <ProductCode>string</ProductCode>
            <ClientProductCode>string</ClientProductCode>
            <Style>string</Style>
            <LoadRating>int</LoadRating>
            <Description>string</Description>
            <Finish>string</Finish>
            <Size>string</Size>
            <Bore>decimal</Bore>
            <Load>int</Load>
            <Offset>decimal</Offset>
            <Backside>double</Backside>
            <BoltPatterns>string</BoltPatterns>
            <ImageUrl>string</ImageUrl>
            <Brand>string</Brand>
            <Overview>string</Overview>
            <CapPartNumber>string</CapPartNumber>
            <Lip>double</Lip>
            <Weight>double</Weight>
            <LugType>string</LugType>
            <HasIconMediaImage>boolean</HasIconMediaImage>
            <RimDiameter>decimal</RimDiameter>
            <RimWidth>decimal</RimWidth>
            <ATVOffset>string</ATVOffset>
            <CustomField1>string</CustomField1>
            <Quantity>int</Quantity>
            <QuantitySecondary>int</QuantitySecondary>
            <QuantityPlus>boolean</QuantityPlus>
            <QuantityDetails xsi:nil="true" />
            <BuyPrice>decimal</BuyPrice>
            <SellPrice>decimal</SellPrice>
            <Tax>decimal</Tax>
            <IsSpecial>boolean</IsSpecial>
          </Wheel>
          <Wheel>
            <ID>int</ID>
            <ProductCode>string</ProductCode>
            <ClientProductCode>string</ClientProductCode>
            <Style>string</Style>
            <LoadRating>int</LoadRating>
            <Description>string</Description>
            <Finish>string</Finish>
            <Size>string</Size>
            <Bore>decimal</Bore>
            <Load>int</Load>
            <Offset>decimal</Offset>
            <Backside>double</Backside>
            <BoltPatterns>string</BoltPatterns>
            <ImageUrl>string</ImageUrl>
            <Brand>string</Brand>
            <Overview>string</Overview>
            <CapPartNumber>string</CapPartNumber>
            <Lip>double</Lip>
            <Weight>double</Weight>
            <LugType>string</LugType>
            <HasIconMediaImage>boolean</HasIconMediaImage>
            <RimDiameter>decimal</RimDiameter>
            <RimWidth>decimal</RimWidth>
            <ATVOffset>string</ATVOffset>
            <CustomField1>string</CustomField1>
            <Quantity>int</Quantity>
            <QuantitySecondary>int</QuantitySecondary>
            <QuantityPlus>boolean</QuantityPlus>
            <QuantityDetails xsi:nil="true" />
            <BuyPrice>decimal</BuyPrice>
            <SellPrice>decimal</SellPrice>
            <Tax>decimal</Tax>
            <IsSpecial>boolean</IsSpecial>
          </Wheel>
        </Wheels>
        <Message>string</Message>
      </GetWheelsByWheelElementsResult>
    </GetWheelsByWheelElementsResponse>
  </soap:Body>
</soap:Envelope>
```

The response from a successful GetWheelsByWheelElements request.
