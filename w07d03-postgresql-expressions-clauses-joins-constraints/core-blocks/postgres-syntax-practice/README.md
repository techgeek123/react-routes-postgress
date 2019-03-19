# postgres Clauses & Joins

# Release 0:
- Below have a `COMPANY` Table insert it into the database

 id | name  | age | address   | salary | join_date
----|-------|-----|-----------|--------|----------
  1 | Paul  |  32 | California|  20000 | 2001-07-13
  3 | Teddy |  23 | Norway    |  20000 |
  4 | Mark  |  25 | Rich-Mond |  65000 | 2007-12-13
  5 | David |  27 | Texas     |  85000 | 2007-12-13
  2 | Allen |  25 | Texas     |        | 2007-12-13
  8 | Paul  |  24 | Houston   |  20000 | 2005-07-13
  9 | James |  44 | Norway    |   5000 | 2005-07-13
 10 | James |  45 | Texas     |   5000 | 2005-07-13

- Then you have another table called `DEPARTMENT`. Just create this table. It has the following definition: 

```
CREATE TABLE DEPARTMENT(
   ID INT PRIMARY KEY      NOT NULL,
   DEPT           CHAR(50) NOT NULL,
   EMP_ID         INT      NOT NULL
);
```

- Populate DEPARTMENT table −

```
(ID, DEPT, EMP_ID) -> (1, 'IT Billing', 1 );

(ID, DEPT, EMP_ID) -> (2, 'Engineering', 2 );

(ID, DEPT, EMP_ID) -> (3, 'Finance', 7 );
```

# Release1: 

Based on the above tables, we can write a CROSS JOIN as follows −

- Perform a `CROSS JOIN` that joins `EMP_ID, NAME, DEPT` from `COMPANY` with `DEPARTMENT` & get the output
- In `COMPANY` table return all the employees that have age greater than 27
- Return the `Union` of all employees name that are `Having` similar age group
- `Order` all the employees in table based on their age
- Return the name of all employees `WITH` state `Texas` in common
- There's a company party for senior employees so `LIMIT` all new employees based on their join date. Whosoever joined IN & AFTER 2007 should show up to party