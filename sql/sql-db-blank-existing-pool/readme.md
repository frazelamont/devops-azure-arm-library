# Creates a new blank sql database within an existing sql elastic pool

Use this template when you want to add a new blank sql database to an existing sql elastic pool.  

> Note: the sql elastic pool must exist within the resource group that is the target for a deployment with this template

# Inputs

| Name | Purpose |
|-|-|
|`location`|the location of the resource group in which the deployment is happening|
|`sqlServerName`|The name of the sql server resource, excluding .database.windows.net|
|`sqlPoolName`|The name of the sql elastic pool|
|`sqlDbName`|The name of the database to create|
|`sqlDbUserId`|The user id to use when constructing the returned connection string|
|`sqlDbUserPassword`|The user password to use when constructing the returned connection string|
|`sqlDbEnableTDE`|Whether to enable TDE (transparent database encryption), defaults to `true`|
|`sqlDbCollation`|What collation to use for the newly created database, defaults to `SQL_Latin1_General_CP1_CI_AS`|

# Outputs
| Name | Purpose |
|-|-|
|`sqlServerFqdn`|`string` containing the fully qualifed domain name for the sql server containing the database|
|`sqlDbName`|`string` containing the name of the database|