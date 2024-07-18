# Retail Management System

## Contents
1. [Introduction](#introduction)
2. [Software Needed](#software-needed)
3. [Relational Model](#relational-model)
4. [Applications](#applications)
5. [Constraints](#constraints)
6. [Triggers](#triggers)

## Introduction
In many developing countries, retail businesses still rely on traditional pen-and-paper methods, leading to inefficiencies and security risks. This project introduces a Sales Management Web Application designed for wholesale businesses to enhance efficiency and security. The lightweight web application is particularly suitable for small businesses that may find expensive alternatives less practical.

The Retail Management System (RMS) includes an administrator login with features to monitor sales, manage inventory, and register customers and suppliers. Customers can also log in to track their purchases. The RMS simplifies daily business operations, aligning with the practices adopted in many developed countries.

## Software Needed
- **Backend (Database):** MySQL version 5.7
- **Frontend (Web Technologies):** Python Jupyter Notebook

## Applications
There are two types of accounts: Administrator and Customer.

**Features for the Administrator:**
- Add and update product details by category.
- Add and update supplier details.
- Add and update customer details.
- Stock maintenance in the warehouse.
- Add new transactions offline and store payment details.
- Add and store payment details from the supplier's side.

## Constraints
- **Category Table:**
  - CID (Primary key)
  - Cname (Not null)
- **Product Table:**
  - PID (Primary key)
  - Price (Not null)
  - CID (Foreign key)
- **Customer Table:**
  - CuID (Primary key)
  - Cname (Not null)
  - Area (Not null)
  - Phone (Not null)
  - Email (Not null)
- **Supplier Table:**
  - SID (Primary key)
  - Sname (Not null)
  - Area (Not null)
  - Phone (Not null)
  - Email (Not null)
- **Payment_Customer Table:**
  - PaID (Primary key)
  - CuID (Foreign key)
- **Payment_Supplier Table:**
  - PaID (Primary key)
  - SID (Foreign key)
- **Warehouses Table:**
  - WID (Not null)
  - Area (Not null)
  - PID (Not null)
  - Quantity (Not null)
  - (WID, PID) (Primary key)
  - PID (Foreign key)

## Triggers
**Primary Triggers:**
1. **Price_trigger:**
   If the price entered is less than 0, the server will automatically input zero in the table.
2. **Quantity_trigger:**
   If the quantity is less than 0, the server will automatically input zero.
