# Overview:
**What is EMR**   
EMR a.k.a - Amazon Elastic MapReduce (EMR) is a web service that makes it easy to quickly and cost-effectively process vast amounts of data.   
Amazon EMR uses Hadoop, an open source framework, to distribute your data and processing across a resizable cluster of Amazon EC2 instances. Amazon EMR is used in a variety of applications, including log analysis, web indexing, data warehousing, machine learning, financial analysis, scientific simulation, and bioinformatics. Customers launch millions of Amazon EMR clusters every year.   

EMR can be launched on   
- ec2   
- EKS   
- AWS outposts   

**Billable components** (Billed per-second with a one-minute minimum )   
EMR can be launched on ec2.   
- ec2 instance type attached to the cluster.   
- EMR price (license cost).   
- EBS volumes.   

**Options to reduce EMR cost**   
- Use right type of instance types for the job. (r5- memory intensive).   
- Leverage newer version of EMR.   
- Leverage managed scaling instead of auto scaling.   
- Use a mix of SPOT and On-Demand instances for compute.   
- Multi-tenant cluster instead of dedicated clusters.   
- Optimize usage of all underneath resaources such as DynamoDB, RDS, Glue etc.   
- Review performance configurations parameters over a period of time.   
- Use ephemeral model.   

**AWS provided tools / services**
- AWS cloudwatch.   
- EMR Ganglia.   
- Build your own custom solutions.   