
## Technology Docs

- [Angular](Angular.md)  
- [MongoDB](MongoDB.md)  
- [MySQL](Mysql.md)  
- [Node.js](Node-Js.md)  
- [TypeScript](TypeScript.md)  
- [JavaScript](JavaScript.md)

Here is a list of 100+ common MySQL interview questions and answers:

### Basic MySQL Interview Questions:

1. **What is MySQL?**
   - MySQL is an open-source relational database management system (RDBMS) that uses SQL (Structured Query Language) to manage and query data.

2. **What is a database?**
   - A database is an organized collection of data stored and accessed electronically. It allows for storing, modifying, and querying data in a structured way.

3. **What are the different types of joins in MySQL?**
   - **INNER JOIN**: Returns only matching rows from both tables.
   - **LEFT JOIN**: Returns all rows from the left table and matching rows from the right table.
   - **RIGHT JOIN**: Returns all rows from the right table and matching rows from the left table.
   - **FULL OUTER JOIN**: Returns rows when there is a match in one of the tables.
   - **CROSS JOIN**: Returns the Cartesian product of both tables.

4. **What is the difference between `WHERE` and `HAVING`?**
   - **WHERE**: Filters rows before any grouping is done.
   - **HAVING**: Filters rows after the `GROUP BY` clause has been applied.

5. **Explain the different data types in MySQL.**
   - **Numeric**: INT, FLOAT, DOUBLE, DECIMAL.
   - **String**: CHAR, VARCHAR, TEXT, BLOB.
   - **Date and Time**: DATE, DATETIME, TIMESTAMP, TIME, YEAR.
   - **Miscellaneous**: ENUM, SET.

6. **What are primary keys and foreign keys in MySQL?**
   - **Primary Key**: A unique identifier for each record in a table. Cannot be `NULL`.
   - **Foreign Key**: A key used to link two tables. It references the primary key in another table.

7. **What is normalization?**
   - Normalization is the process of organizing a database to reduce redundancy and improve data integrity by dividing large tables into smaller, related tables.

8. **What are the normal forms in MySQL?**
   - **1st Normal Form (1NF)**: Ensures that the table has only atomic columns (no repeating groups).
   - **2nd Normal Form (2NF)**: Ensures that all non-key attributes are fully functionally dependent on the primary key.
   - **3rd Normal Form (3NF)**: Ensures that no transitive dependencies exist between non-key attributes.
   - **Boyce-Codd Normal Form (BCNF)**: A stricter version of 3NF.

9. **What is an index in MySQL?**
   - An index is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional space and slower writes.

10. **What is the difference between `CHAR` and `VARCHAR`?**
    - **CHAR**: Fixed-length string data type. Padding is done with spaces.
    - **VARCHAR**: Variable-length string data type. It only uses as much space as needed.

### Intermediate MySQL Interview Questions:

11. **What is a subquery in MySQL?**
    - A subquery is a query within another query, usually used in `SELECT`, `INSERT`, `UPDATE`, or `DELETE` statements.

12. **What is a stored procedure in MySQL?**
    - A stored procedure is a set of SQL statements that can be stored and executed on the MySQL server to perform complex operations.

13. **What is a trigger in MySQL?**
    - A trigger is a set of SQL statements that automatically execute in response to certain events on a table (e.g., `INSERT`, `UPDATE`, `DELETE`).

14. **What is the use of the `AUTO_INCREMENT` attribute in MySQL?**
    - The `AUTO_INCREMENT` attribute automatically generates a unique value for a column, usually used for primary keys.

15. **Explain the difference between `TRUNCATE` and `DELETE`.**
    - **TRUNCATE**: Removes all records from a table without logging individual row deletions. It is faster but cannot be rolled back.
    - **DELETE**: Removes rows based on a condition, can be rolled back, and is slower than `TRUNCATE`.

16. **What is the purpose of the `LIMIT` clause in MySQL?**
    - The `LIMIT` clause is used to specify the number of rows to return in a query result.

17. **What is the difference between `UNION` and `UNION ALL`?**
    - **UNION**: Combines the result sets of two or more queries and removes duplicates.
    - **UNION ALL**: Combines the result sets of two or more queries without removing duplicates.

18. **What is the `GROUP BY` clause in MySQL?**
    - The `GROUP BY` clause groups rows that have the same values in specified columns into summary rows, often used with aggregate functions like `COUNT`, `SUM`, `AVG`, etc.

19. **What is the difference between `IN` and `EXISTS`?**
    - **IN**: Used to check if a value is present in a list of values.
    - **EXISTS**: Checks if a subquery returns any results.

20. **What is the purpose of the `ORDER BY` clause in MySQL?**
    - The `ORDER BY` clause sorts the result set of a query by one or more columns, either ascending or descending.

### Advanced MySQL Interview Questions:

21. **Explain the concept of transactions in MySQL.**
    - A transaction is a set of SQL statements that are executed as a unit. Transactions ensure data integrity and consistency with properties known as ACID (Atomicity, Consistency, Isolation, Durability).

22. **What are the different isolation levels in MySQL?**
    - **READ UNCOMMITTED**: Allows dirty reads.
    - **READ COMMITTED**: Prevents dirty reads, but non-repeatable reads are allowed.
    - **REPEATABLE READ**: Prevents dirty and non-repeatable reads.
    - **SERIALIZABLE**: The highest level of isolation that prevents all concurrency.

