## Talend Data Integration Documentation

In order to fulfil the data requirements from Our teachers, we have to integrated two datasets.

One of the dataset is found in Kaggle, which is **first dataset** [First Dataset](https://github.com/sokqi918/WQD7005_AA1/blob/main/Dataset/ecommerce.csv)

In order to match the dataset Dr. need, I have generated own dataset to merge with first dataset. The data was generated based on the customer behaviours and “PreferedOrderCat”, For example, “TotalSpent” and “Age” data have been generated based on “PreferedOrderCat”. Also, Column of “Membership” has been generated based on the column of “Tenure” in first dataset. The link of **second dataset** [Second Dataset](https://github.com/sokqi918/WQD7005_AA1/blob/main/Dataset/lastpurchasedateorder.csv)

### Talend Data Integration

After that, I use Talend Data Integration to map the first and second dataset together. Below is the pipeline to map both datasets. “CustomerID” has been used to map these both datasets together.

**Pipeline in Talend Data Integration**

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Integration/pipelinedataintegration.jpg)

Firstly, drag the component of "tFileInputDelimited" into Job for first and second datasets.

The configurations for each datasets are showed as below:

**1. Configuration in First Dataset**

Configuration for first dataset:
![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Integration/file1configuration.jpg)

Edit Schema:
![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Integration/file1editschema.jpg)

**2. Configuration in Second Dataset**

Configuration for second dataset:
![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Integration/file2configuration.jpg)

Edit Schema:
![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Integration/file2editschema.jpg)

Next, we drag the component "tMap" to map both datasets.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Integration/mapping.jpg)

Finally, we save the output into our local computer.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Integration/output.jpg)


