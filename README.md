# Specialised Systems' Azure Templates

The [Azure Quickstart Templates](https://github.com/Azure/azure-quickstart-templates)
provide a starting point for deploying software into Azure. However, for our
purposes, they have 3 key shortcomings:

  1. There focus on quantity over quality.
  2. They don't follow common behaviours.
  3. They are poorly documented and often outdated.

While they suffice for 'getting started', they did not provide us with what we
needed to provide production-quality deployments for our customers.

This Azure templates in this repository:

  1. focus on quality over quantity;
  2. apply informed standards and practices;
  3. are extensively documented.

These templates are written to satisfy the needs of our customers, and may not
be suitable for others. Nonetheless, we welcome pull requests and encourage
others to try our templates.

## Usage

Fork this repository and then add your own customisations over the top. To
update your fork, merge from this (upstream) repository and upgrade to our most
recent templates.

## Standards and Practices

One of the stated aims of this repository is to apply informed standards and
practices. This helps to ensure the templates provided here are easy to read,
update, and adapt to satisfy new requirements. These standards and practices
are outlined below.

### Atomiticity

Templates are written with the goal of providing a single, well-defined piece
of functionality. Complex deployments are performed by applying templates in
sequence.

### Directory Structure

Templates are organised into directories in the `/templates` directory. Each
directory in `/templates` contains a single template, and every template has:

* a `README.md`, which describes the template; and
* a `deploy.json`, which is the root file of the deployment.

Common images used throughout documentation are stored in the `/images`.

### Parameters

All parameters names follow the `camelCase` convention. Wherever possible,
parameters should have reasonable default values. These default values must
ensure that, when executed, the template produce resources that follow other
standards and practices.

### API Versions

The latest API versions should always be used. The following commands shows how
to retrieve the API versions for various resource types.

```PowerShell
(Get-AzureRmResourceProvider -ProviderNamespace Microsoft.Insights).ResourceTypes | Where {$_.ResourceTypeName -eq 'components'} | Select -ExpandProperty ApiVersions
(Get-AzureRmResourceProvider -ProviderNamespace Microsoft.SQL).ResourceTypes | Where {$_.ResourceTypeName -eq 'servers/databases'} | Select -ExpandProperty ApiVersions
```

When executed, these commands will provide the API versions for a resource
type. By changing the resource type, this command can provide the API versions
for any resource type.

## References

  1. [Create Resource Manager parameter file](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/parameter-files) (Accessed January 12th)
  2. [Standardising Azure Resource Naming Conventions Using ARM Templates](https://adatis.co.uk/standardising-azure-resource-naming-conventions-using-arm-templates/) (Accessed January 12th)
