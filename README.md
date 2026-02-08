# 🏋️ Personal Fitness Tracker System

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.7.18-green)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📖 About The Project
**Personal Fitness Tracker** is a comprehensive Java-based application designed to help users monitor their physical activities and health metrics. 

Unlike simple trackers, this system automates calorie calculations using **MET (Metabolic Equivalent of Task)** values based on specific workout types (Cardio vs. Strength) and user biometrics (Weight, Height, Age).

This project was developed as a coursework for **Astana IT University** (Course: Object-Oriented Programming).

---

## 🚀 Key Features
* **User Management (CRUD):** Complete lifecycle management for users with duplicate email detection.
* **Polymorphic Calorie Calculation:**
    * **Cardio:** Calculates based on duration, heart rate, and distance.
    * **Strength:** Calculates based on sets, reps, and weight lifted.
* **Advanced Analytics:**
    * Dynamic dashboard with real-time statistics.
    * Filtering workouts by calories burned (Java Stream API).
    * Sorting workouts by duration or difficulty.
* **Data Consistency:** Implemented complex Stream operations (grouping & flatMap) to detect data anomalies.
* **Interactive UI:** Responsive web interface using vanilla JavaScript (Fetch API) for asynchronous data updates without page reloads.

---

## 🛠️ Tech Stack

### Backend
* **Language:** Java 17 (Records, Pattern Matching)
* **Framework:** Spring Boot 2.7.18 (Web, Data JDBC)
* **Database:** PostgreSQL
* **Build Tool:** Apache Maven

### Frontend
* **Core:** HTML5, CSS3, JavaScript (ES6+)
* **Communication:** REST API (JSON) via Fetch API

### Architecture & Design
* **Pattern:** MVC (Model-View-Controller)
* **Database Access:** DAO Pattern with `JdbcTemplate` & `PreparedStatement`
* **Design Patterns:** Factory, Builder, Repository.
* **Principles:** SOLID, OOP (Inheritance, Polymorphism, Encapsulation).

---

## 📸 Screenshots

### 1. Interactive Dashboard
*Real-time overview of total users, workouts, and progress records.*
![Dashboard](screenshots/dashboard.png)
*(Note: Place your Dashboard screenshot here)*

### 2. User Management & CRUD
*Dynamic table with sorting and quick actions (Edit/Delete).*
![Users](screenshots/users.png)

### 3. API Testing
*REST endpoints verified via Postman and built-in API Console.*
![API](screenshots/api_test.png)

---

## ⚙️ Installation & Setup

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/your-username/fitness-tracker.git](https://github.com/your-username/fitness-tracker.git)
    cd fitness-tracker
    ```

2.  **Configure Database**
    * Create a PostgreSQL database named `postgres` (or update `application.properties`).
    * The system uses `data.sql` to initialize tables automatically.

3.  **Run the Application**
    ```bash
    mvn spring-boot:run
    ```

4.  **Access the App**
    * Open your browser and go to: `http://localhost:8080`

---

## 📂 Database Schema
The system uses a normalized relational schema (3NF):
* **`users`**: Stores profile data (Unique Email constraint).
* **`workouts`**: Uses **Single Table Inheritance** with a discriminator column for Cardio/Strength types.
* **`progress`**: Linked to users via Foreign Key (One-to-Many).

---

## 👨‍💻 Author
**Bekzat Abilkhayev**
* Group: SE-2501
* Astana IT University

---
*Thank you for visiting! If you find this project interesting, please give it a star ⭐.*
