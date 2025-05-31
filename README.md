# Ghada Shopping Cart Service

This is a RESTful Shopping Cart Service developed by **Ghada Alotaibi** using Java 21 and Spring Boot with PostgreSQL.

## Features

-  List products
-  Search products by ID or keyword
-  View product details
-  Add product to shopping cart
-  Remove product from cart
-  Show shopping cart
-  Empty shopping cart
-  Pay for shopping cart (including tax)

## Technical Stack

- Java 21
- Spring Boot (without Spring Data)
- JPA (EntityManager-based)
- PostgreSQL
- Maven
- No Lombok
- Embedded Tomcat

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST   | `/api/cart` | Create new cart |
| POST   | `/api/cart/{cartId}/add/{productId}` | Add product to cart |
| DELETE | `/api/cart/{cartId}/remove/{productId}` | Remove product |
| DELETE | `/api/cart/{cartId}/empty` | Empty cart |
| GET    | `/api/cart/{cartId}/pay` | Pay and get total |
| GET    | `/api/products` | List all products |
| GET    | `/api/products/search?keyword=...` | Search products |
| GET    | `/api/product/{id}` | Show product details |

## Assumptions

- No authentication is needed.
- Products have a static tax.
- Cart is tied to ID only (no users).
- Data is inserted manually or via SQL script.

## Setup

1. Clone the repo.
2. Create PostgreSQL DB named `ShoppingCartDB`.
3. Run the app.
4. Test using Postman.

---

## Ready for Deployment 

Ensure PostgreSQL is running on port `5432` with user `postgres` and no password.

> Created by **Ghada Alotaibi**
