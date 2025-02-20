---
title: Azure CLI Script Example - Add an Application in Batch | Microsoft Docs
description: Learn how to add an application for use with an Azure Batch pool or a task using the Azure CLI.
ms.topic: sample
ms.date: 09/17/2021
ms.custom: devx-track-azurecli, seo-azure-cli
keywords: batch, azure cli samples, azure cli code samples, azure cli script samples
---

# CLI example: Add an application to an Azure Batch account

This script demonstrates how to add an application for use with an Azure Batch pool or task. To set up an application to add to your Batch account, package your executable, together with any dependencies, into a zip file. 

[!INCLUDE [azure-cli-prepare-your-environment.md](../../../includes/azure-cli-prepare-your-environment.md)]

 - This tutorial requires version 2.0.20 or later of the Azure CLI. If using Azure Cloud Shell, the latest version is already installed. 

## Example script

[!code-azurecli-interactive[main](../../../cli_scripts/batch/add-application/add-application.sh "Add Application")]

## Clean up deployment

Run the following command to remove the
resource group and all resources associated with it.

```azurecli-interactive
az group delete --name myResourceGroup
```

## Script explanation

This script uses the following commands.
Each command in the table links to command-specific documentation.

| Command | Notes |
|---|---|
| [az group create](/cli/azure/group#az-group-create) | Creates a resource group in which all resources are stored. |
| [az storage account create](/cli/azure/storage/account#az-storage-account-create) | Creates a storage account. |
| [az batch account create](/cli/azure/batch/account#az-batch-account-create) | Creates the Batch account. |
| [az batch account login](/cli/azure/batch/account#az-batch-account-login) | Authenticates against the specified Batch account for further CLI interaction.  |
| [az batch application create](/cli/azure/batch/application#az-batch-application-create) | Creates an application.  |
| [az batch application package create](/cli/azure/batch/application/package#az-batch-application-package-create) | Adds an application package to the specified application.  |
| [az batch application set](/cli/azure/batch/application#az-batch-application-set) | Updates properties of an application.  |
| [az group delete](/cli/azure/group#az-group-delete) | Deletes a resource group including all nested resources. |

## Next steps

For more information on the Azure CLI, see [Azure CLI documentation](/cli/azure).