23. **What are the advantages of using indexing in MySQL?**
    - Indexing improves query performance by reducing the amount of data the database needs to scan.

24. **What is the difference between `INNER JOIN` and `LEFT JOIN`?**
    - **INNER JOIN**: Returns only matching records from both tables.
    - **LEFT JOIN**: Returns all records from the left table and matching records from the right table.

25. **What is the difference between `TRIGGERS` and `STORED PROCEDURES`?**
    - **Triggers** are automatically executed based on events (INSERT, UPDATE, DELETE) on a table, whereas **stored procedures** are explicitly called by the user.

26. **How do you optimize a slow-performing query in MySQL?**
    - You can optimize queries by:
      - Using indexes
      - Avoiding `SELECT *`
      - Using `EXPLAIN` to analyze query execution
      - Properly using joins and subqueries
      - Caching results where possible
      - Breaking down complex queries into simpler parts

27. **What is the `EXPLAIN` command in MySQL?**
    - The `EXPLAIN` command provides information about how MySQL executes a query, including the use of indexes and the order of table joins.

28. **What is the use of `FOREIGN KEY` in MySQL?**
    - A `FOREIGN KEY` ensures referential integrity by enforcing a relationship between two tables, where a value in one table must exist in another.

29. **What are the differences between MyISAM and InnoDB storage engines in MySQL?**
    - **MyISAM**: Faster read operations, doesn't support transactions or foreign keys.
    - **InnoDB**: Supports transactions, foreign keys, and ACID compliance.

30. **What is `ACID` in database transactions?**
    - **Atomicity**: Ensures that all operations within a transaction are completed successfully or none are applied.
    - **Consistency**: Ensures the database remains in a consistent state before and after a transaction.
    - **Isolation**: Ensures transactions are executed independently of each other.
    - **Durability**: Ensures that once a transaction is committed, it will persist even in the event of a system crash.

---

Certainly! Here are more MySQL interview questions with examples:

---

### 31. **What is the difference between `UNIQUE` and `PRIMARY KEY`?**
   - **PRIMARY KEY**: Uniquely identifies a record and does not allow `NULL` values.
   - **UNIQUE**: Ensures that all values in a column are different but allows `NULL` values.

   **Example:**
   ```sql
   CREATE TABLE Users (
       UserID INT PRIMARY KEY,
       Username VARCHAR(50) UNIQUE
   );
   ```

---

### 32. **Explain the `LEFT JOIN` with an example.**

   **Example:**
   ```sql
   SELECT Orders.OrderID, Customers.CustomerName
   FROM Orders
   LEFT JOIN Customers
   ON Orders.CustomerID = Customers.CustomerID;
   ```
   - This query will return all orders, even if there is no matching customer. If no match is found, the `CustomerName` will be `NULL`.

---

### 33. **What is a `BETWEEN` operator in MySQL?**

   The `BETWEEN` operator is used to filter the result set within a certain range (inclusive of the boundary values).

   **Example:**
   ```sql
   SELECT * FROM Employees
   WHERE Salary BETWEEN 50000 AND 100000;
   ```
   - This query will return all employees with a salary between 50,000 and 100,000 (inclusive).

---

### 34. **What are aggregate functions in MySQL?**

   Aggregate functions perform a calculation on a set of values and return a single value. Common aggregate functions are `COUNT()`, `SUM()`, `AVG()`, `MAX()`, and `MIN()`.

   **Example:**
   ```sql
   SELECT COUNT(*) FROM Employees WHERE Department = 'HR';
   ```
   - This query will return the number of employees in the 'HR' department.

---

### 35. **What is the difference between `NULL` and `NOT NULL`?**

   - **NULL**: Represents a missing or undefined value.
   - **NOT NULL**: Ensures that a column cannot have a `NULL` value.

   **Example:**
   ```sql
   CREATE TABLE Employees (
       EmployeeID INT NOT NULL,
       EmployeeName VARCHAR(100),
       Department VARCHAR(100) NOT NULL
   );
   ```
   - In this table, the `Department` column cannot be `NULL`.

---

### 36. **What is a `CASE` statement in MySQL?**

   The `CASE` statement is used for conditional logic in queries. It works similarly to `if-else` statements.

   **Example:**
   ```sql
   SELECT EmployeeName,
          CASE
              WHEN Salary > 100000 THEN 'High Salary'
              WHEN Salary BETWEEN 50000 AND 100000 THEN 'Medium Salary'
              ELSE 'Low Salary'
          END AS SalaryCategory
   FROM Employees;
   ```
   - This query categorizes employees based on their salary.

---

### 37. **How do you create an index in MySQL?**

   An index is created using the `CREATE INDEX` statement to speed up query performance.

   **Example:**
   ```sql
   CREATE INDEX idx_employee_name ON Employees(EmployeeName);
   ```
   - This creates an index on the `EmployeeName` column, which will improve query performance when filtering or sorting by name.

---

### 38. **Explain the `DISTINCT` keyword in MySQL.**

   The `DISTINCT` keyword is used to remove duplicate values in the result set.

   **Example:**
   ```sql
   SELECT DISTINCT Department FROM Employees;
   ```
   - This query will return a list of unique departments, removing any duplicates.

