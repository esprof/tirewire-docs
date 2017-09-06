## UnmappedTire Object

Unmapped tire when a match could not be made to the Tirelibrary

### Object Parameters
Parameter | Type | Description
--------- | ---- | -----------
ClientProductCode | string | Product code from supplier system
ClientMake | string | Make name from supplier system
ClientMakeAbbreviation | string | Make abbreviation from supplier system
ClientMakeID | int | Make ID from suppler system
ClientDescription | string | Description from supplier system
ProductCode | string | Product code
Make | string | Make name from Tirelibrary
MakeID | int | Tirelibrary make ID
PlyRating | string | Ply Rating
BuyPrice | decimal | Buy price from supplier system
SellPrice | decimal | Sell price either from supplier system (if available) or marked up from buy price (if markups set)
Tax | decimal | FET value from supplier system (if available)
Quantity | int | Primary stock quantity
QuantitySecondary | int | Secondary stock quantity
Quantities | string[] | *(internal)*
IsSpecial | boolean | Is special pricing
GBB | int | Good Better Best (1 = Good, 2 = Better, 3 = Best, -1 Default)
ItemFlag | int | *(internal)*
ConnectionID | int | Connection ID
Notes | string | *(internal)*
Programs | TireProgram[] | *(internal)*
TireClasses | TireClass[] | Classes that provide a general grouping for tires
