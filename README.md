E-Commerce REST API – Spring Boot

 Project Overview

This project is a Spring Boot-based REST API application that provides Customer Management, Product Management, and Shopping Cart Management functionalities.

The application performs CRUD operations and follows RESTful API principles to manage customers, products, and shopping carts.

 Technologies Used

- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- REST APIs
- Postman

 Project Modules

1. Customer Management APIs

HTTP Method| Endpoint| Description
POST| "/api/customers/register"| Register Customer
GET| "/api/customers"| Get All Customers
GET| "/api/customers/{id}"| Get Customer By ID
PUT| "/api/customers/{id}"| Update Customer
DELETE| "/api/customers/{id}"| Delete Customer

Customer Validation Rules:

- Email must be unique.
- Mobile number must contain exactly 10 digits.
- Customer name cannot be blank.

2. Product Management APIs

HTTP Method| Endpoint| Description
POST| "/api/products"| Add Product
GET| "/api/products"| Get All Products
GET| "/api/products/{id}"| Get Product By ID
PUT| "/api/products/{id}"| Update Product
DELETE| "/api/products/{id}"| Delete Product
GET| "/api/products/category/{category}"| Get Products By Category

Product Validation Rules:

- Product price must be greater than zero.
- Product quantity cannot be negative.
- Product name is mandatory.
- Implement product search by name.

3. Shopping Cart Management APIs

HTTP Method| Endpoint| Description
POST| "/api/cart/add?customerId={customerId}&productId={productId}"| Add Product To Cart
GET| "/api/cart/{customerId}"| View Customer Cart
PUT| "/api/cart/update?customerId={customerId}&productId={productId}"| Update Cart Quantity
DELETE| "/api/cart/remove?customerId={customerId}&productId={productId}"| Remove Product From Cart
DELETE| "/api/cart/clear/{customerId}"| Clear Entire Cart

📋 Business Rules

- A customer can have only one active cart.

- If a product is added again, its quantity must be updated in the existing cart item.

- Requested quantity cannot exceed available product stock.

- Cart item price must be fetched from the product database.

- Cart total must be calculated as:
  
  "Total Price = Product Price × Quantity"

 Installation & Setup

Step 1: Clone Repository

git clone YOUR_REPOSITORY_URL

Step 2: Navigate to Project

cd YOUR_PROJECT_NAME

Step 3: Configure Database

Update your "application.properties" file with your database credentials.

Step 4: Install Dependencies

mvn clean install

Step 5: Run Application

mvn spring-boot:run

Application URL:

"http://localhost:8080"

 API Testing

All REST APIs can be tested using Postman or Thunder Client.

Test the following functionalities:

- Customer Registration and Management.
- Product Creation and Management.
- Product Search by Name.
- Product Filtering by Category.
- Adding Products to Cart.
- Updating Cart Quantity.
- Removing Products from Cart.
- Clearing Entire Cart.
- Cart Total Calculation.

 Project Objectives

- Understand RESTful API development using Spring Boot.
- Implement CRUD operations.
- Perform customer and product management.
- Implement shopping cart functionality.
- Apply business validation rules.
- Manage relationships between customers, products, and carts.
- Test REST APIs using Postman.

