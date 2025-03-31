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
- Scheduling automated backups using Task Scheduler.
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
   - Created a function to return customers with a credit limit less than 96800.

8. **Triggers:**  
   - Implemented triggers to:
     - Log insert operations on the `employees` table.
     - Display customer numbers when payment amounts exceed 10,000.

9. **User Roles & Security:**  
   - Created users, roles, and logins for Admin, HR, and Employee, ensuring proper data access and security.

10. **Backup & Maintenance:**  
    - Scheduled database backups using Task Scheduler with a batch script due to the absence of SQL Agent in SQL Server Express.

11. **Monitoring:**  
    - Utilized Activity Monitor to record observations on processes, resource waits, and active expensive queries.

## Screenshots & Results

- **ER Diagram:**  
  - See `Screenshots/er_diagram.png` for the complete ER model.
- **Query Outputs:**  
  - Screenshots of key query executions, view creations, stored procedures, triggers, and backup operations are located in the `Screenshots` folder.
- **Live Examples:**  
  - Detailed examples are provided in the project report (`Project_Report.pdf`).

## Challenges & Resolutions

- **Data Type Mismatches:**  
  - Minor issues with data type mismatches and formatting during data insertion were resolved by updating the SQL scripts.
- **SQL Server Express Limitations:**  
  - Since SQL Agent was unavailable, backups were scheduled using Task Scheduler.

## Usage Instructions

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/MotorsCertification-SQL-Project.git

