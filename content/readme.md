# Azure CosmosDB Data Transfer Service Private Preview Tutorials

This book contains tutorials that demonstrate how to use data transfer service (DTS) to export and import data from Azure CosmosDB Cassandra API to Azure Storage using Managed Identity.

## **Prerequisites**

To start tutorials, you would need to have an Azure Subscription with 'Data Transfer Capability' enabled.
If you don't have the capability enabled, please [sign-up here](https://forms.office.com/r/Hv0pwdn3iz).
You may contact shwetn@microsoft.com and flnarenj@microsoft.com for any additional queries or assistance.

Note: There is a charge associated with this service and shows up on your invoice as 'Cluster compute'.

If you don't have an Azure subscription, create a <a href="https://azure.microsoft.com/free/?WT.mc_id=A261C142F" data-linktype="external">free account</a> before you begin.</p>

### **Tools**

- <a href="https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15" data-linktype="external"> Azure Studio </a> (Note: Samples use Powershell and Python 3 kernels, please ensure these kernel dependencies are installed before running the samples)

### **Azure Resources**

- Azure CosmosDB Cassandra API Account, if you don't have one <a href="https://docs.microsoft.com/en-us/azure/cosmos-db/free-tier" data-linktype="external"> Create a free account </a>

- Azure Storage Account, if you don't have one <a href="https://docs.microsoft.com/en-us/azure/storage/common/storage-account-create?tabs=azure-portal" data-linktype="external"> click here </a>

- Azure Cosmos DB Cassandra API Table, if you don't have one, please use this notebook to setup [sample data](tutorials/cassandra-sample-data-setup.ipynb)

### **Enable Managed Idendtity between Azure CosmosDB Account and Azure Storage Account**

- Data transfer uses Managed Identity to access Azure storage account. This is required for Enteprise security and to avoid keys. You may [refer to this notebook](tutorials/managed-identity.ipynb) to complete this setup.

### **Provision a Data Transfer Service Cluster**

- Please [provision the service](tutorials/provision-data-transfer-service.ipynb) before running export and import jobs. Data transfer service uses this cluster to perform the export and import jobs.

### **Export/Import data between Azure CosmosDB Cassandra Account and Azure Storage**

- [Use this notebook](tutorials/export-import-sample.ipynb) for sample commands to run export/import jobs.

### **Use cases**

- Long term retention of data into blob storage in Avro format for auditing & compliance purposes.
- Migrate table from shared throughput to dedicated throughput vice versa.
- Change partition key (Note: Schema of the Source and Destination must be same).
- Migrate table with more RUs to lesser RUs to reduce foot print underneath it.
