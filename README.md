# buildyourproperty
# 🏗️ BuildYourProperty Backend

## 📌 Project Overview

**BuildYourProperty** is a Spring Boot backend application that connects **users (customers)** with **contractors** for property-related services like construction, maintenance, and bookings.

The system allows:

* Users to register and log in
* Contractors to be managed
* Users to create bookings with contractors
* Secure communication using JWT authentication

---

## 🚀 Tech Stack

* Java 17+
* Spring Boot
* Spring Security
* JWT (JSON Web Token)
* Spring Data JPA
* MySQL
* Maven

---

## 📂 Project Structure

```bash
com.BuildYourProperty
│
├── config          # Security & CORS configuration
├── controller      # REST Controllers (User, Contractor, Booking)
├── dto             # Request DTOs
├── entity          # Database Entities
├── exception       # Global Exception Handling
├── payload         # Login Request & Response
├── repository      # JPA Repositories
├── security        # JWT Utility & Filter
├── service         # Business Logic Layer
```

---

## 🔐 Security Implementation

* JWT-based Authentication
* Custom JWT Filter (`JwtFilter`)
* Role-based access (extendable)
* Password encryption (Spring Security)
* Secured endpoints (except login/register)

---

## 👥 Modules

### 1️⃣ User Module

* Register user
* Login user
* JWT token generation

### 2️⃣ Contractor Module

* Add contractor
* View contractors
* Manage contractor details

### 3️⃣ Booking Module

* Create booking between user & contractor
* View bookings
* Manage booking data

---

## ⚙️ Setup Instructions

### 1️⃣ Extract & Open Project

* Unzip the project
* Open in IntelliJ IDEA / Eclipse

---

### 2️⃣ Configure Database

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/buildyourproperty
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

### 3️⃣ Add Required Dependencies

Make sure your `pom.xml` includes:

* Spring Web
* Spring Data JPA
* Spring Security
* MySQL Driver
* Validation
* JWT (jjwt)

---

### 4️⃣ Run Application

```bash
mvn spring-boot:run
```

App runs on:

```
http://localhost:8080
```

---

## 🔑 Authentication APIs

### 📌 Register

```
POST /users/register
```

### 📌 Login

```
POST /users/login
```

Response:

```json
{
  "token": "JWT_TOKEN"
}
```

---

## 🔒 How to Use JWT

For secured APIs, add header:

```
Authorization: Bearer YOUR_TOKEN
```

---

## 📌 Example APIs

### 👤 User APIs

* Register User
* Login User

### 👷 Contractor APIs

* Add Contractor
* Get All Contractors

### 📅 Booking APIs

* Create Booking
* Get Bookings

---

## ⚠️ Important Notes

* No Lombok is used (manual getters/setters)
* JWT secret is hardcoded (should be moved to environment variables)
* Basic security implemented (can be enhanced with roles & permissions)

---

## 🔮 Future Enhancements

* Role-based authorization (Admin / Customer / Contractor)
* Project posting system
* Contractor bidding system
* Chat system
* Ratings & reviews
* Payment integration

---

## 👨‍💻 Author

Vaishnavi Hajare

---

## ⭐ Contribution

Feel free to improve this project and add new features.

---

## 📜 License

This project is for learning and development purposes.