---

### 39. **What is the difference between `TRUNCATE` and `DELETE`?**

   - **TRUNCATE**: Removes all rows from a table but does not log individual row deletions and cannot be rolled back.
   - **DELETE**: Removes rows based on a condition and can be rolled back if wrapped in a transaction.

   **Example of `DELETE`:**
   ```sql
   DELETE FROM Employees WHERE Department = 'HR';
   ```

   **Example of `TRUNCATE`:**
   ```sql
   TRUNCATE TABLE Employees;
   ```

---

### 40. **What is a `SELF JOIN` in MySQL?**

   A self join is a regular join, but the table is joined with itself.

   **Example:**
   ```sql
   SELECT e1.EmployeeName AS Employee, e2.EmployeeName AS Manager
   FROM Employees e1
   JOIN Employees e2 ON e1.ManagerID = e2.EmployeeID;
   ```
   - This query returns a list of employees and their managers by joining the `Employees` table with itself.

---

### 41. **What is the difference between `INNER JOIN` and `LEFT JOIN`?**

   - **INNER JOIN**: Returns only the rows that have matching values in both tables.
   - **LEFT JOIN**: Returns all rows from the left table and matching rows from the right table. If no match is found, `NULL` values are returned for the right table columns.

   **Example of `INNER JOIN`:**
   ```sql
   SELECT Orders.OrderID, Customers.CustomerName
   FROM Orders
   INNER JOIN Customers
   ON Orders.CustomerID = Customers.CustomerID;
   ```

   **Example of `LEFT JOIN`:**
   ```sql
   SELECT Orders.OrderID, Customers.CustomerName
   FROM Orders
   LEFT JOIN Customers
   ON Orders.CustomerID = Customers.CustomerID;
   ```

---

### 42. **What is the `EXPLAIN` command in MySQL?**

   The `EXPLAIN` command provides information about how MySQL executes a query. It is useful for query optimization.

   **Example:**
   ```sql
   EXPLAIN SELECT * FROM Employees WHERE Department = 'HR';
   ```
   - This will show the execution plan for the query, including the use of indexes and join types.

---

### 43. **What is a `VIEW` in MySQL?**

   A view is a virtual table that contains the result of a query. It does not store data but allows users to query complex data easily.

   **Example:**
   ```sql
   CREATE VIEW EmployeeView AS
   SELECT EmployeeName, Department, Salary
   FROM Employees
   WHERE Salary > 50000;
   ```

---

### 44. **What is `AUTO_INCREMENT` in MySQL?**

   The `AUTO_INCREMENT` attribute is used to generate unique identifiers automatically for new records.

   **Example:**
   ```sql
   CREATE TABLE Employees (
       EmployeeID INT AUTO_INCREMENT PRIMARY KEY,
       EmployeeName VARCHAR(100)
   );
   ```
   - The `EmployeeID` will automatically increment with each new row.

---

### 45. **What is `JOIN` optimization in MySQL?**

   - Proper indexing on the columns involved in the join condition can help optimize the performance.
   - Ensure that you join on indexed columns.
   - Avoid joining large tables without necessary filters or conditions.

   **Example of JOIN optimization:**
   ```sql
   CREATE INDEX idx_customer_id ON Orders(CustomerID);
   ```
   - This index speeds up the join between `Orders` and `Customers` tables on the `CustomerID` column.

---

### 46. **What are `temporary tables` in MySQL?**

   Temporary tables are tables that exist temporarily during the session and are automatically dropped when the session ends.

   **Example:**
   ```sql
   CREATE TEMPORARY TABLE TempOrders AS
   SELECT * FROM Orders WHERE OrderDate > '2024-01-01';
   ```
   - This creates a temporary table `TempOrders` which can be used within the session.

---

### 47. **How to prevent SQL injection in MySQL?**

   SQL injection can be prevented by using prepared statements and parameterized queries.

   **Example using PHP (PDO):**
   ```php
   $stmt = $pdo->prepare('SELECT * FROM Users WHERE Username = :username AND Password = :password');
   $stmt->execute(['username' => $username, 'password' => $password]);
   ```

---

### 48. **What is `REPLACE INTO` in MySQL?**

   The `REPLACE INTO` statement works like `INSERT`, but if the record already exists (based on the primary key or unique key), it deletes the old record and inserts the new one.

   **Example:**
   ```sql
   REPLACE INTO Employees (EmployeeID, EmployeeName)
   VALUES (1, 'John Doe');
   ```

---

### 49. **What is `FULLTEXT` search in MySQL?**

   `FULLTEXT` search is used to search for text-based content in a table. It is available for `CHAR`, `VARCHAR`, and `TEXT` columns.

   **Example:**
   ```sql
   CREATE TABLE Articles (
       ArticleID INT PRIMARY KEY,
       Content TEXT,
       FULLTEXT(Content)
   );

   SELECT * FROM Articles
   WHERE MATCH(Content) AGAINST('search term');
   ```

---

### 50. **What is the difference between `NOW()` and `CURDATE()`?**

   - **NOW()**: Returns the current date and time.
   - **CURDATE()**: Returns the current date (without time).

   **Example:**
   ```sql
   SELECT NOW();    -- Returns '2024-12-31 10:00:00'
   SELECT CURDATE(); -- Returns '2024-12-31'
   ```

