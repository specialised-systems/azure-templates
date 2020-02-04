# New Virtual Network Peered to an Existing Virtual Network

Deploy a new virtual network and peer it with an existing one. This allows
substantial isolation in exchange for a nominal transfer fee (cents/Gb) for
data moving between peered networks.

[![Deploy Button](https://raw.githubusercontent.com/specialised-systems/azure-templates/master/images/deploy-to-azure-button.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fspecialised-systems%2Fazure-templates%2Fmaster%2Ftemplates%2Fpeered-vnet%2Fdeploy.json)

## Prerequisites

For peering to work, a peering link must also be created from the existing
virtual network to the virtual network created by this template.
