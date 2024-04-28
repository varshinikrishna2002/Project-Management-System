Project-Management-System
RESTful API using Java 17 and Spring Boot, implementing CRUD (Create,  Read, Update, Delete) operations for a Project Management System.

This is a simple RESTful API-based Project Management System built using Java 17 and Spring Boot, with an in-memory H2 database for data persistence.
Setup Instructions
Prerequisites
Java 17 installed on your system
Maven for dependency management (optional, as the project includes Maven Wrapper)
Clone the Repository
git clone <repository_url>
cd project-management-system

Build the Project
./mvnw clean install

Run the Application
./mvnw spring-boot:run

Access the Application
The application will be running at http://localhost:8080

API Usage
Endpoints
Create a Project
URL: POST /projects
Request Body:
{
    "name": "Project Name",
    "description": "Project Description",
    "startDate": "2024-04-28",
    "endDate": "2024-05-28"
}
Response: Returns the created project with its assigned ID.
Get All Projects
URL: GET /projects
Response: Returns a list of all projects.
Get Project by ID
URL: GET /projects/{id}
Response: Returns the project with the specified ID.
Update a Project
URL: PUT /projects/{id}
Request Body: Same as create endpoint
Response: Returns the updated project.
Delete a Project
URL: DELETE /projects/{id}
Response: Returns a success message upon deletion.
Error Handling
The API provides meaningful error messages for invalid requests or server errors.
Data Validation
Input data is validated for create and update operations to ensure data integrity.
Documentation
API documentation is available at http://localhost:8080/swagger-ui.html when the application is running.
