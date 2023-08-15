## INNER JOIN
### Inlist all the customer id, names along with the amount allocated to there.
```select c.customer_id as ID, c.first_name as fname, o.amount as Am from Customers as c INNER JOIN Orders as o ON c.customer_id = o.customer_id;```

### Fetch out all the customer ID and their contact details who have been shipping status is pending with the customers working in Anytown
```select c.CustomerID as ID, c.Phone as Contact, s.status as Status from Cust as c INNER JOIN Shippings as s ON c.CustomerID = s.shipping_id WHERE s.status = "Pending" and c.City = "Anytown"; ```

## LEFT JOIN
### Fetch out each all amount allocated to the each customer
``` select * from Cust as c LEFT JOIN Orders as o ON o.customer_id = c.CustomerID;```

## RIGHT JOIN
### List out all the order item along with the customer name and their respective allocated email id
``` select o.item as Item, c.FirstName as fname, c.Email as email from Orders as o LEFT JOIN Cust as c ON o.customer_id = c.CustomerID;```

## CROSS JOIN
###List out all the combinations possible for the customer name and orders that can exist
``` select c.FirstName, c.LastName, o.customer_id, o.item from Cust as c CROSS JOIN Orders as o;```

### join Two table without join keyword
``` select c.customer_id as ID, c.first_name as fname, o.amount as Am from Customers as c , Orders as o Where c.customer_id = o.customer_id;```
