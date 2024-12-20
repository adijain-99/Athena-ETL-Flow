# Athena-ETL-Flow

## csv-glue crawler-s3 source bucket-amazon glue-s3 target bucket-athena query


- AWS offers serverless services which we are gonna use
- pay as you go method.
- we will place data in s3 bucket(source).
- with glue crawler i am gonna fetch the data to Amazon glue
- the through etl job i am gonna store the data in target bucket
- main engine of ETL  - glue
- then i am gonna query the information by using AWS athena
- athena is a query tool

## STEPS

- create 3 S3 buckets - source, target and results
- have to craete IAM role - I created role with GLUE usecase and I provided S3fullaccess and AWSGlueServiceRole
- You can also give administrator access as well, if you want
- why we need an IAM role? - Glue requires some permission to get/write or perform any ETL job so for that we need an IAM role.
- Now create the glue crawler - add the data source - select 'Crawl all sub folders'
- Select the appropriate IAM role
- Create target Database - necessary.
- Don't add any  tables in the DB.
- 
