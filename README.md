# Car Rental Management System

## Project Overview

This is a comprehensive Car Rental Management System developed in Java using Swing for the GUI and MySQL for database management. The system provides a complete solution for managing car rentals, customers, vehicles, payments, and maintenance records.

## Features

### Core Modules
1. **User Authentication**
   - Secure login system for employees
   - New user registration

2. **Dashboard**
   - Central hub for accessing all system functionalities
   - Menu-based navigation to different modules

3. **Vehicle Management**
   - Add, update, delete, and view car information
   - Track vehicle details (make, model, year, license plate, rental rate, status)
   - Vehicle status tracking (Available, Rented, Maintenance)

4. **Customer Management**
   - Maintain customer records (name, contact info, address, license number)
   - Add, update, delete, and search customer information

5. **Rental Management**
   - Process car rental agreements
   - Assign vehicles to customers
   - Calculate rental amounts based on duration and daily rates
   - Track rental start/end dates

6. **Payment Processing**
   - Record payment transactions
   - Support multiple payment methods (Cash, Mobile Money, Bank Transfer, etc.)
   - Link payments to specific rental agreements

7. **Vehicle Maintenance**
   - Track maintenance activities for vehicles
   - Record service dates, descriptions, and costs
   - Maintain vehicle service history

8. **Reporting System**
   - Generate PDF reports for:
     - Customer information
     - Car inventory
     - Rental transactions
     - Payment records
     - Maintenance activities

## System Architecture

### Technologies Used
- **Frontend**: Java Swing (GUI Framework)
- **Backend**: Java (Core Logic)
- **Database**: MySQL
- **Reporting**: iText PDF library
- **Date Handling**: JCalendar library
- **IDE**: NetBeans

### Database Schema
The system uses a MySQL database named `car_rental_sys` with tables for:
- Customers
- Cars
- Employees
- Rentals
- Payments
- VehicleMaintenance

## Workflow

### 1. Authentication Flow
1. User launches the application
2. Login screen appears with email and password fields
3. User can either login with existing credentials or click "Sign up" to create a new account
4. After successful authentication, user is redirected to the Dashboard

### 2. Dashboard Navigation
From the Dashboard, users can access all system modules through the menu bar:
- **System Menu**:
  - Manage Cars: Add, update, delete vehicle information
  - Manage Customers: Maintain customer records
  - Manage Rentals: Process car rental agreements
  - Manage Payments: Record and track payment transactions
  - Vehicle Maintenance: Track vehicle service activities

- **Reports Menu**:
  - Customer Report: Generate PDF report of all customers
  - Car Inventory Report: Generate PDF report of all vehicles
  - Rental Report: Generate PDF report of rental transactions for a date range
  - Payment Report: Generate PDF report of all payments
  - Maintenance Report: Generate PDF report of all maintenance activities

- **File Menu**:
  - Exit: Close the application

### 3. Vehicle Management Workflow
1. Navigate to System > Manage Cars
2. Add new vehicles by filling in details (make, model, year, license plate, rental rate)
3. Update existing vehicle information
4. Delete vehicles from inventory
5. View all vehicles in the system

### 4. Customer Management Workflow
1. Navigate to System > Manage Customers
2. Add new customers by providing personal information
3. Update customer details
4. Delete customer records
5. View all customers in the system

### 5. Rental Process Workflow
1. Navigate to System > Manage Rentals
2. Select customer from dropdown
3. Select available vehicle from dropdown
4. Select employee processing the rental
5. Set rental start and end dates
6. System automatically calculates total rental amount
7. Process the rental agreement

### 6. Payment Processing Workflow
1. Navigate to System > Manage Payments
2. Select active rental from dropdown
3. System automatically populates the amount due
4. Select payment method
5. Record payment date
6. Process the payment

### 7. Maintenance Tracking Workflow
1. Navigate to System > Vehicle Maintenance
2. Select vehicle requiring maintenance
3. Enter service date
4. Provide description of maintenance performed
5. Enter cost of maintenance
6. Record maintenance activity

### 8. Reporting Workflow
1. Navigate to Reports menu
2. Select desired report type
3. For rental reports, specify date range
4. System generates PDF report
5. Report is saved in the application directory

## Database Configuration

The system connects to a MySQL database with the following configuration:
- **Host**: localhost
- **Port**: 3306
- **Database Name**: car_rental_sys
- **Username**: root
- **Password**: isaacK@12345

*Note: These credentials are hardcoded in the DbConnection.java file and should be updated for production use.*

## Setup Instructions

### Prerequisites
1. Java Development Kit (JDK) 8 or higher
2. MySQL Server
3. NetBeans IDE (recommended)
4. Required libraries:
   - MySQL Connector/J
   - iText PDF library
   - JCalendar library

### Installation Steps
1. Clone or download the project repository
2. Create the MySQL database using the provided schema
3. Update database credentials in `DbConnection.java` if necessary
4. Add required libraries to the project
5. Build and run the project

## Project Structure

```
src/proj1/
├── BranchMgt.java
├── CarAssignment.java
├── CellHeights.java
├── CustomerManagement.java
├── Dashboard.java
├── DbConnection.java
├── EmployeeAssignmentMgt.java
├── InsuranceMgt.java
├── Login.java
├── Payment.java
├── PdfSample.java
├── Proj1.java
├── ReportGenerator.java
├── Signup.java
├── VehicleMantenance.java
└── VehicleMgt.java
```

## Key Classes

- **Login.java**: Entry point for the application with authentication
- **Dashboard.java**: Main interface with menu navigation
- **VehicleMgt.java**: Vehicle management functionality
- **CustomerManagement.java**: Customer records management
- **CarAssignment.java**: Rental processing module
- **Payment.java**: Payment transaction handling
- **VehicleMantenance.java**: Maintenance tracking
- **ReportGenerator.java**: PDF report generation
- **DbConnection.java**: Database connection management

## Security Considerations

- Passwords are stored in plain text (should be hashed in production)
- Database credentials are hardcoded (should use environment variables)
- No session management implemented

## Future Enhancements

1. Implement proper password hashing
2. Add user roles and permissions
3. Implement data validation and sanitization
4. Add data backup and recovery features
5. Improve error handling and user feedback
6. Add unit tests for core functionality
7. Implement audit logging
8. Add data export/import capabilities

## Author

Izaek Kisuule

## License

This project is proprietary and intended for educational purposes.