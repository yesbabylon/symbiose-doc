## Identity

### Partner

Contacts, suppliers, customers, and customer contacts all inherit from the 'Partner' class but are stored in separate tables.

Since it's not possible to retrieve all derived objects of 'Partner' when modifying a value within an Identity, we do not store computed/related fields (firstname, lastname, addres, ...).

To search among all partners, we use a specific controller (providing virtual entities) that uses parameters to search amongst each type of entity and provides results using only common fields from Partner. The controller performs searches on derived fields (firstname, lastname, address) based on related identities.