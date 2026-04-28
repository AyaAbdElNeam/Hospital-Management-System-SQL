# Hospital-Management-System-SQL
Project Overview
This project involves the design and implementation of a comprehensive relational database for a modern hospital environment using SQL Server. The system is engineered to streamline healthcare operations by integrating patient care, staff management, financial tracking, and logistical support into a unified data architecture.

Database Architecture
The schema is built around several interconnected modules to ensure high data integrity and operational efficiency:

1. Human Resources & Access Control
Employee Management: A central EMPLOYEES table stores core staff data, utilizing computed columns for full names, age calculation, and formatted contact strings.

Role-Based Access: Specialized tables for DOCTORS, NURSES, TECHNICIANS, and RECEPTIONISTS inherit from the main employee table, while a Roles and Users system manages secure login credentials.

2. Clinical Operations
Patient Records: The PATIENTS table captures detailed demographics, insurance information, and medical history.

Appointments & Documentation: Tracks the full lifecycle of a patient visit, from scheduling in APPOINTMENTS to clinical findings in Medical_Records.

Diagnostics & Treatment: Dedicated tables for Lab_Tests, TREATMENT, and Prescription ensure every medical action is logged and traceable.

3. Logistical & Support Services
Pharmacy & Inventory: Manages MEDICINE stock levels, types, and expiration dates, linked directly to patient prescriptions.

Facility Management: Tracks ROOMS availability and Room_Assignments for patients and staff.

Emergency Services: Includes a specialized module for AMBULANCE tracking and Ambulance_Log for emergency response management.

Technical Features
Automated Data Integrity: Implements complex CHECK constraints (e.g., ensuring salaries > 0, valid blood types, and chronological order of dates).

Advanced Referential Integrity: Utilizes ON DELETE CASCADE and ON UPDATE CASCADE to maintain consistency across 20+ related tables.

Financial Logic: The INVOICES table features a computed outstanding_Amount column to automatically calculate balances based on total costs, insurance coverage, and payments.

Transactional Logging: A Hospital_Transactions_Log captures critical events (Patient/Room/Employee interactions) for auditing and security.

Files in this Repository
Hosp_creation.sql: Full DDL script for database, table, and constraint creation.

ProjectERD.jpg: Visual representation of the Entity Relationship Diagram.

Developed by: Aya Abdelnaem Mahmoud
Strategic Data Analyst | Insight Architect
