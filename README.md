
-- Task 1: change the points to reads times by 10 and plus 100
USE sql_store;
select last_name, first_name,points, (points*10)+100
from customers;

-- create a discount factor so the table now shows a discount header and changing the (point + 10) *100
USE sql_store;
select last_name, first_name, points, (points+10)*100
from customers;

-- Task 2: Show columns; name, unit price, and new column called new price which is based on this expression, (unit price * 1.1 ).
USE sql_store;
select name, unit_price, (unit_price * 1.1) As new_price
from products;

-- Task 3: create a new query to find all the customers with a birth date > '1990-01-01'
USE sql_store;
Select * 
from customers 
where birth_date > '1990-01-01';

-- Task 4: Find out the name of the product with most amount in stock.
USE sql_inventory;
select  name, (quantity_in_stock * unit_price) As amount
 from products 
 order by amount DESC
 limit 1;
 
 -- Task 5: Find out the name of the most expensive product
 USE sql_inventory;
 select name
 from products
 order by unit_price DESC
 limit 1;
 
 -- Task 6: Find out the first name, last name, address and the birthdate of the oldest customer.
USE sql_store ;
Select first_name, last_name, address, birth_date
from customers
order by birth_date
limit 1;
