# SQL-BASIC-COMMAND-ASSIGNMENT
Data Definition Language (DDL) commands provide the essential framework for building, maintaining, and managing database architectures. By effectively utilizing creation, alteration, and constraint rules, developers ensure long-term data integrity, security, and structural adaptability.
# DDL Commands & Constraints
   
   
   ## Table Creation (CREATE): 
                            ⦿ create a database named “employee” 
                            ⦿create tables Departments, Location , Employees
   ## Table Alteration (ALTER): Alter the structure of the tables accordingly:
                            ⦿ Add a new column named "email" to the Employees table to store employee email addresses. 
                                     Query: Alter table employees add column email varchar(20);
                            ⦿ Modify the data type of the "designation" column in the Employees table to support a wider range of values. 
                                     Query:Alter table employees modify column designation varchar (200);
                            ⦿ Drop the “age” column from the Employees table.
                                     Query: Alter table employees drop column age;
                                            
                            ⦿ Rename the “hire_date” column to “date_of_joining”.
                                      Query:Alter table employees rename column hire_date to date_of_joining;

   ## Table Renaming (RENAME): Rename the following tables: 
                            ⦿ Rename the "Departments" table to "Departments_Info". 
                                      Query: Rename table Departments to Departments_Info;
                            ⦿ Rename the "Location" table to "Locations".
                                      Query: Rename table location to locations

   ## Table Truncation (TRUNCATE): To truncate the Employees table. 
                                      Query:  truncate  table employees;
 

   ## Database & Table Dropping (DROP): Write the SQL statements to drop the Employees table and then the “employee” database.
                                      	Query1:drop table employees;
                                        Query2:drop database employees;

# Constraints 

## Departments Table:
	⦿Ensure that the "department_id" uniquely identifies each department.

	⦿Set up constraints on the "department_name" to avoid duplicate and null entries.
                          Query:create table Departments(department_id int unique,department_name varchar(100) 
unique not null);
## Location Table:
        ⦿Establish a mechanism to automatically generate unique identifiers for each location, ensuring that they are incremented sequentially. 
        ⦿Implement constraints to prevent the insertion of null and duplicate locations.
               
                          QUERY:  create table Location(location_id int auto_increment primary key ,location varchar(30) not null unique);
## Employees Table: 
	⦿Guarantee that each employee has a distinct identifier.
                      [Distinct identifier: employee_id INT AUTO_INCREMENT PRIMARY KEY (guarantees uniqueness and auto-increments).]
            
                               
   ⦿Create a restriction to ensure that the employee's name is always provided. 
                    [Employee name always provided: employee_name VARCHAR(50) NOT NULL (prevents null/missing names)].
   ⦿Limit the acceptable values for the "gender" field to only 'M' or 'F'. 
                    Gender limited to 'M' or 'F': gender ENUM('M', 'F') (restricts values)
   ⦿Enforce a condition to ensure that the employee's age is 18 or above.  
                    Age 18 or above: CHECK (age >= 18) (enforces the minimum age restriction).
   ⦿Automatically assign the current date to the "hire_date" field if not specified.
                    Auto-assign current date to hire date: hire_date DATE DEFAULT (CURRENT_DATE) (automatically populates today's date if omitted).
   ⦿Establish links between the "department_id" and "location_id" fields in the "employees" table and their respective tables.
                    Foreign key links: FOREIGN KEY constraints linking department_id and location_id to their respective tables








                                        
