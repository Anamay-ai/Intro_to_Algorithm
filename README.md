# Warehouse Management System

A simple Java + JDBC + MySQL warehouse management project with:

- Login screen
- Role-based access for Admin and Staff
- Swing GUI
- Console mode
- Product, supplier, inventory, and transaction management
- Search, low-stock tracking, and CSV export
- REST API mode
- Input validation and unit tests

## How to Run on This Mac

The easiest way is to use the run script from the project folder:

```bash
./run.sh
```

This script:

- starts the local MySQL server on port `3307` if needed
- loads the schema and sample data
- runs the application in GUI mode

## Login Details

- Admin: `admin / admin123`
- Staff: `staff / staff123`

## Stop the App

```bash
./stop.sh
```

## If Needed

Make sure these are installed:

- Java 17+
- Maven
- MySQL 8+

If `run.sh` is not executable, run:

```bash
chmod +x run.sh stop.sh
```

## Other Run Modes

Console mode:

```bash
mvn exec:java -Dexec.args="console"
```

API mode:

```bash
mvn exec:java -Dexec.args="api"
```

## Main Project Files

- `src/main/java/com/wms/Main.java` - application entry point
- `src/main/java/com/wms/ui/` - GUI and console UI
- `src/main/java/com/wms/service/` - business logic
- `src/main/java/com/wms/dao/` - database access layer
- `src/main/resources/db.properties` - database configuration
- `sql/schema.sql` - database tables
- `sql/sample_data.sql` - sample records
- `run.sh` - setup and run script
- `stop.sh` - stop script

## Notes for Submission

- The project is already cleaned to remove generated build files.
- The app is configured to use the local MySQL instance on `127.0.0.1:3307`.
- If you move the project to another computer, update `src/main/resources/db.properties` and `run.sh` if the MySQL paths are different.
