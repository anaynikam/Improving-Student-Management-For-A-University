# Improving-Student-Management-For-A-University

ABC University has been using a basic student management system that lacks the modern features required for efficient administration. They have tasked your team with enhancing the existing Student Dashboard application to improve the user experience and provide a more comprehensive solution. Here are the specific requirements:

Tech Stack:

Frontend: Angular (running on port 8081) Backend: Spring Boot (running on port 8080)

Implementation Details:

Enhance the User Interface:
The application interface needs to be improved to provide a better user experience. You should focus on refining the following components:

Models:

Create models folder under angularapp/src Implement student.model.ts file to export the Student Interface with attributes id(int), name(string), department(string), phonenumber(string)

Routing :

Create routing folder under angularapp/src/app move the app-routing.module.ts file into the routing folder.

Navbar Component:

Create Navbar Component under angularapp/src/app Implement navbar component with two routes Students List (by default route - ""), Add Students (/add) Apply CSS styling to align and visually group the form elements.

Student-List Component:

Create Student-List Component under angularapp/src/app Implement student-list component to list all the students from the database(back-end). Apply CSS styling to align and visually group the form elements.

Student-Add Component:

Create Student-Add Component under angularapp/src/app Implement a student-add component to add new students to the database (back-end). Apply CSS styling to align and visually group the form elements.

Student-Details Component:

Create Student-Details Component under angularapp/src/app Implement student-details component to view the details of individual students by ID. Apply CSS styling to align and visually group the form elements.

Services:

Create Services folder under angularapp/src Implement student.service.ts to integrate with the backend. Implement three methods in this student.service.ts file getStudents createStudent getStudentById

App-Routing:

Implement App-Routing with paths '' - default route to list students 'add' - to route to Student-Add component 'details/:id' - to route to Student-Details Component .

Backend Integration:
Integrate the frontend with the backend API to handle student data. The backend is implemented using Spring Boot and is running on port 8080.

Endpoint Details:

GET /getAllStudent:

Description: Fetches a list of all students from the backend.

GET /getById/{id}:

Description: Fetches a specific student's details based on the provided ID. Path Variable:

id (String): The unique ID of the student to fetch.

POST /addStudent:

Description: Adds a new student to the backend database. Request Body: JSON Object:

id (String): Registration ID of the student.

name (String): Name of the student.

department (String): Department of the student.

phonenumber (String): Phone number of the student.

Backend Integration for Student Dashboard Application

Overview:

The backend integration for the Student Dashboard application involves creating the necessary components and endpoints to handle student data. The backend is developed using Spring Boot and will provide APIs for adding students, retrieving individual student details, and fetching a list of all students.

Functional Requirements:

Create Folders: Inside the WORKSPACE/springapp/src/main/java/com/examly/springapp, create the following folders:

controller models repository service configuration

ApiController: Inside the controller folder, create a Java file named ApiController.java. This class will handle API endpoints.

Student Model: Inside the models folder, create a Java file named Student.java. Define the Student class with the following variables:

id (int) name (String) department (String) phonenumber (String) Include appropriate getters, setters, and constructors for these variables.

StudentRepo: Inside the repository folder, create a Java file named StudentRepo.java. This interface will extend the JpaRepository interface to perform database operations.

StudentService: Inside the service folder, create a Java file named StudentService.java. This class will handle business logic related to students.

CORS Configuration: Inside the configuration folder, create a Java file to implement CORS (Cross-Origin Resource Sharing) configuration.
