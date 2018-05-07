## GetOrdersByGroupExtended

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/ordersservice/GetOrdersByGroupExtended"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/ordersservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetOrdersByGroupExtended xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <key>string</key>
      <groupToken>string</groupToken>
      <skip>int</skip>
      <take>int</take>
      <from>dateTime</from>
      <to>dateTime</to>
    </GetOrdersByGroupExtended>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetOrdersByGroupExtendedResponse xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <GetOrdersByGroupExtendedResult>
        <Orders>
          <Order>
            <ID>int</ID>
            <LogId>string</LogId>
            <TirewireConnectionID>int</TirewireConnectionID>
            <SubData>string</SubData>
            <SupplierSystemID>int</SupplierSystemID>
            <SupplierSystemOrderID>string</SupplierSystemOrderID>
            <Status>string</Status>
            <StatusID>int</StatusID>
            <DatePlaced>dateTime</DatePlaced>
            <Number>string</Number>
            <Notes>string</Notes>
            <DeliveryID>string</DeliveryID>
            <ShipTo xsi:nil="true" />
            <Tires xsi:nil="true" />
            <UnmappedTires xsi:nil="true" />
            <MiscProducts xsi:nil="true" />
            <Wheels xsi:nil="true" />
          </Order>
          ...
        </Orders>
        <TotalCount>int</TotalCount>
      </GetOrdersByGroupExtendedResult>
    </GetOrdersByGroupExtendedResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves orders for a Group with extended options.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/ordersservice/GetOrdersByGroupExtended`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)
skip | int | Number of orders to skip for pagination
take | int | Number of orders to return for pagination
from | dateTime | Only return orders after this date and time
to | dateTime | Only return orders before this date and time

### Response Parameters
An array of Order objects.

Parameter | Type | Description
--------- | ---- | -----------
ID | int | Connections Center order ID
LogId | string | Connections Center order log ID
TirewireConnectionID | int | Connection ID
SubData | string | SubData value provided at the time of order
SupplierSystemID | int | Connection supplier system ID
SupplierSystemOrderID | string | Supplier system order ID
Status | string | Order status
StatusID | int | Order status ID
DatePlaced | datetime | Time that the order was placed
Number | string | Purchase order number
Notes | string | Order notes
DeliveryID | int | Delivery ID
ShipTo | ShipTo | Ship-to information (if available)
Tires | [Tire](#tire-object)[] | Array of tires that successfully map to the Tirelibrary
UnmappedTires | [UnmappedTire](#unmappedtire-object)[] | Array of tires that did not map to the Tirelibrary
MiscProducts | MiscProduct[] | Array of miscellaneous products
Wheels | Wheel[] | Array of wheels

Parameter | Type | Description
--------- | ---- | -----------
TotalCount | int | Total number of orders in the provided date range
