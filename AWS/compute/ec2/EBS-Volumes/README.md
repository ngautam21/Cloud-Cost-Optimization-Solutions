# Overview:
**What are EBS Volumes**   
EBS volumes are easy to use, high performance block level storage service designed to work with EC2 to run any type of workload.    
**Type of EBS:**   
- General Purpose SSD (gp2)/  General Purpose SSD (gp3).   
    - Use case: General purpose solid state disk, can be use for OLTP application, Streaming, Ware housing applications.   
- Provisioned IOPS SSD (io1)/ Provisioned IOPS SSD (io2)   
- High performance SSDs: (Speeds up to 1024 MB/s + cost => 25% increase from gp2 )   
     - Use case: IOPS-intensive and throughput-intensive workloads that require extremely low latency   
- Cold HDD (sc1)   
    - Use case: defines performance in terms of throughput rather than IOPS. Good fit for large, sequential cold-data workloads.   
- Throughput Optimized HDD (st1):   
    - Use case: Designed for frequently-accessed, throughput-intensive workloads, and is suitable for development and testing environments.   
- Magnetic (standard):   	
    - Use case: Workloads with smaller datasets where data is accessed infrequently or when performance consistency isn't of primary importance.   

**Cost component: Storage cost + data transfer**    
- Data transfer to S3 ($0.02 per GB) - cheapest in Virginia region   
- Storage Costs ($0.05 per GB-month)   
- Indirectly charged for KMS key. (AWS default keys are free, customer managed key are charged $1/key)   

**Most common opportunities to reduce the waste.**
- Depending on the workload migrate to the volume that makes more sense. may be smaller in size or volume type like gp2 to gp3 etc.   
- Use io1/2 only where they are absolutely needed. as they are the costliest volumes.   
- Underused volume groups: Charges begin when a volume is created. If a volume remains unattached or has very low write activity (excluding boot volumes) for a period of time, the volume is probably not being used.  

**AWS provided tools / services.**   
- AWS SDK or api’s   
- Cloudwatch metrics:   
    - VolumeQueueLength metrics:  shows how many pending operations the volume is waiting to fulfill. If this graph is spiking up, you’re likely maxing out your EBS volume, and should consider upgrading to provisioned IOPS storage.   
    - EC2’s IOWait: Which measures how many CPU cycles are spent waiting for read or write operations.   

**Solution to reduce the cost**   
- Creating a snapshot and deleting the volume to reduce costs.   
- Verify under/over provision volumes.   