# Design-a-Data-Warehouse-for-analysing-E-Commerce-customers-shopping-pattern
## Objective
1. To observe the purchase pattern of the customer according to their information such as gender, education and annual salary etc.
2. Discover the potential clients who could bring the max amount of sales and profits  
### Notice  
Spark can only be used to process distributed big data but not in saving them. Therefore, it requires to use Hadoop to save data in advance,
then parse them by interacting with Spark  
# Architecture
![image](https://user-images.githubusercontent.com/103509243/203409730-19cdd9a2-706b-444d-b94b-90680848ea41.png)


# Approach
## 1. Create EC2 instance on Amazon and Docker container
![image](https://user-images.githubusercontent.com/103509243/193682249-65be5c24-1313-488d-8b97-0523160244a2.png)
## 2. Add Postgresql jar and put hive-site.xml from hive to spark
Download and add Postgresql jar file
![image](https://user-images.githubusercontent.com/103509243/193688782-e8702a8e-e3b5-4ede-ae46-4ecb47189c2d.png)
![image](https://user-images.githubusercontent.com/103509243/193688812-049c012e-10a7-4f07-aa13-06628857f7d3.png)
![image](https://user-images.githubusercontent.com/103509243/193689459-068efba7-64d4-40df-ab0e-eca0b36bf650.png)  
Check the postgreSQL jar file has imported  
## 3. Create Tables of Customer’s Information in MySQL to store data
![image](https://user-images.githubusercontent.com/103509243/193690826-c64e6bc6-fb0e-4b07-893e-ff71b7677550.png)
## 4. Import data from MySQL to HDFS (Hadoop Distributed File System)
![image](https://user-images.githubusercontent.com/103509243/193691411-79b4cee5-6c98-40ed-8457-1a6d6b93faa3.png)
## 5. Load data into Apache Hive tables
![image](https://user-images.githubusercontent.com/103509243/203391086-805846f0-dcac-4d79-bd6d-568dd945ad3a.png)
## 6. Integrate Hive into Spark (Handle XML file & save in parquet format)
![image](https://user-images.githubusercontent.com/103509243/193694543-8cf42571-2e6f-4860-8425-fc9b09678fc1.png)
![image](https://user-images.githubusercontent.com/103509243/193695539-b59428fb-1138-45b8-ba98-081b252cb714.png)
![image](https://user-images.githubusercontent.com/103509243/203408724-b0d2eb0b-addb-438d-aba5-1bcc3ed97e9b.png)

## 7. Create Tables in Hive and load processed data into tables
![image](https://user-images.githubusercontent.com/103509243/193695991-ee34977a-823b-4989-ad2e-28e78275eca1.png)
![image](https://user-images.githubusercontent.com/103509243/203418598-fd313f2c-9bb7-4f7c-abc2-dfa2149e26b9.png)
![image](https://user-images.githubusercontent.com/103509243/193696590-d775bfdf-f5dc-4427-8e68-8bb466727aeb.png)
## 8. Perform analysis through Hive
![image](https://user-images.githubusercontent.com/103509243/193696991-bbd8710e-06bf-4428-ac39-6b4e7e96ccae.png)
![image](https://user-images.githubusercontent.com/103509243/193697037-7e555721-876c-4484-adbc-786477421fce.png)
![image](https://user-images.githubusercontent.com/103509243/193697080-497936ef-590d-4ce0-ba70-0caf29192831.png)
![image](https://user-images.githubusercontent.com/103509243/193697165-df2ef67c-68de-440c-b035-cdc70f76ea78.png)
![image](https://user-images.githubusercontent.com/103509243/193697298-b9ed4035-b45f-43ec-a1dc-f988418bca40.png)

