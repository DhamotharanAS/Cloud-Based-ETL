# Cloud-Based-ETL

Hi all!

Step 1: I have created an AWS RDS database. The engine that I have used is MySQL.
Step 2: After creating the MySQL I have connected the RDs to the MySQL Workbench using the hostname, username, and password.
Step 3: Next, I have created a database on the MySQL Workbench.
Step 4: After that, I exported all the tables by using the RDS snapshots method.
Step 5: Then I imported the tables into the S3 bucket.
Step 6: By using AWS Glue, I have created a database and crawled all the data by using the Data Catalog.
Step 7: Change the CSV format to Parquet format using AWS Glue Job
Step 8: Then upload that data in the S3.
Step 9: After that, create another database, crawl the parquet format, and store it in the database catalog.
Step 10: Transformation takes place here. I have used Split, Joins, Concat, and Data Format Change.
Step 11: After the glue, the job succeeds. The data's stored in the S3 bucket.
Step 12: If the glue job is successful, I will receive the email I have integrated by using AWS glue and AWS SNS.

So overall, all the processes are automated only if I first upload the data to S3. It will trigger the AWS Lambda Code, and it will
trigger the AWs Glue Data catalog so the CSv is transformed into parquet. After the change in the parquet format, data's are uploaded.
in the S3 bucket. So if it is uploaded, then the other Lambda function will get triggered. So the transformation is done. And the glue job is successful.
I will get notified in the mail.
