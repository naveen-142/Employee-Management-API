# Employee Management API

A production-ready **Employee Management REST API** built using **FastAPI**, **MySQL**, and **SQLAlchemy**. This project provides secure and scalable employee management with CRUD operations, search, filtering, pagination, sorting, request validation, and standardized API responses following REST API best practices.

---

## 🚀 Features

* ✅ Create, Read, Update and Delete (CRUD) employee records
* ✅ Search employees by name, email, department, and designation
* ✅ Pagination for large datasets
* ✅ Sorting by salary, name, and joining date
* ✅ Request validation using Pydantic
* ✅ SQLAlchemy ORM for database operations
* ✅ Centralized exception handling
* ✅ Structured logging
* ✅ Standardized API responses
* ✅ Interactive API documentation with Swagger UI
* ✅ RESTful API architecture
* ✅ Environment variable configuration
* ✅ Git version control

---

## 🛠 Tech Stack

* Python 3.12
* FastAPI
* MySQL
* SQLAlchemy
* Pydantic
* Uvicorn
* Alembic
* python-dotenv
* Logging
* Pytest
* Git
* Postman

---

## 📂 Project Structure

```text
employee-management-api/
│
├── app/
│   ├── api/
│   ├── core/
│   ├── database/
│   ├── exceptions/
│   ├── models/
│   ├── repository/
│   ├── schemas/
│   ├── services/
│   ├── utils/
│   └── main.py
│
├── tests/
├── requirements.txt
├── .env
├── README.md
└── run.py
```

---

## ⚙ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/employee-management-api.git

cd employee-management-api
```

---

### 2. Create Virtual Environment

**Windows**

```bash
python -m venv venv

venv\Scripts\activate
```

**Linux / macOS**

```bash
python3 -m venv venv

source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure Environment Variables

Create a `.env` file in the project root.

```env
DATABASE_URL=mysql+pymysql://username:password@localhost:3306/employee_db

SECRET_KEY=your_secret_key

ALGORITHM=HS256

ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

### 5. Run Database Migrations

```bash
alembic upgrade head
```

---

### 6. Start the Server

```bash
uvicorn app.main:app --reload
```

Server will run at

```text
http://127.0.0.1:8000
```

---

## 📘 API Documentation

Swagger UI

```text
http://127.0.0.1:8000/docs
```

ReDoc

```text
http://127.0.0.1:8000/redoc
```

---

## 📌 API Endpoints

| Method | Endpoint                            | Description           |
| ------ | ----------------------------------- | --------------------- |
| POST   | `/employees`                        | Create Employee       |
| GET    | `/employees`                        | Get All Employees     |
| GET    | `/employees/{id}`                   | Get Employee by ID    |
| PUT    | `/employees/{id}`                   | Update Employee       |
| DELETE | `/employees/{id}`                   | Delete Employee       |
| GET    | `/employees?page=1&limit=10`        | Pagination            |
| GET    | `/employees?department=IT`          | Filter by Department  |
| GET    | `/employees?designation=Developer`  | Filter by Designation |
| GET    | `/employees?sort=salary&order=desc` | Sorting               |

---

## 🗄 Database Schema

| Field        | Type     |
| ------------ | -------- |
| id           | Integer  |
| first_name   | String   |
| last_name    | String   |
| email        | String   |
| phone        | String   |
| department   | String   |
| designation  | String   |
| salary       | Decimal  |
| joining_date | Date     |
| status       | Boolean  |
| created_at   | DateTime |
| updated_at   | DateTime |

---

## 📄 Sample Request

```json
{
  "first_name": "Naveen",
  "last_name": "Kumar",
  "email": "naveen@example.com",
  "phone": "9876543210",
  "department": "Engineering",
  "designation": "Python Developer",
  "salary": 65000,
  "joining_date": "2026-01-15"
}
```

---

## ✅ Sample Response

```json
{
  "success": true,
  "message": "Employee created successfully",
  "data": {
    "id": 1,
    "first_name": "Naveen",
    "last_name": "Kumar"
  }
}
```

---

## 🧪 Testing

Run all tests using:

```bash
pytest
```

---

## 📬 API Testing

The API can be tested using:

* Postman
* Swagger UI
* cURL

---

## 🔮 Future Enhancements

* JWT Authentication
* Role-Based Access Control (RBAC)
* Employee Profile Image Upload
* CSV Import & Export
* Dashboard Analytics
* Docker Support
* CI/CD Pipeline
* Redis Caching
* Email Notifications

---

## 👨‍💻 Author

**Naveen Kumar**

* Python Developer
* FastAPI Enthusiast
* Open Source Learner

---

## ⭐ Support

If you found this project useful, consider giving it a **⭐ Star** on GitHub. It helps others discover the project and supports future improvements.
