## Tire Object

Mapped tire with data from the Tirelibrary

### Object Parameters
Parameter | Type | Description
--------- | ---- | -----------
ID | int | Tirelibrary tire ID
ProductCode | string | Manufacturer product code from Tirelibrary
ClientProductCode | string | Product code from supplier system
Name | string | Product name from Tirelibrary
ClientName | string | Product name from supplier system
BuyPrice | decimal | Buy price from supplier system
SellPrice | decimal | Sell price either from supplier system (if available) or marked up from buy price (if markups set)
Tax | decimal | FET value from supplier system (if available)
Quantity | int | Primary stock quantity
QuantitySecondary | int | Secondary stock quantity
Quantities | string[] | *(internal)*
Make | string | Make name from Tirelibrary
MakeID | int | Tirelibrary make ID
Pattern | string | Pattern name from Tirelibrary
PatternID | int | Tirelibrary pattern ID
Description | string | Description from Tirelibrary
SizeID | int | Tirelibrary size ID
ImageURL | string | Tire image URL from Tirelibrary
Width | double | Width (mm)
AspectRatio | double | Aspect Ratio (%)
Rim | double | Rim Size (inch)
InchWidth | double | Inch Width (inch)
Diameter | double | Diameter (inch)
MetricRim | double | Metric Rim Diameter (mm)
Weight | double | Weight (lbs)
SpeedRating | string | Speed Rating
LoadRating | string | Load Rating (Single/Double)
PlyRating | string | Ply Rating
UTQG | string | UTQG
LoadCapacity | string | Load Capacity (lbs)
InflationPressure | double | Inflation Pressure (psi)
Sidewall | string | Sidewall
LoadRange | string | Load Range
ApprovedRimWidth | string | Approved Rim Width (inch)
MeasuringRimWidth | string | Measuring Rim Width (inch)
SectionWidth | string | Section Width
MeasuredOD | string | Overall Diameter (inch)
TreadDepth | string | Tread Depth (1/32")
RevsPerMile | string | Revolutions Per Mile
MaxLoadSingle | string | Load Capacity Single (lbs)
MaxLoadDual | string | Load Capacity Dual (lbs)
Features | string | Features
Benefits | string | Benefits
Has360Image | boolean | Has 360 degree tire images
MaxInflationPressure | string | Max Inflation Pressure
IsSpecial | boolean | Is special pricing
Warranty | boolean | Warranty (miles)
SupplierSystemID | int | Supplier system ID
ConnectionID | int | Connection ID
TireClasses | TireClass[] | Classes that provide a general grouping for tires
Programs | TireProgram[] | *(internal)*
TireMake | TireMake | Tire make information (ID, Name, Image URL)
ClientDescription | string | Description from supplier system
GMProductCode | string | GM product code
GBB | int | Good Better Best (1 = Good, 2 = Better, 3 = Best, -1 Default)
ItemFlag | int | *(internal)*
Notes | string | *(internal)*
unusedlw | string | *(internal)*
unusedmd | string | *(internal)*
unusedhg | string | *(internal)*
unusedsp | string | *(internal)*
FeaturesArray | string[] | Features (separated out by line)
BenefitsArray | string[] | Benefits (separated out by line)
