# Sql-MultiScriptDeployment
This PowerShell script can be used to deploy multiple SQL scripts from a .sql files to multiple instances and databases.

To use the script the following steps should be followed.
1. Create a database (e.g., AdminDB) and table (e.g., server_list) to store a list of SqlInstances and associated databases for deployment.
2. Make sure that you have the necessary permissions to connect to the SqlInstances and deploy the scripts on the databases. The PowerShell script uses IntegatedSecurity to avoid the use of username and password to connect to the distribution list as well as SqlInstances. If you need to use Sql authentication, just add username and password to the connection string (Line #9) and  Invoke-Sqlcmd (Line #62).
3. Keep the release scripts in one folder as .sql files. 
