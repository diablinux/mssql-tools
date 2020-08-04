# mssql-tools (Linux Container with mssql-tools preloaded)
## Kubernetes cronjob to exec Store Procedures or run queries on MSSQL Server Databases in Azure

Combine Kubernetes and SQL Server Databases to improve your workflows or maintenance tasks with this data pipeline.

This yaml will create the cronjob only, make sure you have a namespace (in this case mssql-jobs) and the secret (mssql-jobs-secret) to store your credentials to access the SQL Database.

To create the namespace you can use this command:

`kubectl create namespace mssql-jobs`

To create the secret you can use this command:

`kubectl create secret generic mssql-jobs-secret --from-literal=username=DB_Username --from-literal=password=DB_Password -n mssql-jobs`

The sqlcmd utility lets you enter Transact-SQL statements, system procedures, and script files through a variety of available modes:

* At the command prompt.
* In Query Editor in SQLCMD mode.
* In a Windows script file.
* In an operating system (Cmd.exe) job step of a SQL Server Agent job.
The utility uses ODBC to execute Transact-SQL batches.

Take a look at sqlcmd utility documentation:
https://docs.microsoft.com/en-us/sql/tools/sqlcmd-utility?view=sql-server-ver15


