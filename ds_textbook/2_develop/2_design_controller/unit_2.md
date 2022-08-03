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
There are two steps in processing your data for insertion.
- Cleaning the data
- Inserting the data into your database

### Cleaning the data
> Data cleaning is the process of ensuring that your data is correct, consistent and usable.{cite}`gimenez_2020_6`

To clean the data you need to have a close look at the data you have been provided, and identify possible problems with the data. To fix the data manually is not feasible, once the dataset becomes sufficiently large, so you will need to work out an algorithm, which identifies problems and then corrects the data ready for insertion into the database.

Possible errors include:
- unnecessary leading or trailing spaces
- duplicate entries
- incorrect capitalisation
- inconsistent values (eg. NA, n/a, not applicable)
- missing data
- formatting of values (eg date format)
- merging or splitting values (eg. name column split into FirstName and LastName)

Your cleaning algorithm will depend on the errors you identify and it is recommended that it is written as a separate function, as it will be called for each line of data that you need to insert

```
BEGIN clean_data (data)

clean_data = []

id = data[0]
first_name = data[1] STRIPSPACE CAPITALISE
last_name = data[2] STRIPSPACE CAPITALISE
name = first_name + last_name
dob = data[3] REPLACE "-" WITH "/"

RETURN [id, name, dob]

END
```

### Inserting data into
Once the data has been cleaned, it need to be inserted into your database. This can get quite tricky, as Unit 2 data will be provided in a flat file database, and you will need to parse it into a relational database. Why is this tricky? Well each row of the flat file data source may contain multiple database tables, or a single database table my be provided over several rows in the flat file data source.

Your application will read the source data one row at a time, and you will need to assemble the data into the appropriate tables for your database.


## Manipulating data 


## Displaying retrieved data
