# EBS volume

### EBS stands for Elastic Block Store

(AWS source page)[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes.html]

### Why use EBS volumes

- Data availability 
    - EBS volumes are replicated at creation to avoid data loss in case of failure. You can attach one EBS volume to multiple EC2 instances and vice versa, multiple EBS volumes can be attached to one EC2 instance. 
    
- Data Persistance 
    - EBS volume is used because EC2 instance might not be persistant and sometimes it might crash. In that situation the data will be lost on that instance. However, if you have backed up the data in an EBS instance attached to that EC2 instance. Then, the data in that EBS volume will be intact (Assuming that DeleteonTermination option is disabled)
    
- Snapshots 
    - Snapshots of the EBS volume can be taken for bakup and to create new EBS volume in different AZ
    - Snapshots cost you money but the first time you take snapshot of a EBS volume then it is big. The later snapshots just include the changes made to the volume since the last snapshot was taken. Therefore, they might cost way less than the first snapshot
    - From AWS site (Even though snapshots are saved incrementally, the snapshot deletion process is designed so that you need to retain only the most recent snapshot) How???
  
- Encryption
  - EBS volumes can be encrypted. Snapshot of encrypted volume is also encrypted
 
