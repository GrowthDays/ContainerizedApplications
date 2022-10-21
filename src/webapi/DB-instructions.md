# DB

## Instructions


Please run the following SQL statements against your database server:

```sql
CREATE DATABASE user_db;
```

```sql
CREATE TABLE users (
  ID SERIAL PRIMARY KEY,
  name VARCHAR(30),
  email VARCHAR(30)
);
```

```sql
INSERT INTO users (name, email)
   VALUES ('Joe', 'joe@example.com'), 
          ('Ruby', 'ruby@example.com');
```
