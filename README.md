# Lab 5 – Assignment 1

## Deploy and Connect Database for Lab 4 EC2 Application

### Application

- Application: Listmonk
- Application Version: v4.1.0
- Platform: AWS EC2
- Database: PostgreSQL
- Database Service: Amazon RDS
- Region: us-east-1

## Architecture

EC2 (Listmonk)
        |
        | PostgreSQL : 5432
        |
        v
Amazon RDS PostgreSQL

## EC2 Details

- Instance ID: i-0f14bed30c0892d6a
- Instance Type: t3.micro
- OS: Ubuntu
- Application Port: 9000

## RDS Details

- DB Identifier: listmonk-rds
- Engine: PostgreSQL
- Instance Class: db.t4g.micro
- Storage: 20 GiB
- Port: 5432
- Public Access: No

## Database Security

The RDS Security Group allows PostgreSQL traffic on port 5432
only from the EC2 Security Group.

Source:

EC2 Security Group: sg-0f050f8cb5d449586

No public inbound rule (0.0.0.0/0) is configured for PostgreSQL.

## Database Migration

The PostgreSQL database used by the Lab 4 application was migrated
from the local PostgreSQL database on EC2 to Amazon RDS PostgreSQL.

The Listmonk database schema and existing data were migrated to RDS.

## Application Connection

Listmonk running on EC2 was configured to connect to the RDS PostgreSQL
endpoint using PostgreSQL port 5432 and SSL.

## CRUD Operations

The following CRUD operations were demonstrated:

### Create
Created a subscriber through the Listmonk application.

### Read
Read and displayed the subscriber record.

### Update
Updated the subscriber information.

### Delete
Deleted the test subscriber.

## Evidence

Screenshots included in this repository demonstrate:

1. EC2 Listmonk application
2. RDS PostgreSQL database
3. RDS Security Group configuration
4. Database connectivity
5. Create operation
6. Read operation
7. Update operation
8. Delete operation

## EC2 Application URL

http://98.90.201.154/admin/login
