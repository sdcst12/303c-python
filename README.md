## SDSS Computing Studies Python Assignment
### Assignment #xx (Total Marks xx)

Objectives:
* Define a table in a database
* Define a record in a table
* Determine the relation between a record and a row


Once we have a database with information in the tables, the next thing to do is search the database and pull out all relevant information. Sometimes we may want to search for specific items, or order them in a specific way. We may also want to limit the number of results if there are too many.




```
```
PRAGMA table_info(customers);
```
```
create table if not exists customers (
    id integer primary key autoincrement,
    name tinytext,
    email tinytext,
    cnum int);
```
```
select name from customers
select name,cnum from customers
select name from customers where cnum > 10
select name from customers order by name asc
select * from customers order by cnum desc
```
```
update customers set email='bassist@monkees.ca',cnum=80 where name='Peter Nesmith'
update customers set cnum=10 where email='miley@cyrus.com'
```
```
insert into customers (name,email,cnum) values ('Benjamin Tantalus','benjamin@tantalus.com',1000)
```
```
delete from customers where email='Miley Cyrus'
```

Assignment:

Create a program that will store the database for a veterinary
Each record needs to have the following information:
id unique integer identifier
pet name
pet species (cat, bird, dog, etc)
pet breed (persian, beagle, canary, etc)
owner name
owner phone number
owner email
owner balance (amount owing)
date of first visit

create a program that will allow the user to:
insert a new record into the database and save it automatically
retrieve a record by their id and display all of the information
retrieve a record by the email and display all of the information
retrieve a record by phone number and display all of the information

You will need to create the table yourself. Consider what data types you will
need to use.

