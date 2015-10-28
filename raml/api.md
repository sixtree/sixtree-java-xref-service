# Sixtree Xref API documentation version v1
http://mocksvc.mulesoft.com/mocks/55209f41-93cc-4a7b-a470-f9af3749e479/v1/

---

## /xref

### /xref

* **get**: Returns the usage of the API

### /xref/{tenant}

* **get**: List the Entity Sets for this Tenant

### /xref/{tenant}/{entitySet}

* **get**: Return information about an Entity Set such as the count of Relations and their names (eg. Salesforce, SAP)
* **post**: Create a new Relation for this Entity Set
* **put**: Update a Relation to add or modify a Reference. If the Reference Endpoint exists, it will overwrite what exists. If it does not exist it will create a new Reference

### /xref/{tenant}/{entitySet}/{commonId}

* **get**: Retrieves a specific Relation identified by this Common ID

### /xref/{tenant}/{entitySet}/{commonId}/{endpoint}

* **delete**: Deletes a Reference identified by this Endpoint name from the Relation identified by this Common ID. Eg. http://localhost:27017/xref/viva/customer/55f623ace41d5524d0000001/SAP - note that this is case sensitive and "sap" is not the same endpoint.

### /xref/{tenant}/{entitySet}/{commonId}/{endpoint}/{id}

* **put**: Add or update the Reference for this Endpoint for the Relation identified by this Common ID. Eg. http://localhost:27017/xref/viva/customer/55f623ace41d5524d0000001/sap/11111

