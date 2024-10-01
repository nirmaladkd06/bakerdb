Here’s an explanation of your tables and their relationships for the Bakery Management System:

1. **Products Table**
Purpose: This table holds information about the various products offered by the bakery.<br>
Key Columns:<br>
productid: A unique identifier for each product.<br>
productname: The name of the product (e.g., "Chocolate Cake").<br>
category: The type of product (e.g., "Pastry", "Bread").<br>
price: The selling price of the product.<br>
stockquantity: The number of items available in stock.<br><br>
2.**Customers Table**<br><br>
 Purpose: This table stores information about customers who purchase products from the bakery.<br>
Key Columns:<br>
customerid: A unique identifier for each customer.<br>
firstname: The customer's first name.<br>
lastname: The customer's last name.<br>
email: The customer's email address (unique for each customer).<br>
phonenumber: The customer's contact number.<br>
address: The customer's delivery or billing address.<br><br>
3.**Orders Table**<br><br>
Purpose: This table manages the orders placed by customers.<br>
Key Columns:<br>
orderid: A unique identifier for each order.<br>
customerid: A reference to the customer who placed the order, linking to the Customers table.<br>
orderdate: The date and time when the order was placed.<br>
totalamount: The total cost of the order.<br><br>
4. **Order Details Table**<br><br>
Purpose: This table links products to specific orders, providing detailed information about what was purchased.<br>
Key Columns:<br>
orderdetail_id: A unique identifier for each order detail entry.<br>
orderid: A reference to the order this detail is associated with, linking to the Orders table.<br>
productid: A reference to the product being purchased, linking to the Products table.<br>
quantity: The number of units of the product ordered.<br>
price: The price of the product at the time of the order (in case of price changes later).<br><br>
5. **Bakery Details Table**<br><br>
Purpose: This table provides additional information relevant to bakery operations and can link customers, products, and orders for operational insights.<br>
Key Columns:<br>
customerid: A reference to the customer, linking to the Customers table.<br>
productid: A reference to the product, linking to the Products table.<br>
orderid: A reference to the order, linking to the Orders table.<br>
orderdetail_id: A reference to the order detail, linking to the Order Details table.<br><br>
Relationships Between Tables<br><br>
Customers and Orders: Each customer can place multiple orders, establishing a one-to-many relationship between Customers and Orders.
Orders and Order Details: Each order can contain multiple products, creating a one-to-many relationship between Orders and Order Details.
Products and Order Details: Each order detail refers to a specific product, establishing a many-to-one relationship from Order Details to Products.

<br><br>
Bakery Details links the three main entities (Customers, Products, Orders), allowing for comprehensive tracking of orders and customer interactions with products.
T
