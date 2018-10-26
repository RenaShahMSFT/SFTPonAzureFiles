# SFTPonAzureFiles
# Create an SFTP Server with Azure Files and Container

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F101-azure-database-migration-service%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F101-azure-database-migration-service%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.png"/>
</a>

For more details about the service please follow the link https://azure.microsoft.com/en-us/services/database-migration/

The above template will deploy a resource group with the below resources in your subscription.
-	Deploy this template
o	Takes password and storage account prefix as parameters
o	It creates a storage account and a file share via a linked template 
-	Once finished, the template will output the public IP address for the SFTP container
-	Connect using sftp ftp@<public-ip>
o	SFTP is included in OpenSSH for PowerShell 😊
-	Change directory to “upload”
-	Upload a file using “put <local file name>”
-	Confirm that the file has been uploaded into the file share by looking in the Portal


Using the above resources you can connect to source and target servers select the databases to migrate and run an end-to-end migration.
