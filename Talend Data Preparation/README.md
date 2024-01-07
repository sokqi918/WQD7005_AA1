## Talend Data Preparation Documentation

Talend Data Preparation is a tool for data cleansing and data profiling. Below are the steps to data cleaning and data transformation.

**1. Missing value has been checked using Talend Data Preparation. After checked, we found out that the below columns have missing value. Handling missing value will be done in SAS Enterprise Miner.**

| Columns                     | Missing Values (count) |
|-----------------------------|-------------------------|
| Tenure                      | 264                     |
| WarehouseToHome             | 251                     |
| HourSpendOnApp              | 255                     |
| OrderAmountHikeFromlastYear | 265                     |
| CouponUsed                  | 256                     |
| OrderCount                  | 258                     |
| DaySinceLastOrder           | (No count as deleted)   |
| Membership                  | 264                     |

**2. Data type has been changed in Talend Data Prep if those data type is wrong. In this case, “CustomerID” column data type has been changed from fr_postal_code to TEXT. (HANDLE INCONSISTENT DATA TYPE)**

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/datatype.jpg)

**3. Inconsistent value in columns.**

Inconsistent data in “PreferredPaymentMode”.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/replacecc.jpg)

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/replaceCOD.jpg)

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/payment.jpg)

Inconsistent data in “PreferedOrderCat”

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/replacemobile.jpg)

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/preferred.jpg)

**4. Since “DaySinceLastOrder” will not be used in analysis, hence I have dropped this column.**

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/drop.jpg)

**5. After all activities done, I have exported the preprocessed dataset on local computer for further analysis.**

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Talend%20Data%20Preparation/export.jpg)

In Talend Data Preparation, we are able to ensure data quality. It is a tool for us to prepare and clean data. It helps us to:

- Data profiling and cleansing: identify issues with their data, such as missing values, duplication, or inconsistencies.
- Identify inconsistencies such as “PreferredPaymentMode” and “PreferedOrderCat”.
- Data Validation: we can ensure incoming data meets specific requirements, before passing to SAS Enterprise Miner.

After the data preprocessing is completed, we can proceed further steps in SAS Enterprise Miner.
