## GetAllOrdersByGroup

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/ordersservice/GetAllOrdersByGroup"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/ordersservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetAllOrdersByGroup xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <key>string</key>
      <groupToken>string</groupToken>
    </GetAllOrdersByGroup>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetAllOrdersByGroupResponse xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <GetAllOrdersByGroupResult>
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
      </GetAllOrdersByGroupResult>
    </GetAllOrdersByGroupResponse>
  </soap:Body>
</soap:Envelope>
```

Retrieves all orders for a Group.

### SOAP Action
`http://ws.tirewire.com/connectionscenter/ordersservice/GetAllOrdersByGroup`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)

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
