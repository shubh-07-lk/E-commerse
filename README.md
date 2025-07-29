

# 🛒 E-Commerce Application (Spring Boot Backend)

This is a backend RESTful API for an E-Commerce application built using **Spring Boot**. It provides endpoints for user authentication, product management, cart handling, and order placement — forming the core of a scalable and modular online shopping platform.

---

## 🚀 Features

- 🔐 User Registration & Authentication (JWT-based)
- 📦 Product CRUD (Create, Read, Update, Delete)
- 🛍️ Add to Cart / View Cart / Remove from Cart
- 🧾 Order Placement
- 🧑‍💼 Role-Based Access (User/Admin)
- 📄 Category Management
- 💬 RESTful API with structured JSON responses

---

## 🛠️ Tech Stack

| Layer        | Technology            |
|-------------|------------------------|
| Backend      | Spring Boot, Spring Security |
| Build Tool   | Maven                  |
| Database     | MySQL                  |
| ORM          | Hibernate (JPA)        |
| Authentication | JWT (JSON Web Tokens) |
| Language     | Java 17+               |

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/shubh-07-lk/E-commerse.git
cd E-commerse
```

### 2. Set Up MySQL Database

```sql
CREATE DATABASE ecommerce;
```

### 3. Configure `application.properties`

In `src/main/resources/application.properties`, update:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
spring.datasource.username=your_mysql_user
spring.datasource.password=your_mysql_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
server.port=8080
```

---

### 4. Build and Run the Application

```bash
./mvnw spring-boot:run
```

Or:

```bash
mvn clean install
java -jar target/*.jar
```

---

## 📬 API Endpoints Overview

### 🔐 Authentication

| Method | Endpoint         | Description       |
|--------|------------------|-------------------|
| POST   | `/register`      | User registration |
| POST   | `/login`         | User login (JWT)  |

### 📦 Products

| Method | Endpoint        | Description             |
|--------|-----------------|-------------------------|
| GET    | `/products`     | View all products       |
| POST   | `/products`     | Add a new product (Admin)|
| PUT    | `/products/{id}`| Update product (Admin)  |
| DELETE | `/products/{id}`| Delete product (Admin)  |

### 🛒 Cart & Orders

| Method | Endpoint        | Description       |
|--------|-----------------|-------------------|
| POST   | `/cart/{id}`    | Add to cart       |
| GET    | `/cart`         | View cart         |
| DELETE | `/cart/{id}`    | Remove from cart  |
| POST   | `/order`        | Place order       |

> Full Postman collection available upon request.

---

## 📁 Project Structure

```
src/
├── main/
│   ├── java/com/shubham/ecommerce/
│   │   ├── controller/
│   │   ├── model/
│   │   ├── repository/
│   │   ├── service/
│   │   ├── config/
│   │   └── EcommerceApplication.java
│   └── resources/
│       ├── application.properties
│       └── static/
```

---

## 📌 Future Enhancements

- Frontend using React or Angular
- Payment Gateway Integration
- Email Notifications
- Docker Deployment
- Swagger Documentation

---

## 🙋‍♂️ Maintained by

**Shubham Kalashetty**

Connect with me on [LinkedIn]([https://www.linkedin.com/](https://www.linkedin.com/in/shubham-kalashetty-b02941272/))

---

## 📝 License

This project is open-source and free to use under the [MIT License](LICENSE).
