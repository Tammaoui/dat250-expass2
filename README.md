# DAT250: Experiment Assignment 2.

- [X]  Experiment 1: Application using JPA
- [ ]  Experiment 2: Banking/Credit Card example JPA

## Experiment 1: Application using JPA
I started with cloning the maven projec and changed the connection string to the following:

`                      
<property name="javax.persistence.jdbc.url" value="jdbc:derby:C:\Source\assignment2\todoDb;create=true"/>
`

I then installed derby database, and began with step 4.3 in the tutorial.

By doing so, I created a couple of todo items in the database. I edited the todo description to include my name, and summary to include my lastname. 

`todo.setSummary("This is a test by Ayoub");`


`todo.setDescription("Tammaoui");`

These were created by running the Main class:
![bilde](https://user-images.githubusercontent.com/44643583/132558975-6de346c8-18d5-428b-b7c1-a85f6cab5bfb.png)

I managed to visualize them in Intellij by connecting to the derby database (using my new connection string) and executing the SQL query:

`select * from TODO`

Screenshot of the generated database tables. Also the rows in the table.
![bilde](https://user-images.githubusercontent.com/44643583/132559187-2548a0ed-d82a-48ac-ac85-67b591653ae9.png)

## Experiment 2: Banking/Credit Card example JPA

