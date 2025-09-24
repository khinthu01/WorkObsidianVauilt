Every securable object resides within a **logical container** in a hierarchy of containers. 

Top most is the **ORGANISATION**
Followed by **Account**

All objects in your Snowflake Account are contained in the account object.

![[Pasted image 20250924164716.png]]

## Ownership Privilege
To own an object means that a ROLE has the OWNERSHIP privilege on that object. **Each securable object is owned by a single role** - by default, this is the role used to create the object. When this role is assigned to users, they have shared control over the object. 

**GRANT OWNERSHIP** *transfers* ownership - multiple roles cannot own an object at once. ([[Privileges and Grants]])

The owner role **has all privileges on the object by default** including the ability **to grant or revoke privileges on the object.** 
*Exception: in managed access schemas object owners don't have grant privileges - only the schema owner or a role with MANAGE GRANTS ([[Privileges and Grants]]) can grant privileges on objects in the schema.*

> [!NOTE] Question
> Can an owner revoke certain privileges from themselves without transferring that privileges - for example, is it possible for a role to lose the privilege to grant privileges to an object?

