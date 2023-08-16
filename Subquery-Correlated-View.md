# Sub Queries
## Where Clauses same table
### List out all the employees with age >  25
```select * from Customers where age IN (select age from Customers where age > 25);```

## Where clause Different table
### Emp details working in more than 2 item
```select * from Customers where customer_id IN (select customer_id from Orders group by customer_id having count(customer_id) > 1);``` 

## Single value subquery
### emp details having age > average age
```select * from Customers where age > (select avg(age) from Customers);```


## From claues -- Derived tables
### select max age person whose first name contains 'J'
```select max(age) from (select * from Customers where first_name LIKE '%J%') AS temp;```

# Corelated Query
## find 3rd oldest Employee
```select * from Customers as c1 where 3 = (select COUNT(c2.age) from Customers as c2 where c2.age >= c1.age);```

# VIEW
``` select * from Customers;```

## Create View 
 ```create view custom_view_exist AS select first_name, age from Customers;```

## Viewing a view
```select * from custom_view_exist;```

## ALTERING THE VIEW
```ALTER VIEW custom_view_exist AS select first_name, last_name , age from Customers;```

## DROPING a View
```DROP VIEW IF EXISTS custom_view_exist;```
