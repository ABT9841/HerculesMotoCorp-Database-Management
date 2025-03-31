# HerculesMotoCorp-Database-Management
A comprehensive SQL Server database project designed for an automobile retailer, showcasing ER modeling, table creation, stored procedures, triggers, and more.

## Introduction

HerculesMotoCorp is a leading automobile retailer and garage service provider in the United States. Due to the complexity of its operations, the company required a robust Microsoft SQL Server database to efficiently manage customer records, orders, employees, payments, and inventory. This project, named **MotorsCertification**, was developed to meet these business requirements.

## Project Overview

As the Database Administrator, my task was to design and implement a comprehensive SQL Server database that involved:
- Designing an ER model and creating necessary tables with relationships.
- Inserting, updating, and managing data across multiple tables.
- Performing database operations such as removing unnecessary columns and retrieving key insights.
- Creating views, stored procedures, functions, and triggers to enhance database efficiency.
- Implementing user roles and permissions for different access levels (Admin, HR, and Employees).
- Scheduling automated backups using Task Scheduler since SQL Server Express lacks SQL Agent.
- (Note: Due to limitations with SQL Server Express, Azure migration was not implemented.)

## Technologies Used

- **Database:** Microsoft SQL Server
- **Query Language:** T-SQL (SQL)
- **Tools:** SQL Server Management Studio (SSMS), Task Scheduler (for backups)
- **Documentation:** Microsoft Word / PDF (project report with screenshots)

## Project Structure

## Implementation Steps

1. **ER Diagram & Table Design:**  
   - Designed an ER model and created tables (`orderdetails`, `customers`, `employees`, `orders`, `offices`, `payments`, `productlines`, and `products`) with appropriate primary keys, foreign keys, and indexes.

2. **Data Insertion:**  
   - Inserted records into tables in the following order: `orderdetails`, `employees`, `payments`, `products`, `customers`, `offices`, and `orders`.

3. **Data Cleanup:**  
   - Omitted unnecessary columns (`htmlDescription`, `image`) in the `productlines` table because they were not informative and contained null values.

4. **Data Verification:**  
   - Utilized SELECT statements to verify all data insertions and updates.

5. **Data Analysis:**  
   - Executed queries to determine the highest and lowest payment amounts and to check for duplicate customer names.

6. **View Creation:**  
   - Created a view (`cust_payment`) combining data from `customers` and `payments` to display customer names, amounts, and contact details, then later truncated and dropped it.

7. **Stored Procedures & Functions:**  
   - Developed a stored procedure to display the `productLine` for Classic Cars.
   - Created a function to return customers with a credit limit less than 96,800.

8. **Triggers:**  
   - Implemented triggers to:
     - Log insert operations on the `employees` table.
     - Display customer numbers when payment amounts exceed 10,000.

9. **User Roles & Security:**  
   - Created users, roles, and logins for Admin, HR, and Employee, ensuring proper data access and security.

10. **Backup & Maintenance:**  
    - Scheduled database backups using Task Scheduler with a batch script since SQL Server Express lacks SQL Agent.

11. **Monitoring:**  
    - Utilized Activity Monitor to record observations on processes, resource waits, and active expensive queries.

## How to Use

1. **Set up SQL Server:** Install Microsoft SQL Server and SQL Server Management Studio (SSMS).
2. **Import the SQL Scripts:** Execute the provided SQL scripts to create tables, insert data, and set up views, procedures, and triggers.
3. **Run Queries & Procedures:** Use SSMS to test queries, stored procedures, and functions.
4. **View Database Structure:** Open the provided ER diagram to understand table relationships.
5. **Test Security Features:** Log in with different user roles to validate access permissions.

## Screenshots & Results

- **ER Diagram:**
- - **ER Diagram:**  
  - ![ER Diagram](ER%20Diagram.png)

  - See [`ER Diagram.png`](https://github.com/ABT9841/HerculesMotoCorp-Database-Management/blob/98a3a386a357265329e553a3a3c4bdca4d7e7927/ER%20Diagram.png) for the complete ER model.
 for the complete ER model.
- **Query Outputs:**  
  - Screenshots of key query executions, view creations, stored procedures, triggers, and backup operations are located in the `Screenshots` folder.

 - **Live Examples:**  
  - Detailed examples are provided in the project report [here](https://github.com/ABT9841/HerculesMotoCorp-Database-Management/blob/98a3a386a357265329e553a3a3c4bdca4d7e7927/HerculesMotoCorp.pdf).


## Challenges & Resolutions

- **Data type mismatches:** Resolved by modifying column data types and ensuring proper constraints.
- **SQL Server Express limitations:** Used a batch script and Task Scheduler as an alternative to SQL Agent for automated backups.
