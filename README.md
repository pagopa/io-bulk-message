# io-bulk-message

## How to send message to IO users

1. create a message in **templates** folder
2. in azure portal go to **[iopstexportdata](https://portal.azure.com/#@pagopait.onmicrosoft.com/resource/subscriptions/ec285037-c673-4f58-b594-d7c480da4e8b/resourceGroups/io-p-rg-operations/providers/Microsoft.Storage/storageAccounts/iopstexportdata/overview)** (storage account)
3. upload fiscalcode csv into **input** container (es. beta_testers.csv)
4. go to **[Azure DevOps](https://dev.azure.com/pagopaspa/io-bulk-message/_build?definitionId=531)** and click **run pipeline**
5. insert required params and click run
7. go to **[io-p-lapp-send-message](https://portal.azure.com/#@pagopait.onmicrosoft.com/resource/subscriptions/ec285037-c673-4f58-b594-d7c480da4e8b/resourceGroups/io-p-rg-operations/providers/Microsoft.Web/sites/io-p-lapp-common/workflowsList)** (logic app)
8. monitor running logic apps
9. when all jobs finished you can download log files into **[iopstexportdata](https://portal.azure.com/#@pagopait.onmicrosoft.com/resource/subscriptions/ec285037-c673-4f58-b594-d7c480da4e8b/resourceGroups/io-p-rg-operations/providers/Microsoft.Storage/storageAccounts/iopstexportdata/overview)** **dfout/bulk-message** container
