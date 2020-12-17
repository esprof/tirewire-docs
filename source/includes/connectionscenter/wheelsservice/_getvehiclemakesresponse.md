## GetVehicleMakes Response

> Response XML

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <GetVehicleMakesResponse xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
            <GetVehicleMakesResult>
                <ErrorCode>int</ErrorCode>
                <ErrorMessage>string</ErrorMessage>
                <MakesResult>
                    <FitmentMake>
                        <Name>string</Name>
                        <MakeId>int</MakeId>
                    </FitmentMake>
                    ...
                </MakesResult>
                <Message>string</Message>
            </GetVehicleMakesResult>
        </GetVehicleMakesResponse>
    </soap:Body>
</soap:Envelope>
```

The response from a successful GetVehicleMakes request.
