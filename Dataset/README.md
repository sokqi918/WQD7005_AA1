## Dataset used in this project:

**First Dataset:** [ecommerce.csv](https://github.com/sokqi918/WQD7005_AA1/blob/main/Dataset/ecommerce.csv)

| Variable                  | Description                                       |
|---------------------------|---------------------------------------------------|
| CustomerID                | Unique customer ID                                |
| Churn                     | Churn Flag, 0: no churn, 1: churn                  |
| Tenure                    | Tenure of customer in organization                |
| PreferredLoginDevice      | Preferred login device of customer                |
| CityTier                  | City tier                                         |
| WarehouseToHome           | Distance in between warehouse to home of customer |
| PreferredPaymentMode      | Preferred payment method of customer              |
| Gender                    | Gender of customer                                |
| HourSpendOnApp            | Number of hours spend on mobile application or website |
| NumberOfDeviceRegistered  | Total number of devices registered on particular customer |
| PreferedOrderCat          | Preferred order category of customer in last month |
| SatisfactionScore         | Satisfactory score of customer on service          |
| MaritalStatus             | Marital status of customer                        |
| NumberOfAddress           | Total number of addresses added by a particular customer |
| Complain                  | Any complaint raised in the last month            |
| OrderAmountHikeFromLastYear| Percentage increase in order amount from last year |
| CouponUsed                | Total number of coupons used in the last month    |
| OrderCount                | Total number of orders placed in the last month   |
| DaySinceLastOrder         | Days since the last order by customer              |
| CashbackAmount            | Average cashback in the last month                |

**Second Dataset:** [lastpurchasedateorder.csv](https://github.com/sokqi918/WQD7005_AA1/blob/main/Dataset/lastpurchasedateorder.csv)

In order to match the dataset Dr. need, I have generated own dataset to merge with first dataset. The data was generated based on the customer behaviours and “PreferedOrderCat”, For example, “TotalSpent” and “Age” data have been generated based on “PreferedOrderCat”. Also, Column of “Membership” has been generated based on the column of “Tenure” in first dataset. Below are the descriptions of second dataset.

| Variable                | Description                                 |
|-------------------------|---------------------------------------------|
| CustomerID              | Unique customer ID                          |
| LastPurchaseOrderDate   | Last purchase order date                    |
| TotalSpent              | Total spent in this e-commerce              |
| Age                     | Customer age                                |
| Membership              | Level of membership: bronze, silver, gold & platinum |


**Output after integrated in Talend Data Integration:** [out.csv](https://github.com/sokqi918/WQD7005_AA1/blob/main/Dataset/out.csv)
This output has been saved after data integration with First and Second datasets in Talend Data Integration.

**Output after preprocessing in Talend Data Preparation:** [output_Preparation_v1.xlsx](https://github.com/sokqi918/WQD7005_AA1/blob/main/Dataset/output_Preparation_v1.xlsx)
