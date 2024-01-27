# INSTRUCTOR TABLE
## CREATE, INSERT, UPDATE AND DELETE INSTRUCTOR TABLE 
```sql

---Create a table called Instructor
DROP TABLE IF EXISTS Instructor;
CREATE TABLE Instructor(
Ins_id INT IDENTITY(1,1) NOT NULL,
lastname NVARCHAR(20),
firstname NVARCHAR(20) NOT NULL,
city NVARCHAR(20),
country NVARCHAR(2)
);

---Insert records into Instructor
INSERT INTO Instructor
VALUES('Abobi','Gavi','Accra','GH'),
      ('Ahuja','Rev','Toronto','CA'),
	  ('Chong','Raul','Toronto','CA'),
	  ('Vasudevan','Hima','Chicago','US');

/* Insert a new instructor record with id 5 for Sandip Saha who lives 
in Edmonton, CA into the 'Instructor' table*/
INSERT INTO Instructor
VALUES('Sandip','Saha','Edmonton','CA');

/* Insert two instructor records. first record with id 6 for John Doe who lives 
in Sydney, AU. Second record with id 7 for Jane Doe who lives in Dhaka,BD */
INSERT INTO Instructor 
VALUES('John','Doe','Sydney','AU'),
	  ('Jane','Doe','Dhaka','BD');

/* Insert two new records. first record with id 8 for Steve Ryan who lives 
in Barly, GB. Second record with id 9 for Ramesh Sannareddy who lives in Hyderabad,IN */
INSERT INTO Instructor
VALUES('Steve','Ryan','Barly','GB'),
      ('Ramesh','Sannareddy','Hyderabad','IN');

--Update the city for Sandip to Toronto
UPDATE Instructor
SET city = 'Toronto'
WHERE lastname = 'Sandip';

--Update the city and country for Doe with id 6 to Dubai and AE
UPDATE Instructor
SET city = 'Dubai', country = 'AE'
WHERE firstname = 'Doe' AND Ins_id = 6;

--Update the city of the instructor record to Markham whose id is 1
UPDATE Instructor
SET city = 'Markham'
WHERE Ins_id = 1;

--Update the city and country for Sandip with Id 5 to Dhaka and BD respectively
UPDATE Instructor
SET city = 'Dhaka',country = 'BD'
WHERE Ins_id = 5;

--Remove the instrutor record of Doe whose Id is 7
DELETE FROM Instructor
WHERE Ins_id = 7;

```

