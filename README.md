# 📓 Journal Management App

A **Spring Boot** application for managing personal journals.  
This app allows users to create, update, delete, and search journal entries while ensuring secure authentication and role-based access.

---

## 🚀 Features
- ✏️ **Create, Edit, Delete** journal entries.
- 📜 **View all entries** in a clean UI.
- 🔍 **Search entries** by title or content.
- 🔒 **User authentication** using Spring Security.
- 🗝 **Role-based authorization** (Admin/User).
- 🌐 RESTful API support.

---

## 📂 Project Structure

```
Journal-Management-App/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/journal/
│   │   │       ├── controller/      # REST controllers for handling requests
│   │   │       ├── entity/          # JPA entities (Journal, User, Role)
│   │   │       ├── repository/      # Spring Data JPA repositories
│   │   │       ├── security/        # Spring Security configuration
│   │   │       └── service/         # Business logic
│   │   └── resources/
│   │       ├── application.properties # App configuration
│   │    
│   │       
│   └── test/                        # Unit and integration tests
├── pom.xml                           # Maven dependencies
└── README.md                         # Project documentation
```

---

## 🛠️ Technologies Used
- **Java 17**
- **Spring Boot 3.x**
- **Spring Data JPA**
- **Spring Security**
- **Thymeleaf** (or React/Vue if frontend is separate)
- **MySQL/PostgreSQL**
- **Maven**

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/journal-management-app.git
cd journal-management-app
```

### 2️⃣ Configure Database
Update `src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/journal_app
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
```

### 3️⃣ Build & Run
```bash
mvn clean install
mvn spring-boot:run
```

---

## 📡 API Endpoints

| Method | Endpoint            | Description              | Auth Required |
|--------|--------------------|--------------------------|--------------|
| GET    | `/api/journals`    | Get all journal entries  | ✅ |
| GET    | `/api/journals/{id}` | Get journal by ID        | ✅ |
| POST   | `/api/journals`    | Create new journal       | ✅ |
| PUT    | `/api/journals/{id}` | Update journal           | ✅ |
| DELETE | `/api/journals/{id}` | Delete journal           | ✅ |
| POST   | `/api/auth/signup` | User registration        | ❌ |
| POST   | `/api/auth/login`  | User login               | ❌ |

---

## 🔐 Authentication & Authorization
- **JWT-based Authentication** for secure API calls.
- Roles:
  - `ROLE_USER`: Can create, edit, and view their own journals.
  - `ROLE_ADMIN`: Can manage all users and journals.

---

## 🧪 Running Tests
```bash
mvn test
```

---

## 📌 Future Enhancements
- 📅 Add calendar view for journals.
- 📤 Export journals as PDF/Markdown.
- 📱 Mobile-friendly UI.
- 🔔 Email notifications for new entries.

---



