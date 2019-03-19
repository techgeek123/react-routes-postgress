# postgres Advanced topics

## Release 0: Trigger
- You have to create a trigger in postgresql
- You have to create a function and call it in the trigger
- You have to create two dummy tables LivesIn(pid, name, province) and Places(name, province, population, mayorid)

- Now question is in terms of code. I'll have some wrong SQL code for you

```
CREATE TRIGGER updatePopulation
AFTER INSERT ON LivesIn
FOR EACH ROW  
UPDATE Places
SET NEW.population = OLD.Population + 1
WHERE LivesIn.name = Places.name AND LiveIn.province = Places.province;
```

- Understand what is he is trying to do & fix his SQL Query so that it works


## Release1: Indexing

- Create a `salary_index` on Company salary
- You can download the company.sql db from the root of `code-blocks` directory
- To browse the db from SQL data you can use [DB Browser for SQLite](http://sqlitebrowser.org)

## Release2: Transactions

- Pick the same company.sql database
- Start a transaction and delete records from the table having age = 25 and finally we use ROLLBACK command to undo all the changes
- Now, let us start another transaction and delete records from the table having age = 25 and finally we use COMMIT command to commit all the changes
- What's the final output of table?

## Release3: DeadLocks Exploration

- Check this question on stackoverflow and see if you understand [it](https://stackoverflow.com/questions/18297478/deadlock-in-postgres-on-simple-update-query)
- Create a deadlock situation with `company.sql` database we have provided
