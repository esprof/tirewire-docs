# Orders Web Service

The Orders Web Service contains methods related to retrieving orders, delivery/shipping information, and placing orders.

### URL
http://ws.tirewire.com/connectionscenter/ordersservice.asmx

### WSDL
http://ws.tirewire.com/connectionscenter/ordersservice.asmx?wsdl

<aside class="notice">
Only the GetTires method in the Products Web Service is currently used, the other methods shown at the URL are now obsolete.
</aside>

The GetTires method requires a GetTiresOptions object to be provided. The type of tire search that is performed will depend on which of the GetTiresOptions properties are populated.
