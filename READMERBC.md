#Deployment Steps
1. Ensure Azure Key Vault has been created (The storage account going to be created and the key vault must be in the same region, but they can be in different subscriptions.)
2. Ensure at least one Key in the Azure Key Vault has been created, and the three arguments below are recorded:
-Key Name
-Key Version
-Key Vault URI
3. Ensure that a Azure service principle has been created for the python script, and the three arguments below are recorded:
-Tenant ID for your Azure Subscription
-Your Service Principal App ID
-Your Service Principal Password
4. The scripts takes X input arguments:
-storageAccountName
