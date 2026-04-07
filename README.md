# Warehouse Management System (Java + JDBC)

A Warehouse Management System developed in Java using JDBC and MySQL, with both Console and GUI interfaces.

## Super Simple Run
From project folder:

1. Start everything:
- ./run.sh

2. Login:
- admin / admin123
- staff / staff123

3. Stop everything:
- ./stop.sh

## Features
- Login authentication system (username/password)
- Role-based access control (ADMIN and STAFF)
- GUI interface using Swing
- Product CRUD: add, view, update, delete, search
- Supplier CRUD: add, view, update, delete, search
- Inventory management
- Stock IN and OUT transactions
- Search and filter by name and category
- Low stock product report
- Report generation (CSV export)
- REST API integration (/api/health, /api/products, /api/products/search)
- Exception handling and input validation
- Unit testing with JUnit 5

## OOP Concepts Demonstrated
- Classes and objects
- Constructor usage
- Encapsulation (private fields with getters/setters)
- Inheritance (Product extends Item, Supplier extends Person)
- Polymorphism (method overriding)
- Method overloading
- Abstraction (abstract class Item)
- Collections (ArrayList, HashMap)

## Project Structure
- src/main/java/com/wms/model: entity and base classes
- src/main/java/com/wms/dao: DAO interfaces
- src/main/java/com/wms/dao/impl: JDBC DAO implementations
- src/main/java/com/wms/service: business logic
- src/main/java/com/wms/ui: console and Swing GUI presentation layer
- src/main/java/com/wms/auth: login/authentication logic
- src/main/java/com/wms/api: REST API server
- src/main/java/com/wms/Main.java: entry point
- src/main/resources/db.properties: DB config
- sql/schema.sql: schema creation
- sql/sample_data.sql: seed data
- docs/class-diagram.md: class diagram source
- docs/project-report-template.md: report template

## Prerequisites
- Java 17+
- Maven 3.8+
- MySQL 8+

## Setup Steps
1. Create database and tables:
   - Run sql/schema.sql
2. Insert sample records:
   - Run sql/sample_data.sql
3. Update database credentials:
   - Edit src/main/resources/db.properties

## Build and Run
Build:
- mvn clean compile

Run GUI mode (default):
- mvn exec:java

Run console mode:
- mvn exec:java -Dexec.args="console"

Run REST API mode:
- mvn exec:java -Dexec.args="api"

Run tests:
- mvn test

Default login users:
- admin / admin123 (ADMIN)
- staff / staff123 (STAFF)

## Suggested Submission Package
- Source code folder
- SQL scripts (schema and sample data)
- Project report PDF generated from docs/project-report-template.md
- Application screenshots
- Class diagram image generated from docs/class-diagram.md
