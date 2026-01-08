# 🚆 IRCTC Railway Reservation System (Backend)

A **high‑performance, pure backend railway reservation system** built with **Spring Boot**.  
This project simulates a real‑world ticketing engine using **In‑Memory Data Structures (Java Collections)** instead of a traditional database to demonstrate **algorithmic efficiency, thread safety, and solid OOP design**.

---

## 🚀 Key Features

⚡ **In‑Memory Data Storage**  
Uses optimized Java Collections (`HashMap`, `ArrayList`, `ConcurrentHashMap`) to eliminate database I/O latency.

🔒 **Concurrency Handling**  
Thread‑safe booking logic prevents **double booking** during simultaneous seat reservations.

🔑 **Role‑Based Access Control (RBAC)**  
Separate access for **Admin** (add trains, manage routes) and **User** (book tickets, check PNR), inspired by JWT concepts.

💸 **Dynamic Fare Calculation**  
Ticket pricing based on **seat type**, **distance**, and **availability** using clean OOP logic.

🎫 **PNR Generation & Status**  
Unique PNR generation with **O(1)** ticket lookup using HashMaps.

---

## 🛠️ Tech Stack

- **Language:** Java 17+  
- **Framework:** Spring Boot (Web, Security)  
- **Data Storage:** Java Collections (HashMap, ConcurrentHashMap, Lists)  
- **Build Tool:** Maven  
- **Testing:** JUnit  

---

## 🏗️ Architecture & Data Structures

| Entity       | Data Structure Used        | Reason |
|--------------|----------------------------|--------|
| Users        | HashMap<String, User>      | O(1) authentication & lookup |
| Trains       | ArrayList<Train>           | Fast iteration for search |
| Bookings     | HashMap<String, Ticket>    | O(1) PNR‑based retrieval |
| Seat Locking | synchronized blocks        | Prevents race conditions |

---

## 🔌 API Endpoints

### 1️⃣ Authentication

| Method | Endpoint | Description |
|------|---------|-------------|
| POST | /api/auth/register | Register user/admin |
| POST | /api/auth/login | Authenticate user |

### 2️⃣ Train Operations

| Method | Endpoint | Description |
|------|---------|-------------|
| GET | /api/trains/search?source={A}&dest={B} | Search trains |
| POST | /api/trains/add | Add train (Admin only) |

### 3️⃣ Booking & PNR

| Method | Endpoint | Description |
|------|---------|-------------|
| POST | /api/bookings/book | Book ticket |
| GET | /api/bookings/pnr/{pnrNumber} | Check PNR status |
| DELETE | /api/bookings/cancel/{pnrNumber} | Cancel ticket |

---

## ⚙️ Setup & Installation

### Clone Repository
```bash
git clone https://github.com/ashhdubey/IRCTC-Backend-Project.git
cd IRCTC-Backend-Project
```

### Build Project
```bash
mvn clean install
```

### Run Application
```bash
mvn spring-boot:run
```

Server starts at **http://localhost:8080**

---

## 🧠 Learning Outcomes

✔ Spring Boot backend design without ORM dependency  
✔ Real‑world usage of **Data Structures**  
✔ Handling **Concurrency & Race Conditions**  
✔ Clean **REST API** architecture  

---

## 📬 Contact

**Ashish Kumar Dubey**  
🔗 GitHub: https://github.com/ashhdubey  
🔗 LinkedIn: https://www.linkedin.com/in/ashhdubey/
