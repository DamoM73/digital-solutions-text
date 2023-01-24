# Unit 2: Evaluate Components

## Evaluate data quality

### Accuracy

> Data accuracy is, as its sounds, whether or not given values are correct and consistent. The two most important characteristics of this are form and content, and a data set must be correct in both fields to be accurate {cite}`partida_2021_what`.

#### Form

Do the same fields sort data in the same format. For example:

- Do all the fields storing currency have the same number of decimal places?
- Are all you dates stored in the same format (DD?MM/YYYY or DD/MM/YY or MM/DD/YYYY or YYYY/MM/DD etc.)?

#### Content

Does each field store the same type of data. This is an essential requirement for 1NF. So if your database is in 1NF, then field content should be the same.

### Completeness

Data completeness refers to the comprehensiveness or wholeness of the data. There should be no gaps or missing information for data to be truly complete.

For data to be complete all the required data needs to be gathered and stored properly.

Evidence that data is complete:

- the database is in 3NF
- all necessary fields are required
- referential integrity is reinforced through the PK / FK connection
- data is written to the database before program exits
- database is backed up