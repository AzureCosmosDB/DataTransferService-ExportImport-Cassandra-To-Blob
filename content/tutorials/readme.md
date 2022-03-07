# Azure CosmosDB Data Transfer Service Private Preview Tutorials 

### **Enable Managed Idendtity between Azure CosmosDB Account and Azure Storage Account**

- Data transfer uses Managed Identity to access Azure storage account. This is required for Enteprise security and to avoid keys. You may [refer to this notebook](tutorials/managed-identity.ipynb) to complete this setup.

### **Provision a Data Transfer Service Cluster**

- Please [provision the service](tutorials/provision-data-transfer-service.ipynb) before running export and import jobs. Data transfer service uses this cluster to perform the export and import jobs.

### **Export/Import data between Azure CosmosDB Cassandra Account and Azure Storage**

- [Use this notebook](tutorials/export-import-sample.ipynb) for sample commands to run export/import jobs.
