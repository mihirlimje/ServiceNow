# ServiceNow Visitor Management Application

## Overview
This ServiceNow application provides a comprehensive visitor management system for tracking and managing visitors within an organization.

## Features
- **Visitor Registration**: Register visitors with personal information
- **Visit Scheduling**: Schedule visits with specific dates and times
- **Check-in/Check-out**: Track visitor arrival and departure times
- **Host Management**: Assign host employees to visitors
- **Status Tracking**: Monitor visitor status (Scheduled, Checked In, Checked Out, Cancelled)
- **Company Information**: Track visitor company details

## Table Structure

### Visitor Table (x_vm_visitor_mgmt_visitor)
The main visitor table includes the following fields:

#### Visitor Information
- **Visitor Number** (number): Auto-generated unique identifier
- **First Name** (first_name): Visitor's first name
- **Last Name** (last_name): Visitor's last name
- **Email** (email): Visitor's email address
- **Phone** (phone): Visitor's phone number
- **Company** (company): Visitor's company/organization

#### Visit Details
- **Visit Date** (visit_date): Scheduled date of visit
- **Check In Time** (check_in_time): Actual check-in timestamp
- **Check Out Time** (check_out_time): Actual check-out timestamp
- **Purpose of Visit** (purpose_of_visit): Reason for the visit
- **Host Employee** (host_employee): Reference to sys_user table
- **Status** (status): Current visit status (choice field)

#### Status Choices
- **Scheduled**: Visit is scheduled but not yet started
- **Checked In**: Visitor has arrived and checked in
- **Checked Out**: Visitor has departed
- **Cancelled**: Visit was cancelled

## Installation

1. Import the XML files into your ServiceNow instance
2. The application will be available as "Visitor Management" in the application navigator
3. Access the Visitors module to manage visitor records

## Files Structure

- `sys_app.xml`: Application definition
- `x_vm_visitor_mgmt_table.xml`: Visitor table definition
- `x_vm_visitor_mgmt_dictionary.xml`: Table dictionary
- `x_vm_visitor_mgmt_fields.xml`: Field definitions
- `x_vm_visitor_mgmt_choices.xml`: Status field choices
- `x_vm_visitor_mgmt_form.xml`: Form configuration
- `x_vm_visitor_mgmt_sections.xml`: Form sections and elements
- `x_vm_visitor_mgmt_list.xml`: List view configuration
- `x_vm_visitor_mgmt_module.xml`: Module definition
- `x_vm_visitor_mgmt_menu.xml`: Application menu

## Usage

1. Navigate to the "Visitor Management" application
2. Click on "Visitors" module to see all visitor records
3. Click "New" to register a new visitor
4. Fill in visitor information and visit details
5. Save the record
6. Use the status field to track visitor progress through check-in and check-out

## Security

The application follows ServiceNow's standard security model. Access can be controlled through:
- Role-based access control
- Field-level security
- Record-level security (ACLs)

## Extensibility

The application can be extended with:
- Additional visitor fields
- Custom workflows for approval processes
- Integration with badge printing systems
- Email notifications for hosts
- Visitor kiosk interface
- Reporting and analytics
