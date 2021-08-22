# Overview:
**What are EBS Snapshots**   
To backup the EBS volumes, that can be used for many reasons/scenario’s such as – Disaster recovery,  provide HA, data migration, other compliances. 

**Important to remember:**   
- Snapshot are incremental in nature & hence grow overtime.
- Snapshot pricing is identical for all EBS volume types.
- Encrypted volumes don’t offer incremental backups (so full backup every time)- Snapshots are retained until you erase them
- Extra cost if cross-region data transfers for snapshots.

**What is billable:** ( Cost component: Storage cost + data transfer )   
- Data transfer to S3 ($0.02 per GB) - cheapest in Virginia region   
- Storage Costs ($0.05 per GB-month)   
- Indirectly charged for KMS key. (AWS default keys are free, customer managed key are charged $1/key)   

**Most common opportunities to reduce the waste**
- Delete un-needed snapshots.

**AWS provided tools / services**


**Solution to reduce the cost**
- Delete un-needed snapshots.
- Use lifecycle polices to automate the deletion of snapshots.

