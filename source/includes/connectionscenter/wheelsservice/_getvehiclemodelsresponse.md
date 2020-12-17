## GetVehicleModels Response

> Response XML

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <GetVehicleModelsResponse xmlns="http://ws.tirewire.com/connectionscenter/wheelsservice">
            <GetVehicleModelsResult>
                <ErrorCode>int</ErrorCode>
                <ErrorMessage>string</ErrorMessage>
                <ModelsResult>
                    <FitmentModel>
                        <Name>string</Name>
                        <VehicleCode>string</VehicleCode>
                        <MoreData>boolean</MoreData>
                        <ModelId>int</ModelId>
                    </FitmentModel>
                    <FitmentModel>
                        <Name>string</Name>
                        <VehicleCode>string</VehicleCode>
                        <MoreData>boolean</MoreData>
                        <ModelId>int</ModelId>
                    </FitmentModel>
                </ModelsResult>
            </GetVehicleModelsResult>
        </GetVehicleModelsResponse>
    </soap:Body>
</soap:Envelope>
```

The response from a successful GetVehicleModels request. If MoreData is true and VehicleCode is empty, you must do a model search before proceeding to get wheels by vehicle. Otherwise, you can use VehicleCode to retrieve wheels.
