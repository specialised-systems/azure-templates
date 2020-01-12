# SonarQube Deployment Template

Deploy SonarQube, backed by an Azure SQL Server Database. SonarQube's docker
image is deployed as an Azure WebApp inside a new App Service Environment. Once
deployed, SonarQube is only visible internally.

This deployment does not require any virtual machines to be administrated. All
underlying infrastructure is managed automatically.

[![Deploy Button](https://raw.githubusercontent.com/specialised-systems/azure-templates/master/images/deploy-to-azure-button.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fspecialised-systems%2Fazure-templates%2Fmaster%2Ftemplates%2Fsonarqube%2Fdeploy.json)
