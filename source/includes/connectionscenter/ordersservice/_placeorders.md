## PlaceOrders

```shell
curl -p
  -H "Content-Type: text/xml;charset=UTF-8"
  -H "SOAPAction: http://ws.tirewire.com/connectionscenter/ordersservice/PlaceOrders"
  -d @request.xml
  http://ws.tirewire.com/connectionscenter/ordersservice.asmx > response.xml
```

> Request XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlaceOrders xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <accessKey>string</accessKey>
      <groupToken>string</groupToken>
      <ordersToPlace>
        <UnplacedOrder>
          <ConnectionID>int</ConnectionID>
          <SubData>string</SubData>
          <OrderNumber>string</OrderNumber>
          <Notes>string</Notes>
          <DeliveryID>string</DeliveryID>
          <ShipTo>
            <Code>string</Code>
            <Title>string</Title>
            <AddressLine1>string</AddressLine1>
            <AddressLine2>string</AddressLine2>
            <City>string</City>
            <State>string</State>
            <ZIP>int</ZIP>
          </ShipTo>
          <Tires>
            <UnplacedOrderTire>
              <ClientProductCode>string</ClientProductCode>
              <Quantity>int</Quantity>
              <Price>decimal</Price>
              <Tax>decimal</Tax>
            </UnplacedOrderTire>
            ...
          </Tires>
          <UnmappedTires>
            <UnplacedOrderUnmappedTire>
              <ClientProductCode>string</ClientProductCode>
              <Make>string</Make>
              <Quantity>int</Quantity>
              <Price>decimal</Price>
              <Tax>decimal</Tax>
            </UnplacedOrderUnmappedTire>
            ...
          </UnmappedTires>
          <MiscProducts>
            <UnplacedOrderMiscProduct>
              <ClientProductCode>string</ClientProductCode>
              <Make>string</Make>
              <Quantity>int</Quantity>
              <Price>decimal</Price>
              <Tax>decimal</Tax>
            </UnplacedOrderMiscProduct>
            ...
          </MiscProducts>
          <Wheels>
            <UnplacedOrderWheel>
              <ClientProductCode>string</ClientProductCode>
              <Quantity>int</Quantity>
              <Price>decimal</Price>
              <Tax>decimal</Tax>
            </UnplacedOrderWheel>
            ...
          </Wheels>
        </UnplacedOrder>
        ...
      </ordersToPlace>
    </PlaceOrders>
  </soap:Body>
</soap:Envelope>
```

> Response XML

```xml
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetAllOrdersByConnectionResponse xmlns="http://ws.tirewire.com/connectionscenter/ordersservice">
      <GetAllOrdersByConnectionResult>
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
      </GetAllOrdersByConnectionResult>
    </GetAllOrdersByConnectionResponse>
  </soap:Body>
</soap:Envelope>
```

Places orders. (Delivery information, including IDs, can be retrieved using the GetDeliveryOptions method).

### SOAP Action
`http://ws.tirewire.com/connectionscenter/ordersservice/PlaceOrders`

### Request Parameters
Parameter | Type | Description
--------- | ---- | -----------
key | string | [Access Key](#access-keys)
groupToken | string | [The token for the group containing the connection](#creating-a-group)
ordersToPlace | [UnplacedOrder](#unplacedorder)[] | Array of UnplacedOrder objects

#### UnplacedOrder
Parameter | Type | Description
--------- | ---- | -----------
ConnectionID | int | [The ID of the connection](#get-connections-by-group-token)
SubData | string | SubData override
OrderNumber | string | Purchase order number
Notes | string | Order notes
DeliveryID | string | [Delivery option identifying code](#getdeliveryoptions)
ShipTo | ShipTo | *(optional)* [Ship-to information](#getshiptooptions)<br>**Not supported/required by all supplier systems**
Tires | UnplacedOrderTire[] | *(optional)* Array of UnplacedOrderTire objects
UnmappedTires | UnplacedOrderUnmappedTire[] | *(optional)* Array of UnplacedOrderUnmappedTire objects (Make name must be provided)
MiscProducts | UnplacedOrderMiscProduct[] | *(optional)* Array of UnplacedOrderMiscProduct objects (Make name must be provided)
Wheels | UnplacedOrderWheel[] | *(optional)* Array of UnplacedOrderWheel objects

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
