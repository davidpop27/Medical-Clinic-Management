# 🏥 Medical Clinic Management System (Java & Hibernate)

A modular desktop clinic management application designed to streamline healthcare workflows. The system facilitates interactions between doctors and patients, handling appointment scheduling, medical records, and digital prescriptions through an object-oriented, layered architecture backed by an ORM.

---

## 💎 Architecture & OOP Principles

The application is structured around enterprise design patterns and object-oriented principles:

- **Encapsulation:** Domain models (`Patient`, `Doctor`, `User`) enforce strict data integrity using private fields and validated accessor/mutator methods.
- **Service-Oriented Layering:** Business logic is decoupled from presentation and isolated into service classes (`AppointmentService`, `AuthService`), ensuring a clear separation of concerns.
- **Role-Based Access Control:** Strong typing with `UserRole` enums (`PATIENT`, `DOCTOR`) manages permission tiers and feature access.
- **ORM Persistence:** Utilizes **Hibernate / JPA** (configured via `HibernateUtil` and `persistence.xml`) for object-relational mapping to a relational database, abstracting SQL queries into managed entity lifecycles.

---

## 🚀 Key Features

- **Authentication & RBAC:** Secure user login and authorization routing depending on assigned privileges (Doctor vs. Patient).
- **Appointment Scheduling:** Patients and staff can schedule, review, and organize medical consultations via `AppointmentService`.
- **Medical Records & Prescriptions:** Healthcare providers can maintain structured patient medical histories and generate digital prescriptions.
- **Interactive Console UI:** Clean, menu-driven CLI interface driven by `ConsoleMenu` and standard input streams.

---

## 🛠️ Tech Stack

- **Language:** Java (JDK 17+)
- **ORM & Persistence:** Hibernate / JPA (`persistence.xml`)
- **Build & Dependency Management:** Apache Maven (`pom.xml`)
- **Database:** Relational SQL (configured through Hibernate dialect)
- **UI:** Console Interface (`java.util.Scanner`)

---

## 📁 Project Structure

```text
src/main/java/org/example/
├── Model/          # Domain entities (Doctor, Patient, User, etc.)
├── Servicii/       # Business logic layer (AppointmentService, AuthService, etc.)
├── Controller/     # Presentation logic and console menu routing (ConsoleMenu)
└── Database/       # Hibernate configuration and session factory utilities (HibernateUtil)
