# Unit 2: Develop Algorithms

For unit 2 we are concerned about the development of algorithms for the management of the data store. This process will have to occur after the development of the datastore.

Specifically we will need to create IPO tables for:
- Creating the database
- Processing data for insertion
- Manipulation of data
- Retrieval of data

## Creating database structure
You will need a algorithm to create each table of the database expressed in an IPO table.

The pseudocode for creating a table need to include the following details:
- Table name
- For each field
  - Name
  - Data type
- Indicate:
  - Primary key
  - Foreign key (including which primary key it references)

```
CREATE TABLE Teacher
    TeacherID INT PK
    Name TEXT
    Username TEXT
    Password TEXT

CREATE TABLE Subject
    SubjectID INT PK
    Name TEXT
    TeacherID INT FK Teacher.TeacherID

CREATE TABLE Student
    Student INT PK
    Name TEXT
    Username TEXT
    Password TEXT

CREATE TABLE Enrolment
    SubjectID INT PK FK Subject.SubjectID
    Student INT PK FK Student.StudentID
    RESULT TEXT
```

## Processes data for insertion
The data you will be dealing with in 

## Manipulating data 


## Displaying retrieved data
