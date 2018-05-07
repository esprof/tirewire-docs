## GetTires Response

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetTiresResponse xmlns="http://ws.tirewire.com/connectionscenter/productsservice">
      <GetTiresResult>
        <Tires>
          <Tire>
            <ID>int</ID>
            <ProductCode>string</ProductCode>
            <ClientProductCode>string</ClientProductCode>
            <Name>string</Name>
            <ClientName>string</ClientName>
            <BuyPrice>decimal</BuyPrice>
            <SellPrice>decimal</SellPrice>
            <Tax>decimal</Tax>
            <Quantity>int</Quantity>
            <QuantitySecondary>int</QuantitySecondary>
            <Quantities xsi:nil="true" />
            <Make>string</Make>
            <MakeID>int</MakeID>
            <Pattern>string</Pattern>
            <PatternID>int</PatternID>
            <Description>string</Description>
            <SizeID>int</SizeID>
            <ImageURL>string</ImageURL>
            <Width>double</Width>
            <AspectRatio>double</AspectRatio>
            <Rim>double</Rim>
            <InchWidth>double</InchWidth>
            <Diameter>double</Diameter>
            <MetricRim>double</MetricRim>
            <Weight>double</Weight>
            <SpeedRating>string</SpeedRating>
            <LoadRating>string</LoadRating>
            <PlyRating>string</PlyRating>
            <UTQG>string</UTQG>
            <LoadCapacity>string</LoadCapacity>
            <InflationPressure>int</InflationPressure>
            <Sidewall>string</Sidewall>
            <LoadRange>string</LoadRange>
            <ApprovedRimWidth>string</ApprovedRimWidth>
            <MeasuringRimWidth>string</MeasuringRimWidth>
            <SectionWidth>string</SectionWidth>
            <MeasuredOD>string</MeasuredOD>
            <TreadDepth>string</TreadDepth>
            <RevsPerMile>string</RevsPerMile>
            <MaxLoadSingle>string</MaxLoadSingle>
            <MaxLoadDual>string</MaxLoadDual>
            <Features>string</Features>
            <Benefits>string</Benefits>
            <Has360Image>boolean</Has360Image>
            <MaxInflationPressure>string</MaxInflationPressure>
            <IsSpecial>boolean</IsSpecial>
            <Warranty>string</Warranty>
            <SupplierSystemID>int</SupplierSystemID>
            <ConnectionID>int</ConnectionID>
            <TireClasses xsi:nil="true" />
            <Programs xsi:nil="true" />
            <TireMake xsi:nil="true" />
            <ClientDescription>string</ClientDescription>
            <GMProductCode>string</GMProductCode>
            <GBB>int</GBB>
            <ItemFlag>int</ItemFlag>
            <Notes>string</Notes>
            <unusedlw>string</unusedlw>
            <unusedmd>string</unusedmd>
            <unusedhg>string</unusedhg>
            <unusedsp>string</unusedsp>
            <FeaturesArray xsi:nil="true" />
            <BenefitsArray xsi:nil="true" />
          </Tire>
          ...
        </Tires>
        <UnmappedTires>
          <UnmappedTire>
            <ClientProductCode>string</ClientProductCode>
            <ClientMake>string</ClientMake>
            <ClientMakeAbbreviation>string</ClientMakeAbbreviation>
            <ClientMakeID>int</ClientMakeID>
            <ClientDescription>string</ClientDescription>
            <ProductCode>string</ProductCode>
            <Make>string</Make>
            <MakeID>int</MakeID>
            <PlyRating>string</PlyRating>
            <BuyPrice>decimal</BuyPrice>
            <SellPrice>decimal</SellPrice>
            <Tax>decimal</Tax>
            <Quantity>int</Quantity>
            <QuantitySecondary>int</QuantitySecondary>
            <Quantities xsi:nil="true" />
            <IsSpecial>boolean</IsSpecial>
            <GBB>int</GBB>
            <ItemFlag>int</ItemFlag>
            <ConnectionID>int</ConnectionID>
            <Notes>string</Notes>
            <Programs xsi:nil="true" />
            <TireClasses xsi:nil="true" />
          </UnmappedTire>
          ...
        </UnmappedTires>
        <UnmappedCount>int</UnmappedCount>
        <LogID>int</LogID>
        <LogIDs>
          <int>int</int>
          <int>int</int>
        </LogIDs>
        <Message>string</Message>
        <SLogID>guid</SLogID>
      </GetTiresResult>
    </GetTiresResponse>
  </soap:Body>
</soap:Envelope>
```

The response from a successful GetTires request.

### Response Parameters
Parameter | Type | Description
--------- | ---- | -----------
Tires | [Tire](#tire-object)[] | Array of tires that successfully map to the Tirelibrary
UnmappedTires | [UnmappedTire](#unmappedtire-object)[] | Array of tires that did not map to the Tirelibrary
UnmappedCount | int | Number of unmapped tires
LogID | int | *(internal)* The log ID
LogIDs | int[] | *(internal)* The log IDs
Message | string | Message from the supplier system
SLogID | guid | *(internal)* Speed log ID
