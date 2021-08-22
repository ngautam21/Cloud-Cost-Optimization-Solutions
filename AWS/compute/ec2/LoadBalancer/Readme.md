# Overview:
**What are ELB’s**   
- ELB is a AWS service to distribute the workload across registered targets. Can be use for multiple reasons most common - provide high availability, scalability, security.   

**Important to remember:**   
- Any created load balancer accrued charges.   
- Any Idle load balancer costs $18 per month.   

**Cost component**   
- Each hour/partial hour (Partial hours are billed as full hours) that a Load Balancer is running.   
- Each GB of data transferred through your load balancer.   
    - Classic LB:   
        - $0.025 per Classic Load Balancer-hour (or partial hour)   
        - $0.008 per GB of data processed by a Classic Load Balancer   
    - Application LB:   
        - $0.0225 per Application Load Balancer-hour (or partial hour)   
        - $0.008 per LCU-hour (or partial hour)   
    - Network LB:   
        - $0.0225 per Network Load Balancer-hour (or partial hour)   
        - $0.006 per NLCU-hour (or partial hour)   

**Most common opportunities to reduce the waste**   
- A load balancer has no active back-end instances.   
    - Consider registering instances OR deleting your load balancer.   
- A load balancer has no healthy back-end instances.   
    - Troubleshoot OR delete the ELB.   
- A load balancer has had less than 100 requests per day for the last 7 days.   
    - Consider deleting your load balancer, probably its not in use.   
- Migrate to ALB from ELB (If possible).   
    - In typical world 1 ELB per application, so more application more ELB.   
    - By ALB - content based routing feature can achieve the same feature by using multiple ELB’s.   

**AWS provided tools / services**   
- AWS SDK or api’s   
- Cloudwatch metrics   