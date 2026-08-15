# Baraka Mini Mart — Odoo ERP Implementation


## Project Overview

Baraka Mini Mart is a small retail business that previously relied on separate notebooks and manual processes to manage sales, inventory, supplier transactions, customer credit, and financial records.

This project involved analysing the existing business processes and implementing an integrated Odoo 19 Community Edition ERP system to centralise these operations.

The implementation covers:

- Point of Sale (POS)
- Purchasing
- Inventory Management
- Accounting
- Reporting
- Customer and Supplier Management through Odoo Contacts
- User access and role management

The project was approached as an ERP implementation exercise, beginning with business-process analysis and requirements gathering before moving into ERP module mapping, future-state process design, system configuration, testing, and user documentation.

## Business Problem

Before the ERP implementation, Baraka Mini Mart relied heavily on multiple manual records, including sales, inventory, credit, and supplier notebooks.

This created several operational challenges:

- Difficulty monitoring current stock levels
- Difficulty tracking products approaching expiry
- Limited visibility into daily sales performance
- Difficulty identifying best-selling products
- Manual tracking of customer credit
- Difficulty tracking amounts owed to suppliers
- Separation of operational information across multiple notebooks
- Manual compilation of records for accounting and reporting

The objective was therefore not simply to digitise individual tasks, but to create a single system of record through which transactions could flow between the relevant business functions.

## Project Objectives

The implementation aimed to provide Baraka Mini Mart with a system capable of:

1. Recording sales digitally through Point of Sale.
2. Supporting Cash, M-Pesa/Mobile Payment, and customer credit transactions.
3. Maintaining real-time inventory records.
4. Supporting product expiry tracking.
5. Supporting stock replenishment and reorder management.
6. Managing purchasing and supplier transactions.
7. Tracking customer receivables.
8. Tracking supplier payables.
9. Providing management with operational and financial reporting.
10. Replacing duplicated manual record keeping with an integrated workflow.
11. Providing role-appropriate access for the Manager, Cashier, Storekeeper, and Shop Attendant.

## My Role

My work covered:

- Business requirements analysis
- Process discovery
- As-Is workflow documentation
- Business data identification
- ERP module mapping
- Future-State process design
- Odoo module configuration
- User and role configuration
- POS configuration
- Purchasing configuration
- Inventory configuration
- Accounting configuration
- Testing and validation
- User documentation
- Training/adoption documentation

The emphasis was on translating business requirements into an integrated ERP workflow rather than developing custom software.

# Business Process Transformation

## As-Is Process

The original operating model relied heavily on separate manual records.
Information was recorded separately across different business activities, making it difficult to maintain a single, up-to-date view of the business.

## Future-State Process

The redesigned process uses Odoo as the central system of record.
The future-state design follows the principle that each transaction should be entered once, at its source, with the resulting information becoming available to the relevant business functions.

# ERP Applications Implemented

## 1. Point of Sale

The Odoo POS system was configured to support Baraka Mini Mart's retail sales process.

The implementation supports:

- Walk-in sales
- Phone/WhatsApp orders handled through the POS
- Cash payments
- Mobile Payments
- Customer Account / credit sales
- Customer-linked transactions
- Individual user identification
- Receipt generation when required

A completed POS transaction also contributes to the wider inventory and accounting workflow.

### Evidence

See: Applications/POS/

## 2. Purchasing

The purchasing workflow was configured to replace the informal process of ordering from suppliers and recording transactions manually.

The implemented workflow is:

Request for Quotation
        ↓
Purchase Order
        ↓
Goods Receipt
        ↓
Inventory Updated
        ↓
Vendor Bill
        ↓
Accounts Payable

The system allows the Manager to create and approve purchases, the Storekeeper to confirm goods received, and supplier bills to be recorded against the relevant purchase.

### Evidence

See:Applications/Purchasing/

## 3. Inventory Management

Inventory was configured to provide a central view of stock levels and support stock-control activities.

The implementation includes:

- Current stock visibility
- Product inventory records
- Lot/expiry tracking where applicable
- Minimum and maximum stock levels
- Replenishment management
- Stock updates resulting from purchases and sales

This replaces the need for a separate inventory notebook.

### Evidence

See:Applications/Inventory/

## 4. Accounting

Accounting was implemented as the financial layer supporting the operational workflows.

The accounting setup supports the recording and monitoring of:

- Customer receivables
- Supplier payables
- Customer credit transactions
- Vendor bills
- Payment transactions
- Financial records generated from business transactions

Accounting also provides the financial information required for management review and external accounting activities.

### Community Edition Consideration

The project was implemented using Odoo 19 Community Edition.

Because the standard Enterprise Accounting application was not being used, the accounting functionality was approached using a Community-compatible solution.

This project therefore also demonstrates working within the functional and technical constraints of an Odoo Community implementation.

### Evidence

See:Applications/Accounting/

---

## 5. Reporting

Reporting provides management with visibility into operational and financial activity.

The implementation includes reporting capabilities covering areas such as:

- Sales analysis
- Sales by product/category
- Inventory information
- Purchasing activity
- Accounting information
- Customer receivables
- Supplier payables

### Evidence

See:Applications/Reporting/

# Supporting Components

## Customer and Supplier Management

Odoo Contacts provides the underlying records used throughout the system.

Customer and supplier information is connected to operational transactions such as:

- POS sales
- Customer credit
- Purchase orders
- Vendor bills
- Receivables
- Payables

Contacts therefore functions as a supporting component of the overall ERP rather than as a standalone business application.

## User and Role Management

The system was designed around the operational roles identified during the business analysis:

Manager - Purchasing, approvals, bills, credit oversight, management review
Cashier - POS sales and payment processing
Storekeeper - Receiving goods and inventory management
Shop Attendant - Stock monitoring and shelf replenishment

Each user operates through an individual account, allowing activity to be associated with the responsible employee.

# Implementation Documentation

The project documentation is organised into four main areas.

### Business Analysis

Contains:

- Business discovery
- Existing workflows
- Business data inventory
- ERP module mapping
- Future-state workflow design

See:Business analysis/

### Odoo Implementation

Contains:

- Odoo 19 configuration checklist
- Configured applications
- System settings
- User and access configuration
- Implementation details

See:Odoo implementation/

### User Documentation

Contains the user manual prepared for the operational users of the system.

See:User documentation/

### Application Evidence

Contains screenshots from the configured Odoo environment demonstrating the implemented functionality.

See:Applications/

# Technology Stack

| Technology | Purpose |
|---|---|
| Odoo 19 Community Edition | ERP platform |
| PostgreSQL | Odoo database |
| Linux / Ubuntu Server | Server environment |
| Nginx | Reverse proxy / web server layer |
| Docker | Containerised deployment components |
| Git / GitHub | Version control and portfolio documentation |

# Key Outcomes

The implementation transformed Baraka Mini Mart's fragmented manual processes into an integrated ERP workflow.

The resulting system provides a centralised environment for:

- Retail sales
- Purchasing
- Inventory management
- Customer credit
- Supplier transactions
- Financial records
- Management reporting

The implementation also produced structured business-process documentation and a user manual to support adoption.

## Disclaimer

This repository is a portfolio representation of an ERP implementation project.

Any customer, supplier, employee, transaction, financial, or other operational information included in screenshots or examples should be treated as demonstration data and should not be interpreted as confidential production data.
