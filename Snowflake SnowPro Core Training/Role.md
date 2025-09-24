Roles are entites that can have privileges on securable objects.

Roles are assigned to users to allow them to perform actions on these securable objects though access can be granted directly to users as well.
**Users can have multiple roles** and can switch between them for different actions depending on the required privileges.

## System-Defined Roles
There are default *system-defined roles* in a Snowflake account and **they cannot be dropped** and privileges granted to these roles **cannot be revoked.** 
[Overview of Access Control | Snowflake Documentation](https://docs.snowflake.com/en/user-guide/security-access-control-overview#label-access-control-overview-roles-system)

### GLOBALORGADMIN
* Global Organisation Admin
* Performs organisation level tasks such as managing accounts and viewing org-level usage info

### ORGADMIN
* Organisation Admin
* Regular account to manage operations at the org level
* **to be phased out in the future and replaced by GLOBALORGADMIN**

### ACCOUNTADMIN
* Account Admin
* Encapsulates SYSADMIN and SECURITYADMIN

### SECURITYADMIN
* Security Admin
* Manage object grants globally
* **Create, monitor, and manage users and roles**
* Has **MANAGE GRANTS** privilege to be able to modify any grant, including revoking it [[Privileges and Grants]]
* Inherits privileges of USERADMIN as that role is granted to SECURITYADMIN

### USERADMIN
* User and Role Admin
* Manages users and roles - can CREATE USER and CREATE ROLE in the account
* Can manage users and roles that it owns

### SYSADMIN
* System Admin
* Can create warehouses and databases (plus other objects) in an account

### PUBLIC
* Role that is automatically granted to every user and role in your account upon creation
* Can own securable objects but these objects will be owned by everyone in the account since everyone has this role

![[Pasted image 20250924172952.png]]