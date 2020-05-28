# Azure SQL Server Database Deployment Template

Deploy an Azure SQL Server that contains a single database. This template is
often embedded into more complex deployments. Thus, it's highly parameterised.
Azure SQL is a managed service. It's readily scaled up and down to meet demand,
and is effectively serverless.

This deployment prevents access to the database from everywhere except a given
subnet (the 'service subnet'). This template is well-suited for deploying a
private database backing an Azure App Service or a kubernetes deployment.

[![Deploy Button](https://raw.githubusercontent.com/specialised-systems/azure-templates/master/images/deploy-to-azure-button.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fspecialised-systems%2Fazure-templates%2Fmaster%2Ftemplates%2Fazure-sql-server-database%2Fdeploy.json)
