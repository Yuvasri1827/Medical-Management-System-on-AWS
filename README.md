# Medical-Management-System-on-AWS
“My project is a Medical Management System on AWS. The goal was to digitize hospital operations securely. Key features include patient records, appointment scheduling, billing, and role-based access. I used React on S3/CloudFront, API Gateway with Lambda, RDS for data, S3 for reports, and Cognito for authentication. 
To build a secure, cloud-based system that digitizes hospital operations (patient records, appointments, staff, billing) so that healthcare staff can manage everything from one place, reduce paperwork and manual errors, and access data anytime, with patient privacy protected.

One-line answer for interviews: “The goal was to replace manual hospital record-keeping with a secure, scalable, cloud-based system on AWS.”

Key Features
Module	What it does
Patient management	Registration, profile, medical history, search
Appointment scheduling	Book, reschedule, cancel; doctor availability; reminders
Electronic Health Records (EHR)	Diagnoses, prescriptions, lab reports, scans
Doctor and staff management	Profiles, schedules, departments
Billing and payments	Invoices, payment status, insurance details
Pharmacy/inventory	Medicine stock tracking, low-stock alerts
Role-based access	Admin, doctor, nurse, receptionist, patient each see only what they need
Notifications	Email/SMS appointment reminders
Reports and analytics	Daily patient count, revenue, department stats
Tech Stack

(Replace with what you actually used.)

Layer	Technology
Frontend	React / Angular, hosted on S3 + CloudFront
Backend	Node.js / Python / Java on Lambda or EC2
API	Amazon API Gateway (REST)
Database	Amazon RDS (PostgreSQL/MySQL)
File storage	Amazon S3 (encrypted)
Authentication	Amazon Cognito (with MFA)
Security	IAM, KMS, VPC, Security Groups, AWS WAF
Notifications	Amazon SNS / SES
Monitoring and logs	CloudWatch, CloudTrail
Deployment	CloudFormation / Terraform / CodePipeline
Challenges and Solutions
Challenge	How you solved it
Protecting sensitive patient data	Encryption at rest (KMS) and in transit (HTTPS/TLS), private subnets, least-privilege IAM
Controlling who sees what	Role-based access using Cognito groups and IAM policies
Data availability and downtime	Multi-AZ RDS, automated backups, S3 durability
Handling many users at once	Auto Scaling, load balancer, Lambda’s automatic scaling
Audit and compliance	CloudTrail and CloudWatch logs to track who accessed what; HIPAA-aware design
Large file storage (scans, reports)	S3 with pre-signed URLs for secure, temporary access
Double-booking appointments	Database constraints and transaction locking on time slots
Cost control	Serverless where possible, right-sized instances, billing alerts
