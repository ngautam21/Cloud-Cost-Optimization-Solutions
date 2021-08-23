# Overview:   
**What is Athena**   
Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless solution to queries, and you pay only for the queries that you run.   

**Important to remember**   
- Result is stored in S3.   
- Cancelled queries are charged on data scanned.   
- No charges for running DDL’s.   

**Billable components in Athena:**   
- Number of bytes scanned. (Rounded up to nearest MB, with 10MB minimum per query).   
- Query results are stored in an S3 bucket that is billed at standard Amazon S3 rates.   
- Additional cost - usage of   
    - S3 (storage, requests, and inter-region data transfer)   
    - Glue (charged standard AWS Glue Data Catalog rates)   
    - Lambda (charged based on the number of requests for your functions and the duration, the time it takes for your code to execute)   

**AWS provided tools / services**   
- Cloudwatch.   
    - Metrics – EngineExecutionTime, ProcessedBytes, TotalExecutionTime etc.   
- AWS SDK or api’s   

**Solution to reduce the cost**
- Use data compression example GZIP, snappy, bzip2 etc.   
- Use columnar data format like Parquet, ORC (depending on need)   
- Organize dataset by using partition & bucketing    
- Optimize file size ( merge many small files in bigger files)   
- Write efficient queries.   