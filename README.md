# Departments Table (Oracle SQL)

This SQL script creates a Departments table for a company database, inserts example department records, and displays the stored data.

## SQL Code

```sql
-- Step 1: Create the Departments table
CREATE TABLE departments (
    department_id NUMBER(5) PRIMARY KEY,
    department_name VARCHAR2(100) NOT NULL,
    manager_id NUMBER(5),
    location VARCHAR2(100)
);
```


department_id → Unique identifier for each department (Primary Key).

department_name → Name of the department (required).

manager_id → ID of the department’s manager.

location → City/location of the department.


```sql
Step 2: Insert Example Departments
INSERT INTO departments (department_id, department_name, manager_id, location)
VALUES (10, 'Human Resources', 101, 'New York');

INSERT INTO departments (department_id, department_name, manager_id, location)
VALUES (20, 'Finance', 102, 'London');

INSERT INTO departments (department_id, department_name, manager_id, location)
VALUES (30, 'Sales', 103, 'Dubai');

INSERT INTO departments (department_id, department_name, manager_id, location)
VALUES (40, 'IT', 104, 'San Francisco');

INSERT INTO departments (department_id, department_name, manager_id, location)
VALUES (50, 'Marketing', 105, 'Singapore');
```


Inserts 5 sample departments: HR, Finance, Sales, IT, and Marketing.

Each has a unique department_id, a manager, and a location.


```
Step 3: Commit Changes
COMMIT;
```


Saves all insert operations to the database permanently.


```
Step 4: View the Data
SELECT * FROM departments;
```


Displays all rows and columns from the departments table.


## Example Output

When you run the SELECT query, you should see:

DEPARTMENT_ID  DEPARTMENT_NAME   MANAGER_ID   LOCATION
-------------  ----------------  ----------   -------------
10             Human Resources   101          New York
20             Finance           102          London
30             Sales             103          Dubai
40             IT                104          San Francisco
50             Marketing         105          Singapore
