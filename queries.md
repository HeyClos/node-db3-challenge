# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 77 records.
SELECT * FROM [Categories]

SELECT * FROM [Products]

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

SELECT OrderId, ShipperName, OrderDate from Orders
join Shippers
on Orders.ShipperId = Shippers.ShipperId
where OrderDate < "1997-01-09"

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

select OrderDetails.OrderID, OrderDetails.Quantity, Products.ProductName from [OrderDetails]
join Products on products.productID = orderDetails.productID
where OrderID = 10251
order by ProductName

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

select OrderID, CustomerName, LastName from [Orders]
join Customers on customers.CustomerID = orders.CustomerID
join Employees on employees.EmployeeID = orders.EmployeeID

### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 