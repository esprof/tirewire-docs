## GetWheelElements Response

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetWheelElementsResponse xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
      <GetWheelElementsResult>
        <BoltPatterns>
          <string>string</string>
          <string>string</string>
        </BoltPatterns>
        <Brands>
          <string>string</string>
          <string>string</string>
        </Brands>
        <Finishes>
          <string>string</string>
          <string>string</string>
        </Finishes>
        <Sizes>
          <string>string</string>
          <string>string</string>
        </Sizes>
        <Styles>
          <string>string</string>
          <string>string</string>
        </Styles>
        <LoadRatings>
          <int>int</int>
          <int>int</int>
        </LoadRatings>
        <Offsets>
          <decimal>decimal</decimal>
          <decimal>decimal</decimal>
        </Offsets>
        <Bores>
          <decimal>decimal</decimal>
          <decimal>decimal</decimal>
        </Bores>
        <RimDiameters>
          <decimal>decimal</decimal>
          <decimal>decimal</decimal>
        </RimDiameters>
        <RimWidths>
          <decimal>decimal</decimal>
          <decimal>decimal</decimal>
        </RimWidths>
        <Message>string</Message>
      </GetWheelElementsResult>
    </GetWheelElementsResponse>
  </soap:Body>
</soap:Envelope>
```

The response from a successful GetWheelElements request.