---

Certainly! Here are more advanced MySQL interview questions with examples:

---

### 51. **What is the difference between `LEFT JOIN` and `RIGHT JOIN`?**

   - **LEFT JOIN**: Returns all records from the left table, and the matching records from the right table. If no match is found, `NULL` values are returned for the right table's columns.
   - **RIGHT JOIN**: Returns all records from the right table, and the matching records from the left table. If no match is found, `NULL` values are returned for the left table's columns.

   **Example:**
   ```sql
   SELECT Orders.OrderID, Customers.CustomerName
   FROM Orders
   LEFT JOIN Customers
   ON Orders.CustomerID = Customers.CustomerID;
   ```

   ```sql
   SELECT Orders.OrderID, Customers.CustomerName
   FROM Orders
   RIGHT JOIN Customers
   ON Orders.CustomerID = Customers.CustomerID;
   ```

---

### 52. **What is the difference between `UNION` and `UNION ALL` in MySQL?**

   - **UNION**: Combines the results of two queries and removes duplicate rows.
   - **UNION ALL**: Combines the results of two queries without removing duplicates.

   **Example of `UNION`:**
   ```sql
   SELECT EmployeeName FROM Employees WHERE Department = 'HR'
   UNION
   SELECT EmployeeName FROM Employees WHERE Department = 'Finance';
   ```

   **Example of `UNION ALL`:**
   ```sql
   SELECT EmployeeName FROM Employees WHERE Department = 'HR'
   UNION ALL
   SELECT EmployeeName FROM Employees WHERE Department = 'Finance';
   ```

---

### 53. **What is the `GROUP_CONCAT()` function in MySQL?**

   The `GROUP_CONCAT()` function is used to concatenate values from multiple rows into a single string.

   **Example:**
   ```sql
   SELECT Department, GROUP_CONCAT(EmployeeName) AS Employees
   FROM Employees
   GROUP BY Department;
   ```
   - This query will group employees by department and concatenate their names into a single string for each department.

---

### 54. **What is a `FOREIGN KEY` constraint in MySQL?**

   A `FOREIGN KEY` constraint is used to link two tables together by ensuring that the value in the foreign key column matches a value in the referenced table’s primary key.

   **Example:**
   ```sql
   CREATE TABLE Departments (
       DepartmentID INT PRIMARY KEY,
       DepartmentName VARCHAR(100)
   );

   CREATE TABLE Employees (
       EmployeeID INT PRIMARY KEY,
       EmployeeName VARCHAR(100),
       DepartmentID INT,
       FOREIGN KEY (DepartmentID) REFERENCES Departments(DepartmentID)
   );
   ```

---

### 55. **What are `Transactions` in MySQL?**

   A transaction is a sequence of SQL statements executed as a single unit. It ensures that operations are performed in an atomic and consistent manner. The transaction is controlled with `COMMIT` and `ROLLBACK`.

   **Example:**
   ```sql
   START TRANSACTION;
   UPDATE Employees SET Salary = Salary + 5000 WHERE EmployeeID = 1;
   UPDATE Employees SET Salary = Salary - 5000 WHERE EmployeeID = 2;
   COMMIT;
   ```

   If something goes wrong, you can use `ROLLBACK`:
   ```sql
   ROLLBACK;
   ```

---

### 56. **What is the `EXPLAIN` keyword in MySQL?**

   The `EXPLAIN` keyword provides details about how MySQL executes a query. It shows the execution plan, which can be useful for optimizing queries.

   **Example:**
   ```sql
   EXPLAIN SELECT * FROM Employees WHERE Department = 'HR';
   ```

   The output will show information like:
   - How the query is executed
   - Whether indexes are used
   - The number of rows MySQL expects to examine

---

### 57. **How does MySQL handle case sensitivity?**

   - By default, MySQL is case-insensitive for string comparisons in most collation types (`utf8_general_ci` is case-insensitive).
   - You can enforce case-sensitivity using binary collation like `utf8_bin`.

   **Example:**
   ```sql
   SELECT * FROM Employees WHERE EmployeeName = 'john'; -- Case-insensitive by default
   SELECT * FROM Employees WHERE BINARY EmployeeName = 'john'; -- Case-sensitive
   ```

---

### 58. **How do you create a backup of a MySQL database?**

   You can create a backup using the `mysqldump` utility.

   **Example:**
   ```bash
   mysqldump -u root -p my_database > backup.sql
   ```
   - This command backs up the `my_database` database to a file called `backup.sql`.

---

### 59. **What is the difference between `CHAR` and `VARCHAR` data types?**

   - **CHAR**: A fixed-length string data type. It uses the same amount of storage space regardless of the actual string length.
   - **VARCHAR**: A variable-length string data type. It only uses as much space as needed to store the string.

   **Example:**
   ```sql
   CREATE TABLE Users (
       UserID INT PRIMARY KEY,
       Username CHAR(50),   -- Fixed-length string
       UserEmail VARCHAR(100)  -- Variable-length string
   );
   ```

---

### 60. **What is `LOCKING` in MySQL?**

   In MySQL, locking is used to prevent multiple sessions from modifying the same data at the same time, ensuring data consistency and preventing conflicts.

   **Types of Locks:**
   - **Read Lock**: Prevents other sessions from writing to the locked resource but allows them to read it.
   - **Write Lock**: Prevents other sessions from both reading and writing to the locked resource.

   **Example of a read lock:**
   ```sql
   LOCK TABLE Employees READ;
   ```

   **Example of a write lock:**
   ```sql
   LOCK TABLE Employees WRITE;
   ```

