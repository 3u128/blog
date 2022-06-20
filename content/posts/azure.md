---
title: "azure login and tips"
date: 2022-06-16
draft: false
description: ""
---
azure-cli packet install by packet manager in OS or ```pip3 install--user azure-cli```

```
az command --help <- help by command without search in web documentation
az interactive <- interesting way to understand azure with cool feature autocmoplite

az login The following tenants don't contain accessible subscriptions. Use 'az login --allow-no-subscriptions' to have tenant level access.
b41b72d0-4e9f-4c26-8a69-f949f367c91d 'EPAM'
[
  {
    "cloudName": "AzureCloud",
    ...
    ...
    ...
    }
  }
]
```

For use secret for auth in 3rd tools like terraform:
```https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/guides/service_principal_client_secret```

```
$ az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/SUBSCRIPTION(it means - id (can see in az login output))"
This command or command group has been migrated to Microsoft Graph API. Please carefully review all breaking changes introduced during this migration: https://docs.microsoft.com/cli/azure/microsoft-graph-migration
Creating 'Contributor' role assignment under scope '/subscriptions/7ecf38d4-b00e-4aff-ab84-dbb0f4883c0a'
The output includes credentials that you must protect. Be sure that you do not include these credentials in your code or check the credentials into your source control. For more information, see https://aka.ms/azadsp-cli
{
  "appId": "",
  "displayName": "",
  "password": "",
  "tenant": ""
}
```
