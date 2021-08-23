# Overview:   
**What is S3**   
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.   

**Types of Storage class:**   
- S3 Standard - general-purpose storage of frequently accessed data.   
- S3 Intelligent tiering - for data with unknown or changing access patterns.   
- S3 Standard Infrequent Access -  for long-lived, but less frequently accessed data.   
- S3 Standard one zone Infrequent Access -  for long-lived, but less frequently accessed data.   
- S3 Glacier - for long-term archive and digital preservation.   
- S3 Glacier deep Archive - for long-term archive and digital preservation.   
- S3 outposts   

**Cost components (Pay only for what you use)**   
- Storage pricing   
    - You pay for storing objects in S3 buckets. The rate you’re charged depends on your objects' size, how long you stored the objects during the month, and the storage class.   
- Requests & data retrieval pricing   
    - You pay for requests made against your S3 buckets and objects. S3 request costs are based on the request type, and are charged on the quantity of requests   
- Data transfer and transfer acceleration pricing   
    - You pay for all bandwidth into and out of Amazon S3 with few exceptions. (Refer AWS documentation. https://aws.amazon.com/s3/pricing/)   
- Data management and analytics pricing.   
    - You pay for the storage management features and analytics (Amazon S3 Inventory, S3 Storage Class Analysis, S3 Storage Lens, and S3 Object Tagging) that are enabled on your account’s buckets.   
- Replication   
    - For S3 Replication (Cross-Region Replication and Same Region Replication), you pay the S3 charges for storage in the selected destination S3 storage classes, the storage charges for the primary copy, replication PUT requests, and applicable infrequent access storage retrieval fees.   
- S3 Object Lambda pricing   
    - With S3 Object Lambda you can add your own code to S3 GET requests to modify and process data as it is returned to an application.   

**Most common opportunities/actions to reduce the waste.**   
- Identify & understand large buckets that you aren’t aware of.      
- Find and eliminate incomplete multipart upload bytes.   
- Depending on usage pattern increase use of storage classes.      
- Reduce the number of noncurrent versions retained.   
- Uncover buckets that have gone cold & take action.    
- Automatically transition your data using S3 Lifecycle policies.    
- Enable auto-archiving with S3 Intelligent-Tiering.   

**AWS provided tools / services.**   
- S3 Storage Lens dashboard.   
- Cloudwatch   