---

### 61. **What is a `Self Join` in MySQL?**

   A self-join is when a table is joined with itself. It is typically used to find relationships between rows in the same table.

   **Example:**
   ```sql
   SELECT e1.EmployeeName AS Employee, e2.EmployeeName AS Manager
   FROM Employees e1
   LEFT JOIN Employees e2 ON e1.ManagerID = e2.EmployeeID;
   ```

---

### 62. **What are `Stored Procedures` in MySQL?**

   A stored procedure is a precompiled collection of one or more SQL statements. It can be executed as a single unit to perform a task or operation.

   **Example:**
   ```sql
   DELIMITER //
   CREATE PROCEDURE GetEmployeeDetails(IN empID INT)
   BEGIN
       SELECT EmployeeName, Department FROM Employees WHERE EmployeeID = empID;
   END //
   DELIMITER ;
   ```

   To execute the stored procedure:
   ```sql
   CALL GetEmployeeDetails(1);
   ```

---

### 63. **What is the `LIMIT` clause in MySQL?**

   The `LIMIT` clause is used to specify the number of rows returned by a query. It is useful when you want to retrieve only a subset of the result set.

   **Example:**
   ```sql
   SELECT * FROM Employees LIMIT 5;
   ```

   To get rows from a specific offset:
   ```sql
   SELECT * FROM Employees LIMIT 5, 10;  -- Skips the first 5 rows and returns the next 10
   ```

---

### 64. **What are `Triggers` in MySQL?**

   Triggers are special types of stored procedures that are automatically invoked when a specified event (INSERT, UPDATE, DELETE) occurs on a table.

   **Example:**
   ```sql
   CREATE TRIGGER before_insert_employee
   BEFORE INSERT ON Employees
   FOR EACH ROW
   BEGIN
       SET NEW.EmployeeName = UPPER(NEW.EmployeeName);
   END;
   ```

   This trigger automatically converts the employee name to uppercase before inserting a record.

---

### 65. **What is `Normalization` and its types in MySQL?**

   **Normalization** is the process of organizing a database to reduce redundancy and improve data integrity. It involves dividing large tables into smaller, related tables and using foreign keys to establish relationships.

   The different **Normal Forms** are:
   - **1NF** (First Normal Form): Ensures atomicity of data (no repeating groups).
   - **2NF** (Second Normal Form): Ensures no partial dependency (all non-key attributes are fully dependent on the primary key).
   - **3NF** (Third Normal Form): Ensures no transitive dependency (non-key attributes depend only on the primary key).

   **Example of 1NF:**
   ```sql
   CREATE TABLE Orders (
       OrderID INT PRIMARY KEY,
       CustomerName VARCHAR(100),
       ProductName VARCHAR(100),
       Quantity INT
   );
   ```

   - This table is in 1NF because there are no repeating groups of columns. Each row is atomic.

---

### 66. **What is the `REPLACE INTO` statement in MySQL?**

   The `REPLACE INTO` statement is similar to `INSERT`, but if a record with the same primary key or unique key exists, it deletes the old record and inserts the new one.

   **Example:**
   ```sql
   REPLACE INTO Employees (EmployeeID, EmployeeName)
   VALUES (1, 'John Doe');
   ```

---

Here are even more advanced MySQL interview questions with examples:

---

### 67. **What is the difference between `TRUNCATE` and `DELETE` in MySQL?**

   - **TRUNCATE**: Deletes all rows from a table without logging individual row deletions. It's faster but cannot be rolled back unless wrapped in a transaction.
   - **DELETE**: Deletes rows based on a condition, logs each deletion, and can be rolled back if wrapped in a transaction.

   **Example of DELETE:**
   ```sql
   DELETE FROM Employees WHERE Department = 'HR';
   ```

   **Example of TRUNCATE:**
   ```sql
   TRUNCATE TABLE Employees;
   ```

---

### 68. **What is the `HAVING` clause in MySQL?**

   The `HAVING` clause is used to filter records after the `GROUP BY` clause. It's similar to `WHERE` but is applied to aggregated data.

   **Example:**
   ```sql
   SELECT Department, COUNT(*) AS EmployeeCount
   FROM Employees
   GROUP BY Department
   HAVING COUNT(*) > 5;
   ```
   - This query returns departments with more than 5 employees.

---

### 69. **What is a `Composite Key` in MySQL?**

   A composite key is a combination of two or more columns in a table that uniquely identifies each record.

   **Example:**
   ```sql
   CREATE TABLE OrderDetails (
       OrderID INT,
       ProductID INT,
       Quantity INT,
       PRIMARY KEY (OrderID, ProductID)
   );
   ```

---

### 70. **What is the `LIMIT` clause with `OFFSET`?**

   The `LIMIT` clause can be used with `OFFSET` to return a specific range of rows, useful for pagination.

   **Example:**
   ```sql
   SELECT * FROM Employees LIMIT 10 OFFSET 20;
   ```
   - This query returns rows 21 to 30 (skip first 20 rows).

---

