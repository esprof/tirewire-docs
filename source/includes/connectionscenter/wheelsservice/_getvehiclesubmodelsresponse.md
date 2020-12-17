## GetVehicleSubModels Response

> Response XML

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <GetVehicleSubModelsResponse xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
            <GetVehicleSubModelsResult>
                <ErrorCode>int</ErrorCode>
                <ErrorMessage>string</ErrorMessage>
                <SubModelsResult>
                    <FitmentSubModel>
                        <Id>int</Id>
                        <Name>string</Name>
                        <VehicleCode>string</VehicleCode>
                    </FitmentSubModel>
                    ...
                </SubModelsResult>
                <Message>string</Message>
            </GetVehicleSubModelsResult>
        </GetVehicleSubModelsResponse>
    </soap:Body>
</soap:Envelope>
```

The response from a successful GetVehicleSubModels request.
