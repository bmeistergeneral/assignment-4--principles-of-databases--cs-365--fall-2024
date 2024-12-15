# Fall 2024 Principles of Databases — Assignment 4

* **Do not start this project until you’ve read and understood these instructions. If something is not clear, ask.**

---

## ❖ Introduction ❖

For this assignment, you will write responses to nine questions based on different topics from our textbook, *Database Systems — The Complete Book* and to one question based on your notes. Reply to each question in the provided region using Markdown syntax.

---

## ❖ Questions ❖

### 1. [2.4] What is the difference between a Cartesian Product, a Natural Join, and Theta-Joins?

### A Cartesian Product results from joining every row in one table with every row from another table. The resulting Cartesian Product table will have m x n rows, and will produce all possible pairs of combinations of rows. This operation has no conditions or filters. A Natural Join is essentially an inner join that joins two tables for all columns that have the same name. It filters results based on where the values in the shared columns are equal, and implies that at least one attribute is shared. An NJ eliminates duplicate columns from the output, making it cleaner. A Theta Join is when tuples are combined based on a condition that involves comparison operators like less than, greater than, or equal to. When it's solely equal to it's an Equi Join. This allows combination criteria to be specifically defined, making it useful when dealing with relational databases. 

### 2. [2.5] What is a Referential Integrity Constraint?

### A Referential Integrity Constraint is what allows for tables to have a relationship to ensure accurate and consistent data. It can assist foreign keys in relating with primary keys for different tables. The purpose of it is to prevent invalid data by not using foreign keys that don't have a corresponding parent table entry, keep data valid and meaningful, and to control CRUD operations, mainly update and delete.

###  3. [2.5] What is a Key Constraint?

### A Key Constraint is what we know as primary, foreign, and unique keys within a relational database. A primary key keeps unique identifiers for each table record, and a foreign key establishes the link between two tables. A unique key ensures all column values are distinct and not repeated. A table can have only one primary key but can have multiple unique keys, and unique keys can contain null values.

### 4. [4.1] What is an Entity/Relationship Model? What purpose does it serve in the process of creating/designing databases?

### An entity/relationship model is a framework for representing/designing the structure of a database. It helps identify key entities, the relationships between them, and the attributes that characterize these entities. The ER model serves the purpose of conceptualizing data, can be a communication tool among database designers and administrators to discuss the data structure of it, can help the process of transforming from a conceptual framework into a logical model that can be used in a DBMS. It also allows for normalization that can refine the model and reduce data redundancy.

### 5. [4.4] What is a Weak Entity Set?

### A Weak Entity Set is an entity set in a relational database that can't be specifically identified by its own entity attributes alone, as it relies on the existence of other entities (parent entities) to provide a way to uniquely identify it. A weak entity has dependent participation and no primary key, has a relationship with its parent entity, and each instance of the weak entity is associated with an instance of the strong entity.

### 6. [5.2.7; 6.3.8] Explain the concepts of Outerjoin, Natural Right Outer Joins, Natural Left Outer Joins, and Full Outer Joins.

### An outer join is a type of join that retrieves records from two tables that include matched and unmatched records. It includes all rows even if there is no corresponding match in the other table. A Natural Right Outer Join is when all records from the right table are retrieved, as well as the matching records from the left table. If there are no matches, the values turn to NULL. A NLOJ is the opposite direction of a natural right outer join. In both cases, these are useful for when the dataset in the left or right tables specifically are more important. A full outer join is when it retrieves all records from both tables, matched and unmatched, with NULLs where matches do not exist.

### 7. [6.6.3] What is the difference between the SQL command `TRANSACTION` and the execution of any statement in SQL?

### The SQL command 'TRANSACTION' is different from the execution of any statement in SQL because it has a greater scope and encompasses multiple SQL statements, it ensures atomicity, either all operations are successful or none are done, it guarantees data integrity through the ACID properties, and it has functions for committing or rolling back the changes depending on success or failure.

### 8. [8] What is a Virtual View and what are its advantages?

### A virtual view is a versatile database object that can represent a query result without physically storing the data. Some of its advantages include simplified data access, meaning complex data can be accessed in a single table, enhanced security, meaning users can be restricted to view only the necessary data without viewing the underlying tables, data abstraction, meaning that user interaction is simplified by hiding database structure, query flexibility, meaning new virtual views can be created and modified without altering data structure, they can streamline query execution when designed appropriately, and concerns can be separated from either database design or business logic.

### 9. [8.3] What is an *index* and what are its advantages?

### An index is a data structure in a database that improves the speed of data retrieval operations on a table. It serves as a table that can be used to reduce how much data needs to be scanned when performing queries. An index contains keys that point to the physical locations of data. Different types of indexes include B-tree indexes, hash indexes, bitmap indexes, and clustered indexes. A b-tree index, or balanced tree, is the most efficient one that maintains sorted data and has efficient CRUD operations. A hash index maps keys to their locations and is used for equality comparisons, a bitmap index uses bit arrays for execution, and a clustered index is when the physical records in a table are rearranged to match the index order. The advantages of using an index are that the database engine finds data faster without having to search the entire table, there are less I/O operations, queries like where clauses benefit from the presence of indexes, and constraints are enforced as well as the fact that sorting is optimized.

### 10. Explain the concept of an MVC, or model, view, controller, framework for designing full stack applications

### The MVC framework is compromised of the Model, which represents the interface for the database and the management of data, as well as business logic which ensures data is processed according to the application requirements, and is independent of the user interface. The View is the presentation layer of the application, it generates UI and displays data according to what the Model defines it to be. The View sends user actions to the Controller, which acts as an intermediary between the Model and the View. The Controller handles input and determines what action to take based on user interactions with the View, it manages the flow of data between the Model and the View, and it maintains synchronization between the data and the UI. The MVC framework is a preferred framework among developers because of its enhanced testing abilities, it allows for separation between each component, and it allows for improved collaboration as well as reusability and flexibility.

---

## ❖ Due ❖

Sunday, 15 December 2024, at 10:00 AM.

---

## ❖ Grading ❖

| Item        | Points |
|-------------|:------:|
| Question 1  | `10`   |
| Question 2  | `10`   |
| Question 3  | `10`   |
| Question 4  | `10`   |
| Question 5  | `10`   |
| Question 6  | `10`   |
| Question 7  | `10`   |
| Question 8  | `10`   |
| Question 9  | `10`   |
| Question 10 | `10`   |

---

## ❖ Submission ❖

**NO late submissions will be accepted.**

You will need to issue a pull request back into the original repo, the one from which your fork was created for this project. See the **Issuing Pull Requests** section of [this site](http://code-warrior.github.io/tutorials/git/github/index.html) for help on how to submit your assignment.

**Note**: This assignment may **only** be submitted via GitHub. **No other form of submission will be accepted**.