### 71. **What is the `CHARACTER SET` and `COLLATE` in MySQL?**

   - **CHARACTER SET**: Defines the set of characters that a column can store (e.g., `utf8`).
   - **COLLATE**: Defines the rules for comparing characters in a column, including case-sensitivity and accent sensitivity.

   **Example:**
   ```sql
   CREATE TABLE Users (
       Username VARCHAR(100) CHARACTER SET utf8 COLLATE utf8_general_ci
   );
   ```

---

### 72. **What are `Foreign Key Constraints` in MySQL?**

   Foreign key constraints ensure data integrity by enforcing a link between columns in different tables. The foreign key column must contain values that match primary or unique key columns in the referenced table.

   **Example:**
   ```sql
   CREATE TABLE Orders (
       OrderID INT PRIMARY KEY,
       CustomerID INT,
       FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
   );
   ```

---

### 73. **What is a `NULL` value in MySQL and how does it behave in comparisons?**

   A `NULL` value represents missing or undefined data. In MySQL, `NULL` is not equal to any value, not even another `NULL`. You must use `IS NULL` or `IS NOT NULL` to compare.

   **Example:**
   ```sql
   SELECT * FROM Employees WHERE Department IS NULL;
   ```

---

### 74. **What is `AUTO_INCREMENT` in MySQL?**

   The `AUTO_INCREMENT` keyword automatically generates a unique value for a column, typically used for primary keys.

   **Example:**
   ```sql
   CREATE TABLE Employees (
       EmployeeID INT AUTO_INCREMENT PRIMARY KEY,
       EmployeeName VARCHAR(100)
   );
   ```

   - Each time a new row is inserted, `EmployeeID` will automatically increment.

---

### 75. **What are `Indexes` in MySQL?**

   Indexes are used to speed up the retrieval of data by providing a quick lookup for rows in a table. They can be created on one or more columns.

   **Example:**
   ```sql
   CREATE INDEX idx_employee_name ON Employees(EmployeeName);
   ```

   - This index will speed up queries that filter by `EmployeeName`.

---

### 76. **What are `Stored Functions` in MySQL?**

   A stored function is similar to a stored procedure but it returns a value. It's a way to encapsulate logic in a reusable function.

   **Example:**
   ```sql
   DELIMITER //
   CREATE FUNCTION GetEmployeeSalary(EmployeeID INT) RETURNS DECIMAL(10,2)
   BEGIN
       DECLARE salary DECIMAL(10,2);
       SELECT Salary INTO salary FROM Employees WHERE EmployeeID = EmployeeID;
       RETURN salary;
   END //
   DELIMITER ;
   ```

---

### 77. **What is the `SET` data type in MySQL?**

   The `SET` data type allows you to store multiple values in a column, where each value is selected from a predefined set of options.

   **Example:**
   ```sql
   CREATE TABLE Users (
       UserID INT PRIMARY KEY,
       Preferences SET('Email', 'SMS', 'Push')
   );
   ```

---

### 78. **How do you implement pagination in MySQL?**

   Pagination can be implemented by using the `LIMIT` and `OFFSET` clauses.

   **Example:**
   ```sql
   SELECT * FROM Employees LIMIT 10 OFFSET 0;  -- Page 1
   SELECT * FROM Employees LIMIT 10 OFFSET 10; -- Page 2
   ```

---

### 79. **What is the `REGEXP` operator in MySQL?**

   The `REGEXP` operator is used for pattern matching in MySQL with regular expressions.

   **Example:**
   ```sql
   SELECT * FROM Employees WHERE EmployeeName REGEXP '^J';
   ```
   - This query returns employees whose names start with the letter 'J'.

---

### 80. **What are `Triggers` in MySQL?**

   A trigger is a stored procedure that automatically executes in response to certain events on a table or view, such as `INSERT`, `UPDATE`, or `DELETE`.

   **Example:**
   ```sql
   CREATE TRIGGER before_insert_employee
   BEFORE INSERT ON Employees
   FOR EACH ROW
   BEGIN
       SET NEW.EmployeeName = UPPER(NEW.EmployeeName);
   END;
   ```

---

### 81. **What is `Replication` in MySQL?**

   Replication is the process of copying data from one MySQL server (master) to another (slave). It can be used for load balancing, data redundancy, and backup purposes.

   - **Master-Slave Replication**: The master server writes data, and the slave servers replicate the data.

---

### 82. **What is the `LOAD DATA INFILE` statement in MySQL?**

   The `LOAD DATA INFILE` statement is used to load data from a file into a table. It's faster than inserting rows individually.

   **Example:**
   ```sql
   LOAD DATA INFILE '/path/to/file.csv' INTO TABLE Employees
   FIELDS TERMINATED BY ',' ENCLOSED BY '"' LINES TERMINATED BY '\n';
   ```

---

### 83. **What is the `OPTIMIZE TABLE` command in MySQL?**

   The `OPTIMIZE TABLE` command is used to reclaim unused space and defragment the table. It can improve performance for large tables.

   **Example:**
   ```sql
   OPTIMIZE TABLE Employees;
   ```

---

### 84. **What is the `SHOW TABLES` command in MySQL?**

   The `SHOW TABLES` command lists all tables in a database.

   **Example:**
   ```sql
   SHOW TABLES;
   ```

---

