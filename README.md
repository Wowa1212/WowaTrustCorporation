Features
Add Insured Records: Add new individuals with detailed information.
Find Insured by ID: Retrieve specific records using a unique ID.
Update Insured Data: Modify existing records seamlessly.
Delete Insured by ID: Remove records safely with an ID reference.
List All Insured: Display all existing records in the database.
Technologies Used
Programming Language: Java (version 17)
Frameworks: Spring Boot, JPA
Build Tool: Maven
Database: MySQL
Frontend: HTML, CSS, JavaScript
Port: 8081
Setup Instructions
Prerequisites
Install Java 17
Ensure Java 17 is installed and set as the default JDK.
Command to verify:
bash
Copy code
java -version
Install Maven
Command to verify Maven:
bash
Copy code
mvn -version
Install MySQL
Command to verify MySQL installation:
bash
Copy code
mysql --version
Steps
Clone or download the repository to your local machine.
Open a terminal in the project directory and run:
bash
Copy code
mvn spring-boot:run
Navigate to the application login page:
URL: http://localhost:8081/login
Default Credentials:
Username: user
Password: password
Database Setup
Login to your MySQL server:
bash
Copy code
sudo mysql
Execute the following SQL commands to set up the database and table:
sql
Copy code
CREATE DATABASE IF NOT EXISTS wowatrustcorporation;
USE wowatrustcorporation;

CREATE TABLE IF NOT EXISTS insureds (
    ID INT NOT NULL PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Surname VARCHAR(50) NOT NULL,
    Birth_Date DATE DEFAULT NULL,
    Address VARCHAR(100) NOT NULL,
    TelephoneNumber VARCHAR(20),
    BankAccountNumber VARCHAR(30) NOT NULL
);
Security
The application uses Spring Security for authentication.
For testing, use the default credentials. For production, configure your security in application.properties.
Configuration
Default configurations can be found in the application.properties file:

properties

server.port=8081

spring.datasource.url=jdbc:mysql://localhost:3306/wowatrustcorporation
spring.datasource.username=<your_mysql_username>
spring.datasource.password=<your_mysql_password>
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
Replace <your_mysql_username> and <your_mysql_password> with your MySQL credentials.

Contact
basjuk +420 737 100 055
