## GetVehicleWheels Response

> Response XML

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetVehicleWheelsResponse xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <GetVehicleWheelsResult>
        <WheelsResult>
          <FitmentWheel>
            <Id>int</Id>
            <ProductCode>string</ProductCode>
            <ClientProductCode>string</ClientProductCode>
            <Brand>string</Brand>
            <Style>string</Style>
            <Finish>string</Finish>
            <Size>string</Size>
            <PCD>string</PCD>
            <Offset>decimal</Offset>
            <ImageUrl>string</ImageUrl>
            <ImageUrl2>string</ImageUrl2>
            <Description>string</Description>
            <Weight>string</Weight>
            <Bore>decimal</Bore>
            <Backside>decimal</Backside>
            <TireSize>string</TireSize>
            <Price>decimal</Price>
            <LoadRating>int</LoadRating>
            <Quantity xsi:nil="true" />
            <IMImages xsi:nil="true" />
            <Wheel xsi:nil="true" />
            <HasIconMediaImage>boolean</HasIconMediaImage>
          </FitmentWheel>
          ...
        </WheelsResult>
        <Message>string</Message>
      </GetVehicleWheelsResult>
    </GetVehicleWheelsResponse>
  </soap:Body>
</soap:Envelope>
```

The response from a successful GetVehicleWheels request.