### 85. **What is `Database Normalization`?**

   **Normalization** is the process of organizing data in a database to minimize redundancy and dependency. It involves dividing large tables into smaller ones and linking them using foreign keys.

   The stages of normalization are:
   - **1NF (First Normal Form)**: No repeating groups.
   - **2NF (Second Normal Form)**: No partial dependency.
   - **3NF (Third Normal Form)**: No transitive dependency.

---

### 86. **What are `Cursors` in MySQL?**

   A cursor in MySQL is used to retrieve a result set row by row. It's typically used inside stored procedures to loop through query results.

   **Example:**
   ```sql
   DECLARE done INT DEFAULT FALSE;
   DECLARE empName VARCHAR(100);
   DECLARE empCursor CURSOR FOR SELECT EmployeeName FROM Employees;
   DECLARE CONTINUE HANDLER FOR NOT FOUND SET done = TRUE;

   OPEN empCursor;
   read_loop: LOOP
       FETCH empCursor INTO empName;
       IF done THEN
           LEAVE read_loop;
       END IF;
       -- Process the row
   END LOOP;
   CLOSE empCursor;
   ```

---

### 87. **What is `Foreign Key` Constraint in MySQL?**

   A `FOREIGN KEY` constraint is used to establish a relationship between two tables, ensuring that the value in the foreign key column matches a value in the referenced column.

   **Example:**
   ```sql
   CREATE TABLE Orders (
       OrderID INT PRIMARY KEY,
       CustomerID INT,
       FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
   );
   ```

---

### 88. **How do you handle `Deadlocks` in MySQL?**

   A **deadlock** occurs when two or more transactions hold locks on resources that the other transactions are trying to access. MySQL detects deadlocks and automatically resolves them by rolling back one of the transactions.

   - To avoid deadlocks, you should:
     - Access tables in the same order across all transactions.
     - Keep transactions short and use `BEGIN`, `COMMIT`, and `ROLLBACK` appropriately.

---

### 89. **What is the `EXPLAIN` keyword in MySQL?**

   The `EXPLAIN` keyword is used to obtain information about how MySQL executes a query. It can help optimize queries by showing the execution plan.

   **Example:**
   ```sql
   EXPLAIN SELECT * FROM Employees WHERE Department = 'HR';
   ```

---

### 90. **How do you create an index in MySQL?**

   An index is created using the `CREATE INDEX` statement to speed up the retrieval of rows from a table.

   **Example:**
   ```sql
   CREATE INDEX idx_employee_name ON Employees(EmployeeName);
   ```

---

Here are even more advanced MySQL interview questions with examples:

---

### 91. **What is a `VIEW` in MySQL?**

   A `VIEW` is a virtual table based on the result of a SELECT query. It doesn't store data itself but provides a way to represent data from one or more tables in a more readable format.

   **Example:**
   ```sql
   CREATE VIEW EmployeeDetails AS
   SELECT EmployeeID, EmployeeName, Department
   FROM Employees
   WHERE Department = 'HR';
   ```

   - To query the view:
   ```sql
   SELECT * FROM EmployeeDetails;
   ```

---

### 92. **What is the difference between `AND` and `OR` in a WHERE clause?**

   - **AND**: Both conditions must be true for the query to return a result.
   - **OR**: Either one of the conditions must be true for the query to return a result.

   **Example with `AND`:**
   ```sql
   SELECT * FROM Employees WHERE Department = 'HR' AND Salary > 50000;
   ```

   **Example with `OR`:**
   ```sql
   SELECT * FROM Employees WHERE Department = 'HR' OR Salary > 50000;
   ```

---

### 93. **What is a `Subquery` in MySQL?**

   A `Subquery` is a query nested inside another query. It can be used in `WHERE`, `FROM`, or `SELECT` clauses to provide a result set that is used by the outer query.

   **Example:**
   ```sql
   SELECT EmployeeName
   FROM Employees
   WHERE DepartmentID = (SELECT DepartmentID FROM Departments WHERE DepartmentName = 'HR');
   ```

---

### 94. **What is the `GROUP BY` clause in MySQL?**

   The `GROUP BY` clause groups rows that have the same values into summary rows, often used with aggregate functions like `COUNT`, `SUM`, `AVG`, `MAX`, or `MIN`.

   **Example:**
   ```sql
   SELECT Department, COUNT(*) AS EmployeeCount
   FROM Employees
   GROUP BY Department;
   ```

---

### 95. **What is the `DISTINCT` keyword in MySQL?**

   The `DISTINCT` keyword is used to return only distinct (different) values in a column or set of columns.

   **Example:**
   ```sql
   SELECT DISTINCT Department FROM Employees;
   ```

---

### 96. **What is a `Temporary Table` in MySQL?**

   A `Temporary Table` is a table that is created and exists only for the duration of a session. It is automatically dropped when the session ends.

   **Example:**
   ```sql
   CREATE TEMPORARY TABLE TempEmployees (
       EmployeeID INT,
       EmployeeName VARCHAR(100)
   );
   ```

   - To drop the temporary table:
   ```sql
   DROP TEMPORARY TABLE TempEmployees;
   ```

---

