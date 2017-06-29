## Methods
Note: All methods require an Access Key (string) to be provided – this has been omitted from the Parameters column below for simplicity.

Name | Description | Parameters | Returns
---- | ----------- | ---------- | -------
**GetAllMakes** | Retrieves all makes from the TireLibrary. | | A list of Tire Makes from the Tirelibary database, including Make IDs (required by some Web Service methods).
**GetConnectionByID** | Retrieves a Connection by ID. | int ConnectionID, string GroupToken | Returns information on the requested Connection including ID, Name, and Supplier System ID.
**GetConnectionsByGroup** | Retrieves all Connections in a given Group. | string GroupToken | Returns information on all the Connections in the supplied Group including ID, Name, and Supplier System ID.
**GetSupplierSystemByID** | Retrieves a Supplier System by its ID. | int ID | Returns information on the requested Supplier System including Name, Image URL and other fields which are used internally by the Connections Center.
**GetSupplierSystems**
Retrieves all Supplier Systems. | | Returns information on all Supplier Systems including Name, Image URL and other fields which are used internally by the Connections Center.
**ValidateGroupToken**
Checks whether a Group Token is valid. | string GroupToken | Returns true or false
