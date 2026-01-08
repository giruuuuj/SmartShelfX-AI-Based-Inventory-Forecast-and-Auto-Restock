
# 🚀 SmartShelf: AI-Powered Inventory Management System

**SmartShelf** is a secure, role-based platform designed to optimize retail inventory management.  
It uses an **AI-powered forecasting module** to predict demand, automates the purchase order workflow, and provides **real-time sales reporting** and **critical stock alerts**.

---

## 🌟 Key Features

### 🔐 Role-Based Access Control (RBAC)
- Secure authentication and authorization using **JWT (JSON Web Tokens)**.  
- Roles: **ADMIN**, **STORE_MANAGER**, and **USER**.

### 📦 Product Management
- Full **CRUD** (Create, Read, Update, Delete) functionality for inventory items.

### 📊 Sales Reporting
- Dynamic, date-filtered **sales data visualization** (Revenue Trend Graph).  
- Accurate **Total Revenue** calculation.

### 📁 Data Export
- Export detailed sales reports to **Excel (.xlsx)**.

### 🤖 AI Demand Forecasting
- Predicts future stock needs using historical sales data.  
- Provides intelligent **restock suggestions**.

### ⚙️ Automated Restock Workflow
- Manages **Purchase Orders (PO)** through status transitions:
  ```
  PENDING → APPROVED → RECEIVED
  ```
- Automatically updates inventory levels upon receipt.

### 🚨 Critical Stock Alerts
- Real-time dashboard alerts for items below critical thresholds.

---

## 💻 Technology Stack

| Component | Technology | Description |
|------------|-------------|-------------|
| **Backend** | Java 17, Spring Boot 3 | Handles business logic, security (JWT), and REST API endpoints. |
| **Frontend** | React, JavaScript | Built with React Router, Material-UI (MUI) for UI/UX, and Recharts for visualization. |
| **Database** | MySQL / MariaDB | Persistent storage for all entities (Users, Products, Sales, POs, etc.). |
| **Security** | JSON Web Tokens (JWT) | Stateless authentication and token-based authorization. |

---

## 🛠️ Setup and Installation Guide

To run **SmartShelf** locally, you’ll need to set up the **Backend**, **Database**, and **Frontend** separately.

---

### 1️⃣ Database Setup (MySQL)

1. Ensure you have **MySQL** or **MariaDB** running.  
2. Create a new database named:
   ```sql
   CREATE DATABASE smartshelf_db;
   ```
3. The Spring Boot application will automatically create all necessary tables (`users`, `products`, `sales`, `purchase_orders`, etc.) via Hibernate/JPA.

---

### 2️⃣ Backend Setup (Spring Boot)

1. Navigate to the backend directory:
   ```bash
   cd smartshelf-backend/
   ```

2. Configure **application.properties**:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/smartshelf_db
   spring.datasource.username=your_db_username
   spring.datasource.password=your_db_password
   spring.jpa.hibernate.ddl-auto=update
   ```

   *(Optional) Configure JWT secrets if necessary.*

3. Run the application:
   ```bash
   ./mvnw spring-boot:run
   ```

   The backend should start on:  
   👉 http://localhost:8080

---

### 3️⃣ Frontend Setup (React)

1. Navigate to the frontend directory:
   ```bash
   cd smartshelf-frontend/
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

   If you face dependency issues (e.g., with `jspdf-autotable`), try:
   ```bash
   npm install --force
   ```

3. Run the frontend:
   ```bash
   npm start
   ```

   The application will open in your browser at:  
   👉 http://localhost:3000

---

## 🔑 Default Credentials

For initial testing, use the following default users (ensure they are seeded manually or via API):

| Role | Username | Password | Access Level |
|------|-----------|-----------|---------------|
| **ADMIN** | admin | password | Full Control, User Management |
| **MANAGER** | manager | password | Product CRUD, AI, Reports, Restock |
| **USER** | user | password | Shopping / Viewing |

---



<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a72bf562-1062-4a67-b8d7-5bd706ee2cfb" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/095f9d2e-4040-49fd-b426-fb6057310b3a" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/3fa4f6ec-a915-44e8-b282-2fc00fcf9966" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/2f537e42-0f4b-4283-bc76-03cf6caca9d4" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/ae970e7c-2031-4797-b309-0d816727008e" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/35fc9e16-e5da-4c3f-80a0-124e0f343e6d" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/1a04f22a-1bf8-4826-860c-c528a50932d7" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/357d5395-6768-456d-bb3c-5fe580d9c7d4" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/bb9d5728-d392-417d-b80a-20b15f391621" />
[Inventory-Management-System SmartShelfX.pptx](https://github.com/user-attachments/files/24484700/Inventory-Management-System.SmartShelfX.pptx)




