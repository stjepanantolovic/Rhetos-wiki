## Roles

By using a hierarchy of **roles**, the administrator can create groups of users and permissions, or connect them directly.

For automatic synchronization of Rhetos user roles with the user groups in Active Directory,
add the [ActiveDirectorySync](https://github.com/Rhetos/ActiveDirectorySync) plugin package to the Rhetos applications. This will allow the domain administrator to set the user permissions in the Rhetos application.

## Claims

Each record in a *Common.Claim* entity represents a basic element of access. is an operation on an entity (read/insert/update/delete) or an action.

The list of claims (the *Common.Claim* entity) is created on deployment, and does not change during run-time.
There are claims generated for each of the following objects:

* For each entity: Read, New, Edit, Remove
* For each read-only data structure: Read
* For each action: Execute
* For each report: Download

A custom claim can be created in a DSL script by using the CustomClaim concept. Example:

    CustomClaim 'SomeModule.SomeResource' 'CustomOperationName';

## See also

* [User authentication and authorization](https://github.com/Rhetos/Rhetos/wiki/User-authentication-and-authorization) - Other options for user authorization.