Lab followed: [[Process PII data using Snowflake RBAC, DAC, Row Access Policies, and Column Level Security](https://quickstarts.snowflake.com/guide/getting_started_with_pii/index.html?index=..%2F..index#0)]([Process PII data using Snowflake RBAC, DAC, Row Access Policies, and Column Level Security](https://quickstarts.snowflake.com/guide/getting_started_with_pii/index.html?index=..%2F..index#0))## How Priveleges are Granted and Revoked

## Access Control Framework
Source: [Overview of Access Control | Snowflake Documentation](https://docs.snowflake.com/en/user-guide/security-access-control-overview)

Snowflake has three different types of access control:
* **Discretionary Access Control (DAC):** Each object has an owner, who can in turn grant access to that object
* **Role-based Access Control (RBAC):** Access privileges are assigned to roles, which are in turn assigned to users
* **User-based Access Control (UBAC):** Access privileges are assigned directly to users. **Access control considers privileges assigned directly to users only when USE SECONDARY ROLE is set to ALL.**

Key concepts relating to access control:
* **[[Securable Object]]**: the object that access can be granted to. 
* [[Role]]: an entity to which privileges can be granted
* [[Privileges and Grants]]: a defined level of access to an object. Multiple distinct privileges may be used to control the granularity of access granted.
* [[User]]: a user identity recognised by Snowflake, whether associated with a person or service. a user is so an entity that privileges can be granted to.

In essence, in Snowflake privileges can be granted to role or user to access a securable object. 
Roles can be assigned to users or other roles and granting a role to another role creates a [[role hierarchy]].

![[Pasted image 20250924164618.png]]


## Role Hierarchy and Privilege Inheritance
Source: https://docs.snowflake.com/en/user-guide/security-access-control-overview#label-role-hierarchy-and-privilege-inheritance

