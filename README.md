# CLOUD-DATA-STORAGE-SERVER

### NAME: SANJNA G
### REG NO: 212225020043

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output


<img width="1156" height="876" alt="Screenshot 2026-11-20 083051" src="https://github.com/user-attachments/assets/01bd6c9d-4b1d-4b79-8ddf-6b4f33071b48" />
<img width="1147" height="881" alt="Screenshot 2026-11-20 083646" src="https://github.com/user-attachments/assets/e63bae4d-b317-4341-ac46-ea923431a9c9" />
<img width="1160" height="882" alt="Screenshot 2026-11-20 085335" src="https://github.com/user-attachments/assets/b708d137-a7a0-4062-894b-37ef02e737c7" />
<img width="1160" height="872" alt="Screenshot 2026-11-20 085647" src="https://github.com/user-attachments/assets/7d0fda7e-4a02-4883-aaf6-d86000746535" />
<img width="1140" height="886" alt="Screenshot 2026-11-20 090156" src="https://github.com/user-attachments/assets/5769f5f6-c602-4eee-ab8c-70389313c6a8" />
<img width="1470" height="540" alt="Screenshot 2026-11-20 090743" src="https://github.com/user-attachments/assets/69088140-aa03-4276-8b4a-b431bc709b8d" />
<img width="1511" height="501" alt="Screenshot 2026-11-20 091325" src="https://github.com/user-attachments/assets/8af915a0-fef6-4079-bb23-75bed6838926" />
<img width="1591" height="571" alt="Screenshot 2026-11-20 091431" src="https://github.com/user-attachments/assets/32b71b03-9b30-4799-b7e6-ecfb5281a16e" />


## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.
