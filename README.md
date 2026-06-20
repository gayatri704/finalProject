# 🍔 Food Voting Web Application

A full-stack web application built with **Spring Boot** that allows users to register, log in, add food items with images, vote for their favorite dishes, and view the current winner. The application is designed for classrooms, events, and group activities where participants need a simple and interactive way to decide on food choices.

## 📌 Features

### User Authentication
- User registration with username, email, and password
- Secure login and logout functionality
- Password encryption using BCrypt
- Duplicate username and email validation

### Food Management
Authenticated users can:
- Add food items
- Upload food images
- Edit existing food entries
- Delete food items

### Voting System
- Vote for food items
- Automatic vote count updates
- Top Champion display showing the food item with the highest votes

### Search Functionality
- Search food items by name
- Case-insensitive filtering
- Real-time search results

### Responsive User Interface
- Modern card-based layout
- Mobile-friendly design
- Sidebar for search, champion display, and food management

### Cloud Deployment
- Dockerized application
- Deployed on Render
- Supports PostgreSQL (local) and H2 Database (cloud)

---

## 🛠 Technologies Used

| Category | Technology |
|-----------|------------|
| Language | Java 21 |
| Framework | Spring Boot |
| Security | Spring Security |
| ORM | Spring Data JPA / Hibernate |
| Template Engine | Thymeleaf |
| Database (Local) | PostgreSQL |
| Database (Cloud) | H2 In-Memory Database |
| Build Tool | Gradle |
| Utility | Lombok |
| Containerization | Docker |
| Deployment | Render |
| Version Control | Git & GitHub |

---

## 📂 Project Structure

```text
src
├── main
│   ├── java
│   │   └── com.example.foodvoting
│   │       ├── controller
│   │       ├── service
│   │       ├── repository
│   │       ├── model
│   │       ├── config
│   │       └── security
│   └── resources
│       ├── templates
│       ├── static
│       └── application.properties
└── test
```

---

## 🗄 Database Schema

### Users Table

| Column | Type |
|----------|----------|
| id | BIGINT (PK) |
| username | VARCHAR (UNIQUE) |
| email | VARCHAR (UNIQUE) |
| password | VARCHAR |

### Food Table

| Column | Type |
|----------|----------|
| id | BIGINT (PK) |
| name | VARCHAR |
| vote_count | INT |
| image_name | VARCHAR |

---

## 🚀 Getting Started

### Prerequisites

- Java 21
- PostgreSQL
- Gradle
- Git

### Clone the Repository

```bash
git clone https://github.com/gayatri704/finalProject.git
cd finalProject
```

### Configure Database

Update `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/foodvoting
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### Run the Application

```bash
./gradlew bootRun
```

or on Windows:

```bash
gradlew.bat bootRun
```

Open:

```text
http://localhost:8080
```

---

## 🐳 Docker Deployment

Build the Docker image:

```bash
docker build -t food-voting-app .
```

Run the container:

```bash
docker run -p 8080:8080 food-voting-app
```

---

## 🧪 Testing

The application was tested for:

- User registration
- User login/logout
- Food CRUD operations
- Voting functionality
- Search functionality
- Responsive design
- Error handling
- Deployment verification

---

## 👨‍💻 Team Members

### Rai Aayuska
**Responsibilities**
- Frontend UI/UX Design
- Thymeleaf Template Development
- Responsive Layout Design
- Testing and Documentation
- Deployment Assistance

### Bhandari Gayatri Kumari
**Responsibilities**
- Backend Development
- Authentication Logic
- Database Integration
- Controller and Service Implementation
- Repository Management

---

## 🔧 Future Improvements

- User-specific vote tracking
- Food categories and tags
- User profiles
- Persistent cloud PostgreSQL database
- Voting analytics and reports
- Admin dashboard

---

## 📖 Learning Outcomes

Through this project, we gained experience in:

- Spring Boot Development
- Spring Security Authentication
- Thymeleaf Template Engine
- PostgreSQL Database Management
- Docker Containerization
- Cloud Deployment with Render
- Git and GitHub Collaboration
- Responsive Web Design

---

## 📜 License

This project was developed as a university academic project and is intended for educational purposes.

---

## 🔗 Repository

Repository: https://github.com/gayatri704/finalProject
