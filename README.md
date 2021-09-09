# DAT250: Experiment Assignment 2.

- [X]  Experiment 1: Application using JPA
- [X]  Experiment 2: Banking/Credit Card example JPA

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

### 1. Domain model
A domain model created of the java classes using Intellij. The model also shows the relations between the objects.
![bilde](https://user-images.githubusercontent.com/44643583/132565897-fc738aba-9801-4cc6-9d73-f094b98b5939.png)

### 2. Persist object into database. ChecK links are saved correctly
By viewing in the image below, we see the tables. 
![bilde](https://user-images.githubusercontent.com/44643583/132736141-f1a5b445-713f-4a5c-84a9-935f9e44bcb0.png)


By fetching the Person rows after having created them (created them similar to how the todo objects were created) and using Intellijs database UI to display them:
`select * FROM  PERSON`
![bilde](https://user-images.githubusercontent.com/44643583/132736360-db1f6c49-7cef-4f98-b044-9220e8b397ca.png)

We can also see it here that the links are saved correctly by inspecting the objects in the JPA structure in Intellij:
![bilde](https://user-images.githubusercontent.com/44643583/132736652-1ec19157-cfd8-43d5-9ddc-c9ed88795bc2.png)

Issues:
I managed to extend class Person with Address (by autoformatting with Intellij without being aware) and took me a lot of time to figure why the Person entity didnt
get created.
