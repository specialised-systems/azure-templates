{
    "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json",
    "contentVersion": "0.0.1.1",
    "parameters": {
        "imageName": {
            "type": "String",
            "minLength": 1
        },
        "osType": {
            "type": "String",
            "minLength": 1,
            "defaultValue": "Windows"
        },
        "imageUri": {
            "minLength": 1,
            "type": "String"
        },
        "location": {
            "defaultValue": "[resourceGroup().location]",
            "type": "String"
        }
    },
    "resources": [
        {
            "type": "Microsoft.Compute/images",
            "apiVersion": "2016-04-30-preview",
            "name": "[parameters('imageName')]",
            "location": "[parameters('location')]",
            "properties": {
                "storageProfile": {
                    "osDisk": {
                    "osType": "[parameters('osType')]",
                    "osState": "Generalized",
                    "blobUri": "[parameters('imageUri')]",
                    "storageAccountType": "Premium_LRS"
                    }
                }
            }
        }
    ]
}
