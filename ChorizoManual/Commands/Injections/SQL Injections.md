Examples 

SQL injection can be used for far more than reading the data of a single of user. The following are just a few examples of data a hacker could input to a form field (or anywhere user input is accepted) in an attempt to exploit a SQL injection vulnerability: 

- Smith' OR '1' = '1 results in SELECT * FROM users WHERE name = 'Smith' OR TRUE; which will return all entries from the users table 
    
- Smith' OR 1 = 1; -- results in SELECT * FROM users WHERE name = 'Smith' OR TRUE;--'; which, like the first example, will also return all entries from the users table 
    
- Smith'; DROP TABLE users; TRUNCATE audit_log; -- chains multiple SQL-Commands in order to both DROP the users table and delete all entries from the audit_log table 
    

Ex. Can also run: 
User or 1=1 
'or 1=1 --   (This is to get the rest of the data if concatenated) 
tom' AND substring(password, 1,1) = 'a