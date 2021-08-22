This project provides best practices and automation for cloud cost management and optimization. There are several advantages of building in cloud but it can quickly add up in expense when it is not actively managed. There are many simple steps to manage cloud cost, with automation it can prevent unanticipated expense spikes and major cost optimization efforts.  

**Schedulers**   
- Manage cost   
- Manage over provisioned resources using the following schedulers:     
    - EC2 Scheduler - Start/Stop EC2 instances based on a schedule.   
    - Auto Scaling Scheduler - Add/Update a Schedule Scaling Policy.   
    - DynamoDB Scheduler - Add/Update Application Autoscaling policy on DynamoDB tables & indexes.      
    - RDS Scheduler - Starts and Stops Relational database instances /clusters based on a schedule.      
    - EBS Scheduler - Delete unattached volumes.   

**Tagging resources – easy management**      
- Charge back model   
- Reporting      
- Integrate devops/procurement/cloud engineering team etc.   

**Dashboards**   
- Single place to visualize in a multi cloud environment.   
- Use to identify the loose ends in your environment.   

**KPI’s**   
- Compare over a period of time?   

**Save “O” meter**   
- Leverage statistics to determine the cost savings OR saving opportunities.   
- Should crawl to the selected services, see the statistics and determine the cost.   
    - Example:    
        - Last 7 days - ec2 – CPU/Memory/Network in use 20%   
        - Last 7 days – No change in Terabytes of objects in S3.      
- Cloud agnostic.   
- Saving meter show savings in `$`.   
