<div align="center">

# 🏛️ Digital Subsidy & Grant Administration Platform

<p align="center">
  <b>A Transparent, Multi-Tier Government Subsidy Management & Beneficiary Tracking System</b>
</p>

[![Java 17](https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.java.com/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.2.0-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![React](https://img.shields.io/badge/React-19.2.7-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-8.1.1-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Security](https://img.shields.io/badge/Spring_Security-JWT-005F87?style=for-the-badge&logo=jsonwebtokens&logoColor=white)](https://jwt.io/)

[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)](https://github.com/Shaik-Shafi-01/Govt-Subsidy)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

<br />

[Overview](#-overview) • [Features](#-key-features) • [Tech Stack](#-tech-stack) • [Quick Start](#-quick-start) • [Role Portals](#-role-portals--demo-credentials) • [Architecture](#-architecture) • [API Reference](#-api-reference)

---

</div>

## 📋 Overview

The **Government Subsidy & Grant Disbursement Tracking System** is an enterprise-grade full-stack web application designed to streamline government subsidy disbursement processes. It provides a transparent, multi-tier approval workflow system that enables citizens to apply for subsidies while government officers can verify, review, and approve applications across various administrative levels.

> [!NOTE]
> This platform ensures end-to-end accountability, real-time application lifecycle tracking, automated eligibility calculation, and role-restricted disbursement processing.

---

## ✨ Key Features

### 👥 Role-Based Portals & Access Control
* **Citizen / Beneficiary**: Browse scheme catalogs, check eligibility, submit subsidy applications, upload verification documents, and track approval status.
* **Field Officer (Level 1)**: Conduct ground-level physical & document verification and provide preliminary recommendations.
* **District Officer (Level 2)**: Secondary scrutiny of field reports, application evaluation, and district-level approval.
* **Finance Officer (Level 3)**: Final financial validation, budget allocation check, and grant disbursement authorization.
* **System Administrator**: Manage subsidy schemes, configure eligibility rules, assign roles, and monitor system metrics.

---

### 🛡️ Core System Capabilities

| Feature Category | Highlights |
| :--- | :--- |
| 🔄 **Workflow Stepper** | Visual interactive lifecycle tracker for beneficiaries to view live application state |
| 📊 **Analytics Dashboard** | Real-time charts, scheme utilization metrics, and regional status distribution reports |
| 🔒 **Enterprise Security** | Stateless JWT authentication, Spring Security RBAC, BCrypt password encryption, CORS protection |
| ⚡ **Modern UX** | Responsive React 19 single-page application (SPA), instant searching & dynamic filtering |
| 📄 **Document Management** | Upload and review supporting proofs with audit logs for re-verification requests |
| 📈 **Export System** | Generate scheme utilization summaries and application reports |

---

## 🛠️ Tech Stack

<div align="center">

### Backend (Java Spring Boot)

| Layer / Module | Technology | Version / Specification |
| :--- | :--- | :--- |
| **Language** | Java OpenJDK | `17` |
| **Framework** | Spring Boot | `3.2.0` |
| **Web API** | Spring Web MVC | RESTful Architecture |
| **Data Persistence** | Spring Data JPA | Hibernate ORM |
| **Security Layer** | Spring Security | Stateless JWT Authentication |
| **Database Engine** | H2 Database (In-Memory) / MySQL | Configurable |
| **Build & Dependencies** | Maven / Maven Wrapper | `3.6+` (`mvnw`) |
| **Automated Testing** | JUnit 5, Spring Boot Test | MockMvc |

<br />

### Frontend (React + Vite)

| Layer / Module | Technology | Version / Specification |
| :--- | :--- | :--- |
| **UI Library** | React | `19.2.7` |
| **Build System** | Vite | `8.1.1` |
| **Routing** | React Router DOM | `7.18.1` |
| **Styling Engine** | Modern CSS3 | Custom Tokens & Responsive Grid |
| **Iconography** | React Icons | `5.7.0` |
| **HTTP Client** | Native Fetch API | Custom Service Abstraction Layer |

</div>

---

## 🔑 Role Portals & Demo Credentials

Use the pre-configured accounts below to log in and test different system workflow tiers:

| Role | Email | Password | Assigned Dashboard | Primary Responsibility |
| :--- | :--- | :--- | :--- | :--- |
| 👨‍💼 **Admin** | `admin@gov.in` | `Password@123` | `/admin` | Manage schemes, system config & analytics |
| 🔍 **Field Officer** | `field.officer@gov.in` | `Password@123` | `/field-officer` | Ground verification & preliminary review |
| 📋 **District Officer** | `district.officer@gov.in` | `Password@123` | `/district-officer` | Level 2 scrutiny & administrative approval |
| 💵 **Finance Officer** | `finance.officer@gov.in` | `Password@123` | `/finance-officer` | Level 3 final fund disbursement |
| 👤 **Beneficiary** | `citizen@gov.in` | `Password@123` | `/dashboard` | Submit applications & track status |

---

## 🚀 Quick Start

### Prerequisites
Make sure you have installed:
* **Java 17 Development Kit (JDK 17+)** — [Download](https://www.oracle.com/java/technologies/downloads/#java17)
* **Node.js (v16+)** & **npm (v7+)** — [Download](https://nodejs.org/)
* **Git** version control tool — [Download](https://git-scm.com/)

---

### 1️⃣ Clone Repository
```bash
git clone https://github.com/Shaik-Shafi-01/Govt-Subsidy.git
cd Govt-Subsidy
```

### 2️⃣ Launch Backend (Spring Boot Service)
```bash
# Using Maven Wrapper (Windows)
.\mvnw.cmd spring-boot:run

# Using Maven Wrapper (Linux / macOS)
./mvnw spring-boot:run

# OR using local Maven install
mvn clean spring-boot:run
```
> 🌐 **Backend API Service**: Runs at `http://localhost:8080`

### 3️⃣ Launch Frontend (React + Vite)
```bash
# Install NPM dependencies
npm install

# Start Vite development server
npm run dev
```
> 🌐 **Frontend Application**: Runs at `http://localhost:5173`

---

## 🏗️ Architecture & Workflow

### Tiered Approval Pipeline

```
  ┌───────────────────────────┐
  │  1. Beneficiary           │  Submits Subsidy Application & Uploads Documents
  └─────────────┬─────────────┘
                │
                ▼
  ┌───────────────────────────┐
  │  2. Field Officer         │  Conducts Level 1 Ground Verification & Report
  └─────────────┬─────────────┘
                │
                ▼
  ┌───────────────────────────┐
  │  3. District Officer      │  Performs Level 2 Secondary Administrative Scrutiny
  └─────────────┬─────────────┘
                │
                ▼
  ┌───────────────────────────┐
  │  4. Finance Officer       │  Executes Level 3 Financial Approval & Disbursement
  └─────────────┬─────────────┘
                │
                ▼
  ┌───────────────────────────┐
  │  5. Beneficiary Account   │  Disbursement Complete & Final Status Updated
  └───────────────────────────┘
```

---

## 📁 Repository Structure

```text
Govt-Subsidy/
├── 📄 Backend_Documentation.docx    # Detailed Backend Architecture Specification
├── 📄 Frontend_Documentation.docx   # Detailed Frontend Technical Specification
├── 📄 README.md                     # Project Master Documentation
├── 📄 schema.sql                    # SQL Database Schemas & Initial Seed Data
├── 📄 pom.xml                       # Backend Maven Build Configuration
├── 📄 package.json                  # Frontend Dependencies & NPM Scripts
├── 📄 vite.config.js                # Vite Development Server Configuration
├── 📄 mvnw / mvnw.cmd               # Cross-Platform Maven Wrapper Scripts
│
├── 📁 src/
│   ├── 📁 main/
│   │   ├── 📁 java/com/government/subsidy/
│   │   │   ├── 📁 controller/      # REST API Controllers (Auth, App, Scheme)
│   │   │   ├── 📁 dto/             # Data Transfer Objects (Requests/Responses)
│   │   │   ├── 📁 model/           # JPA Entities (User, Application, Scheme)
│   │   │   ├── 📁 repository/      # Spring Data JPA Repositories
│   │   │   ├── 📁 security/        # JWT Authentication Filters & WebSecurity
│   │   │   ├── 📁 service/         # Core Business Logic Layer
│   │   │   └── 📁 exception/       # Global Controller Exception Handlers
│   │   └── 📁 resources/           # Application Properties & Data Schemas
│   │
│   ├── 📁 test/                    # Backend Unit & Integration Tests
│   │
│   ├── 📁 components/              # Reusable UI Components (Navbar, Sidebar, Footer)
│   ├── 📁 pages/                   # Role Dashboards & Main Application Pages
│   ├── 📁 services/                # Axios / Fetch API Integration Layer
│   ├── 📁 layouts/                 # Page Layout Wrappers
│   └── 📁 styles/                  # Modular Component CSS Stylesheets
```

---

## 📡 API Reference Summary

### Base URL
`http://localhost:8080/api/v1`

### 🔑 Authentication Endpoints
* **`POST /api/v1/auth/login`**: Authenticate user & receive JWT token.
* **`POST /api/v1/auth/signup`**: Register a new citizen/beneficiary account.

### 📝 Application Endpoints
* **`POST /api/v1/applications/submit`**: Submit a new subsidy application.
* **`GET /api/v1/applications/my-applications`**: Fetch logged-in user's applications.
* **`GET /api/v1/applications/{id}`**: Retrieve detailed application details & status.

### 🏛️ Scheme Endpoints
* **`GET /api/v1/schemes`**: Fetch list of active government subsidy schemes.
* **`GET /api/v1/schemes/{id}`**: Fetch details and eligibility criteria for a scheme.
* **`POST /api/v1/schemes`**: Create a new subsidy scheme *(Admin restricted)*.

---

## 🧪 Testing

### Run Backend Unit & Integration Tests
```bash
mvn test
```

### Run Specific Test Suite
```bash
mvn test -Dtest=GlobalExceptionHandlerTest
```

---

## 📝 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

<div align="center">

---
**[⬆ Back to Top](#-digital-subsidy--grant-administration-platform)**

</div>
