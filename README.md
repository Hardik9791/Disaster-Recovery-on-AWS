# Disaster-Recovery-on-AWS


## Backup and Disaster Recovery Project on AWS

## Project Overview
In this project, I implemented a comprehensive backup and disaster recovery solution using AWS services, including EC2, RDS, and S3. The project aimed to demonstrate the ability to create, manage, and restore backups in a cloud environment, ensuring data availability and resilience.

## Objectives
•	To set up AWS resources (EC2, RDS, S3) for backup.
•	To configure automated backups using AWS Backup.
•	To simulate a disaster scenario and restore the resources from backups.

## Architecture
<img width="303" alt="image" src="https://github.com/user-attachments/assets/fa9f691e-8444-45fe-ae6f-c05880da0901" />

 
## Step-by-Step Implementation

## Step 1: Set Up AWS Resources
1.	EC2 Instance:
•	Created an EC2 instance named backup-recovery-project using Amazon Linux.

  <img width="394" alt="image" src="https://github.com/user-attachments/assets/14d23e09-7bfa-499b-8491-d175d8d39f4a" /> <br>
  
  <img width="449" alt="image" src="https://github.com/user-attachments/assets/46f14f42-0024-4832-b8a7-2fa1276d0bab" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/640acfe7-cc79-4d97-87f8-5f1c0ead8903" /> <br>

 

•	Connected my EC2 instance using SSH and installed a basic application, “Apache” to simulate real-world usage.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/8b999ac7-2525-417a-b0c4-1bcc3a723c36" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/b993e2b9-175e-4ad7-98c3-08b944e09880" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/54c3eb7e-46d7-4320-be85-0c01381af039" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/4b42146c-6fec-4e1c-98d4-e3c4f73daa8a" /> <br>




 

 

 

•	Modified the application by implementing a simple HTML file.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/1a7597d0-fb51-4444-aeca-c7d9951c4270" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/449e92c9-8d23-4ca0-ade9-bddba8a90ba7" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/f3b9ecd5-f9f4-449e-a97d-dd9603cb164a" /> <br>



 

 

2.	RDS Database:
•	Launched an RDS instance named backup-recovery-db using MySQL as the database engine.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/b431b7ff-7e5f-4c3c-8885-8c771b703870" /> <br>
  
  <img width="418" alt="image" src="https://github.com/user-attachments/assets/c12a121a-7399-4669-bc09-24ad52f76271" /> <br>
  
  <img width="417" alt="image" src="https://github.com/user-attachments/assets/59925548-7f03-48ee-b376-8cc35aebc000" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/925b0904-b7d8-4346-ad8f-a25d93fdc69b" /> <br>





 
 

 

•	Tested RDS database Connection using MySQL Workbench.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/1aed8bf1-51d5-4467-9720-8927fb7b6328" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/3824359b-7d1c-4fd2-8572-61a9dcb5be15" /> <br>



 
3.	S3 Bucket:
•	Created an S3 bucket named backup-recovery-buck and uploaded sample image file.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/9481f4b5-4704-4f08-91db-110b8265ed7f" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/c655ba7c-e70a-4e76-9d5f-6460e263d8aa" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/88b61f92-2dd1-4d50-a409-a98cfbfee65d" /> <br>


 
 

•	Enabled bucket versioning to ensure backup file’s version. 

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/d6885780-b054-4643-89ee-508c291cfb1d" /> <br>








## Step 2: Configure AWS Backup
•	Navigated to the AWS Backup service and created a new backup plan named backup-recovery-plan with daily backup rules and 2-hour lifecycle.

  <img width="439" alt="image" src="https://github.com/user-attachments/assets/6ffce929-ed6e-4c3d-bd9a-3030687eff7b" /> <br>
  
  <img width="388" alt="image" src="https://github.com/user-attachments/assets/6bf14fbf-d86a-44eb-a946-eda2ca892c3d" /> <br>


 
•	Assigned the EC2 instance, RDS database, and S3 bucket to the backup plan.

  <img width="344" alt="image" src="https://github.com/user-attachments/assets/e64f7dad-c8bb-4b1e-b1e0-e0bfafb68f83" /> <br>
  
  <img width="345" alt="image" src="https://github.com/user-attachments/assets/38193337-c4aa-477f-9687-d7b670df4986" /> <br>


 
## Step 3: Test and Verify Backups
•	Checked the status of backup jobs in the AWS Backup dashboard. 

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/13cd0757-a1bb-4c13-8172-7ba05f10f774" /> <br>


 

•	Verified that backups were successfully created for all resources.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/d2184914-a87e-40db-9bd4-db1dfb855250" /> <br>





## Step 4: Simulate a Disaster
•	Terminated the EC2 instance.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/2ca8163b-1dc3-4399-8234-89ae2e116ddb" /> <br>

•	Deleted the RDS instance.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/fc9f69fb-432c-4976-b680-3499cebc8889" /> <br>

•	Removed uploaded files from the S3 bucket.

  <img width="334" alt="image" src="https://github.com/user-attachments/assets/a52efa9d-2f5c-4f8b-8555-e633cfd9facb" /> <br>

## Step 5: Restore from Backup
•	Restored the EC2 instance from the AWS Backup dashboard.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/340fb029-27ca-448b-b7d1-f4c945168d13" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/a73b50d4-10e3-4118-baea-61d5dd7f6ab0" /> <br>

 

•	Restored files back to the S3 bucket.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/6ff58ef7-8df2-425a-8411-b7f6e352665a" /> <br>
  
  <img width="449" alt="image" src="https://github.com/user-attachments/assets/fb1e033e-e927-4bd7-8019-2322e29595a8" /> <br>

 
•	Recreated the RDS instance from the backup.

  <img width="449" alt="image" src="https://github.com/user-attachments/assets/924e523b-c736-45f3-97d7-908889ba8237" /> <br>
  
  <img width="449" alt="image" src="https://github.com/user-attachments/assets/228aa29b-bd33-4e9d-bf0a-aa8b871312ff" /> <br>

 
## Step 6: Test the Restored Resources
•	Connected to the restored EC2 instance and verified that the application was running.

  <img width="470" alt="image" src="https://github.com/user-attachments/assets/5decaa84-b84b-4d4e-9786-9153f7af5f83" /> <br>
  
  <img width="470" alt="image" src="https://github.com/user-attachments/assets/6fbf06ac-478e-4bdd-b5fb-b20198a8c9b8" /> <br>

 


•	Checked the S3 bucket to confirm that file was restored.

  <img width="445" alt="image" src="https://github.com/user-attachments/assets/c505d6eb-aa55-48a3-a15e-1b95aa4e9a44" /> <br>


•	Accessed the restored RDS database to ensure data integrity.

  <img width="445" alt="image" src="https://github.com/user-attachments/assets/1b3915b9-0b70-4e69-96fe-d0c08a73cac6" /> <br>

## Technologies Used
•	Amazon EC2: Virtual servers in the cloud for hosting applications.
•	Amazon RDS: Managed relational database service.
•	Amazon S3: Object storage service for data backup.
•	AWS Backup: Service to automate and centralize backup processes.

## Conclusion
This project successfully demonstrated the implementation of a backup and disaster recovery strategy using AWS. By automating backups with AWS Backup, I ensured data availability and resilience against potential failures.

## Future Enhancements
•	Implementing additional backup strategies, such as cross-region backups.
•	Exploring more advanced recovery options, such as point-in-time recovery for RDS.
•	Automating disaster recovery drills to validate backup and restore processes regularly.