### 97. **What is the `ALTER TABLE` command in MySQL?**

   The `ALTER TABLE` command is used to modify an existing table, such as adding, deleting, or modifying columns or indexes.

   **Example 1: Add a new column:**
   ```sql
   ALTER TABLE Employees ADD COLUMN Email VARCHAR(100);
   ```

   **Example 2: Modify a column:**
   ```sql
   ALTER TABLE Employees MODIFY COLUMN Salary DECIMAL(10,2);
   ```

---

### 98. **What are `Transaction Isolation Levels` in MySQL?**

   Transaction isolation levels define the degree to which a transaction is isolated from other concurrent transactions. The levels are:
   - **READ UNCOMMITTED**: Allows dirty reads.
   - **READ COMMITTED**: Prevents dirty reads but allows non-repeatable reads.
   - **REPEATABLE READ**: Prevents dirty reads and non-repeatable reads.
   - **SERIALIZABLE**: Prevents dirty reads, non-repeatable reads, and phantom reads.

   **Example:**
   ```sql
   SET TRANSACTION ISOLATION LEVEL REPEATABLE READ;
   ```

---

### 99. **What is the `CONCAT()` function in MySQL?**

   The `CONCAT()` function is used to concatenate two or more strings into one.

   **Example:**
   ```sql
   SELECT CONCAT(EmployeeName, ' from ', Department) AS EmployeeDetails
   FROM Employees;
   ```

---

### 100. **What is the difference between `INNER JOIN` and `OUTER JOIN` in MySQL?**

   - **INNER JOIN**: Returns only the rows where there is a match in both tables.
   - **OUTER JOIN**: Returns all rows from one table and the matched rows from the other table. If no match is found, `NULL` values are returned for the columns from the table without a match.

   **Example of `INNER JOIN`:**
   ```sql
   SELECT Employees.EmployeeName, Departments.DepartmentName
   FROM Employees
   INNER JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID;
   ```

   **Example of `LEFT OUTER JOIN`:**
   ```sql
   SELECT Employees.EmployeeName, Departments.DepartmentName
   FROM Employees
   LEFT OUTER JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID;
   ```

---

### 101. **What is a `Self Join` in MySQL?**

   A `Self Join` is when a table is joined with itself, typically used to find relationships between rows in the same table.

   **Example:**
   ```sql
   SELECT e1.EmployeeName AS Employee, e2.EmployeeName AS Manager
   FROM Employees e1
   LEFT JOIN Employees e2 ON e1.ManagerID = e2.EmployeeID;
   ```

---

### 102. **What is a `Unique Key` in MySQL?**

   A `Unique Key` constraint ensures that all values in a column are distinct. Unlike the `PRIMARY KEY`, a `UNIQUE` key allows `NULL` values.

   **Example:**
   ```sql
   CREATE TABLE Users (
       UserID INT PRIMARY KEY,
       Email VARCHAR(100) UNIQUE
   );
   ```

---

### 103. **What are `User Defined Functions (UDFs)` in MySQL?**

   A **User Defined Function (UDF)** is a custom function that you can define and use in queries to extend the functionality of MySQL.

   - You must write UDFs in a compiled language like C and load them into MySQL.

   **Example (Conceptual)**:
   ```sql
   CREATE FUNCTION MyFunction RETURNS INT
   BEGIN
       -- Function logic here
   END;
   ```

---

### 104. **What are `Prepared Statements` in MySQL?**

   A `Prepared Statement` is a feature used to execute the same SQL query repeatedly with high efficiency. The statement is compiled once and executed multiple times with different parameters.

   **Example:**
   ```sql
   PREPARE stmt FROM 'SELECT * FROM Employees WHERE Department = ?';
   SET @department = 'HR';
   EXECUTE stmt USING @department;
   DEALLOCATE PREPARE stmt;
   ```

---

### 105. **What is a `Clustered Index` in MySQL?**

   A **Clustered Index** is a type of index where the data rows are stored in the same order as the index. The table data is sorted according to the clustered index.

   - In MySQL, a **PRIMARY KEY** is a clustered index by default.

   **Example:**
   ```sql
   CREATE TABLE Employees (
       EmployeeID INT PRIMARY KEY,
       EmployeeName VARCHAR(100)
   );
   ```
   - Here, the `PRIMARY KEY` creates a clustered index on the `EmployeeID` column.

---

### 106. **What is the `RANK()` function in MySQL?**

   The `RANK()` function assigns a rank to each row within a partition of a result set. Rows with the same values receive the same rank, and gaps are left in the ranking for duplicate values.

   **Example:**
   ```sql
   SELECT EmployeeName, Salary, RANK() OVER (ORDER BY Salary DESC) AS Rank
   FROM Employees;
   ```

---

### 107. **What is the `LEAD()` function in MySQL?**

   The `LEAD()` function allows you to access data from the next row in the result set.

   **Example:**
   ```sql
   SELECT EmployeeName, Salary, LEAD(Salary) OVER (ORDER BY Salary DESC) AS NextSalary
   FROM Employees;
   ```

---

### 108. **What is `Multi-Table Update` in MySQL?**

   In MySQL, you can update multiple tables in a single query using a `JOIN`.

   **Example:**
   ```sql
   UPDATE Employees e
   JOIN Departments d ON e.DepartmentID = d.DepartmentID
   SET e.Salary = e.Salary * 1.1
   WHERE d.DepartmentName = 'HR';
   ```

---

Let me know if you'd like more details on any of these topics or additional examples!
