# Issues that you might encounter while creating Delta Live Tables (DLT) in Azure Databricks.
### 1. Delta Live Tables tab may not be visible under Workflows tab.
![](./images/azure-databricks-standard-tier.png)
![](./images/azure-databricks-premium-tier.jpg)
DLT is available only in Premium Pricing Tier, it is not available in Standard Pricing Tier
![](./images/azure-create-databricks-ws-edited.jpg)

### 2. Azure Quota Exhaustion Issue
After clicking _Create_ in _Create Pipeline_ page, Waiting for resources step might throw an Azure error.
![](./images/azure-databricks-create-pipeline-01-edited.jpg)
![](./images/azure-databricks-error-01-edited.jpg)
In the _Logs_ tab, click on the line which is highlighted in red.
![](./images/azure-databricks-error-02.jpg)
![](./images/azure-databricks-error-03.jpg)
There is a panel on the right, scroll down till you reach the end. Click on _Logs_ button.
![](./images/azure-databricks-error-04-edited.jpg)
Hover on the red exclamation mark, you will get an explanation of the error. There is a link in the explanation, copy the link and paste into a new browser tab where your Azure portal is open.
![](./images/azure-databricks-error-05-edited.jpg)
If you are finding it difficult to copy the link in the above step, go to _Event Log_ page.
![](./images/azure-databricks-error-06.jpg)
Click the first line ‘TERMINATING’. The link can be copied from here as well.
![](./images/azure-databricks-error-07.jpg)
Copy the link and paste the link into the same browser where your Azure portal is open. Azure’s “Request quota increase” page will open up. Do as suggested there.
![](./images/azure-databricks-error-08-edited.jpg)
You might encounter similar Azure errors again for different Azure resources. Follow the same method as the previous one.

### 3. Databricks feature not supported error.
Some features like _Data quality check_ is available only in **Advanced** edition of Data Live Tables. This will throw an error.
![](./images/azure-databricks-error-09.jpg)
So change the edition accordingly from the Pipeline setting page.
![](./images/azure-databricks-error-10-edited.jpg)