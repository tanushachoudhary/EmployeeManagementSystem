# Employee Management System

<img width="1919" height="845" alt="image" src="https://github.com/user-attachments/assets/86ba3b9d-134a-43c8-87ed-52e25b80f568" />

A web application for managing employee records. Built using:

- Spring Boot  
- Spring Data JPA  
- React  
- Bootstrap  

---

## Features

- Add, view, update, and delete employee details  
- Responsive UI with Bootstrap  
- RESTful backend with Spring Boot and JPA  
- Frontend-backend integration using React  

---

## Project Structure

```

EmployeeManagementSystem/
├── ems-backend/         ← Backend/server-side code
│   ├── src/main/java/...
│   ├── src/main/resources/...
│   └── ...
├── ems-frontend/        ← React frontend
│   ├── public/
│   ├── src/
│   └── ...
└── README.md            ← This file

````

---

## Prerequisites

- Java JDK (version 17+ recommended)  
- Maven 
- Node.js & npm (for frontend)  
- Git  

---

## Getting Started

1. Clone the repository  
   ```bash
   git clone https://github.com/tanushachoudhary/EmployeeManagementSystem.git
   ````


2. Set up the backend

   ```bash
   cd EmployeeManagementSystem/ems-backend
   # (Optional) configure application.properties/application.yml for DB connection, etc.
   mvn clean install     # or ./mvnw clean install
   mvn spring-boot:run   # or ./mvnw spring-boot:run
   ```

3. Set up the frontend

   ```bash
   cd ../ems-frontend
   npm install           # or yarn
   npm start             # or yarn start
   ```

4. Open your browser at `http://localhost:3000` (or whatever port the frontend uses).

---

## Configuration & Environment

* Database settings, ports, etc., can be configured in `application.properties` (backend)
* API endpoints exposed by the backend (e.g., `GET /employees`, `POST /employees`, etc.)
* Frontend environment variables if needed (e.g., base API URL)

---

## Screenshots

<img width="1916" height="742" alt="image" src="https://github.com/user-attachments/assets/2052fee2-81f1-494f-9eea-7e211796fc4b" />

<img width="1917" height="720" alt="image" src="https://github.com/user-attachments/assets/3fad267e-4b0b-4698-bbcf-efdcaf1df8e4" />

---

## Testing

* (If you have unit/integration tests) How to run them:

  ```bash
  # backend
  mvn test

  # frontend
  npm test
  ```

---

## Contributing

Feel free to open issues or submit pull requests. Some ideas:

* Add search / filtering employees
* Add authentication / authorization
* Improve UI styling
* Add reporting (export CSV / PDF)

