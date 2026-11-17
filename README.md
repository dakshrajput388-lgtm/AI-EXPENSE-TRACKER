# SmartSpend - Personal Expense Tracker

A desktop personal expense and budget management application built with JavaFX and MySQL. It helps users track daily income and expenses, set monthly category budgets with real-time alerts, visualize spending trends through charts, export financial reports to CSV, and get personal savings suggestions through an integrated Gemini AI assistant.

---

## Features

- **Authentication & Security**: User registration and login with SHA-256 password hashing.
- **Expense & Income Tracking**: Log daily transactions with category, description, date, and amount.
- **Budget Monitoring**: Set monthly spending limits per category with visual progress and warning indicators when budgets are exceeded.
- **Dashboard & Analytics**: Real-time KPI summaries, category expense breakdown (PieChart), and monthly income vs. expense comparison (BarChart).
- **Reports & CSV Export**: Filter transactions by custom date ranges and export structured reports to CSV.
- **AI Financial Assistant**: In-app financial advisor powered by Google Gemini API to analyze spending patterns and suggest saving strategies (with offline fallback).
- **Concept Reference Folders**: Dedicated folders showcasing core Java topics (`OOP`, `JDBC`, `exceptionhandling`, `JavaFX`, `Streams`, `Multithreading`).

---

## Tech Stack

- **Language**: Java 21
- **GUI Framework**: JavaFX (OpenJFX 21)
- **Database**: MySQL 8.0+ / In-memory H2 database (automatic fallback)
- **Database Access**: Pure JDBC (`PreparedStatement`, DAO pattern)
- **Build Tool**: Maven

---

## Project Structure

```
AI-EXPENSE-TRACKER/
├── src/main/java/com/smartspend/
│   ├── model/          # Domain models (Transaction, Expense, Income, Budget, User)
│   ├── dao/            # Data Access Objects (CRUD operations via JDBC)
│   ├── service/        # Business logic, reports, and Gemini API client
│   ├── controller/     # Controllers coordinating UI and services
│   ├── view/           # JavaFX UI views, layouts, and charts
│   ├── util/           # Helpers (session manager, alerts, CSV export, date utils)
│   └── Main.java       # Application entry point
│
├── exceptionhandling/  # Code references for custom exceptions & try-with-resources
├── JDBC/               # Code references for database connection & queries
├── JavaFX/             # Code references for JavaFX views & lifecycle
├── OOP/                # Code references for OOP concepts (Abstraction, Inheritance, etc.)
├── Streams/            # Code references for Java 8 Streams & File I/O
├── Multithreading/     # Code references for background tasks & async API calls
│
├── database/           # SQL schema scripts
├── run.bat             # One-click Windows runner
├── pom.xml             # Maven build configuration
└── SmartSpend_Project_Documentation.pdf # Full 22-page technical report
```

---

## Getting Started

### Prerequisites
- JDK 21 installed and added to `PATH` (or set in `JAVA_HOME`).
- MySQL Server (optional; if MySQL is not running, the application will automatically run using an embedded in-memory database).

### Running the App

#### Option 1: Using the Batch File (Windows)
Double-click `run.bat` or run it from the terminal:
```cmd
run.bat
```

#### Option 2: Using Maven
```bash
mvn clean javafx:run
```

---

## Default Login Credentials

If running for the first time, you can register a new account or log in with the pre-seeded demo account:
- **Username**: `demo`
- **Password**: `demo123`

---

## Documentation
For complete architecture diagrams, database schema, syllabus concept mappings, and code explanations, refer to **`SmartSpend_Project_Documentation.pdf`** included in the repository root.
