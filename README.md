# 🎓 Campus EventHub
### A Python-based Event Registration & Capacity Management System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![SQLite](https://img.shields.io/badge/SQLite-Database-lightgrey?style=for-the-badge&logo=sqlite)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-orange?style=for-the-badge)

---

## 📖 Overview
**Campus EventHub** is a CLI-based desktop application designed to streamline the chaotic process of event management in educational institutions. It eliminates manual paper sign-ups by providing a centralized digital platform where administrators can host events and students can register in real-time.

The core innovation of this system is the **Automated Capacity Engine**, which ensures that event bookings never exceed the hall capacity, preventing overcrowding issues.

---

## 📸 System Architecture & Design
The system follows a modular design pattern separating the Database Layer, Business Logic, and User Interface.

### 1. System Architecture
> *The flow of data from the User Interface to the SQLite Database.*

![Architecture Diagram](assets/architecture_diagram.png)
*(Place your architectural diagram here. See below for example)*

### 2. Database Schema (ER Diagram)
> *The relationship between Students, Events, and Registrations.*

![ER Diagram](assets/er_diagram.png)
*(Place your ER diagram here)*

---

## 🚀 Key Features

### 🏛 For Administrators
* **Create Events:** Define event name, date, and maximum seating capacity.
* **Live Monitoring:** View real-time "Available Seats" count.
* **Roster Management:** View list of registered students per event.

### 🎓 For Students
* **Event Discovery:** Browse all upcoming active events.
* **One-Click Registration:** seamless booking experience.
* **Validation:** Built-in checks to prevent duplicate registrations.
* **Capacity Handling:** System auto-locks registration when `Seats == 0`.

---

## 🛠️ Technologies Used

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Language** | Python 3.x | Core logic and application flow |
| **Database** | SQLite3 | Serverless, ACID-compliant storage |
| **Architecture** | Modular | Separation of concerns (Model-View-Controller approach) |
| **Version Control** | Git | Source code management |

---

## 📂 Project Structure

```text
EventHub/
├── data/
│   └── events.db           # Persistent Database storage
├── src/
│   ├── __init__.py
│   ├── main.py             # Application Entry Point
│   ├── db_manager.py       # Database Connection & Setup
│   ├── admin_actions.py    # Admin Functionality Module
│   ├── student_actions.py  # Student Registration Module
│   ├── models.py           # Data Classes
│   └── validators.py       # Input Validation (Email/Dates)
├── assets/                 # Screenshots and Diagrams
├── requirements.txt        # Dependencies (if any)
└── README.md               # Project Documentation
