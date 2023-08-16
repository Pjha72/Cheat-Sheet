## SET OPERATORS
### List out all the employees in the company
#### UNION
``` select * from Dept1 UNION select * from Dept2;```

### List out all the employees in all departments who works as salesman
``` select * from Dept1 where role = "salesman" UNION select * from Dept2 where role  = "salesman";```

### Intersection
##### list out all the employees who work for both the departments
``` select Dept1.* from Dept1 INNER JOIN Dept2 using(empid);```

#### MINUS
##### List out all the employees working in dept1 but not in dept2
``` select Dept1.* from Dept1 LEFT JOIN Dept2 using(empid) where Dept2.empid IS NULL;```

