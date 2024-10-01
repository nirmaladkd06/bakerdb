Here’s an explanation of your tables and their relationships for the Bakery Management System:

1. **Products Table**
Purpose: This table holds information about the various products offered by the bakery.
Key Columns:
productid: A unique identifier for each product.
productname: The name of the product (e.g., "Chocolate Cake").
category: The type of product (e.g., "Pastry", "Bread").
price: The selling price of the product.
stockquantity: The number of items available in stock.
2.**Customers Table**
 Purpose: This table stores information about customers who purchase products from the bakery.
Key Columns:
customerid: A unique identifier for each customer.
firstname: The customer's first name.
lastname: The customer's last name.
email: The customer's email address (unique for each customer).
phonenumber: The customer's contact number.
address: The customer's delivery or billing address.
3.**Orders Table**
Purpose: This table manages the orders placed by customers.
Key Columns:
orderid: A unique identifier for each order.
customerid: A reference to the customer who placed the order, linking to the Customers table.
orderdate: The date and time when the order was placed.
totalamount: The total cost of the order.
4. **Order Details Table**
Purpose: This table links products to specific orders, providing detailed information about what was purchased.
Key Columns:
orderdetail_id: A unique identifier for each order detail entry.
orderid: A reference to the order this detail is associated with, linking to the Orders table.
productid: A reference to the product being purchased, linking to the Products table.
quantity: The number of units of the product ordered.
price: The price of the product at the time of the order (in case of price changes later).
5. **Bakery Details Table**
Purpose: This table provides additional information relevant to bakery operations and can link customers, products, and orders for operational insights.
Key Columns:
customerid: A reference to the customer, linking to the Customers table.
productid: A reference to the product, linking to the Products table.
orderid: A reference to the order, linking to the Orders table.
orderdetail_id: A reference to the order detail, linking to the Order Details table.
Relationships Between Tables
Customers and Orders: Each customer can place multiple orders, establishing a one-to-many relationship between Customers and Orders.
Orders and Order Details: Each order can contain multiple products, creating a one-to-many relationship between Orders and Order Details.
Products and Order Details: Each order detail refers to a specific product, establishing a many-to-one relationship from Order Details to Products.
Bakery Details links the three main entities (Customers, Products, Orders), allowing for comprehensive tracking of orders and customer interactions with products.
T
