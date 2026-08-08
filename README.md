# Popfiz Enterprise Linux Operations

## Project Overview

This project demonstrates hands-on enterprise Linux systems administration and IT operations using Microsoft Azure-hosted Ubuntu Linux servers.

The environment was designed to simulate a production-style IT infrastructure where a Systems Administrator is responsible for server administration, security, user access, storage, service management, monitoring, troubleshooting, and incident response.

The project follows a practical operational lifecycle:

**Configure → Secure → Monitor → Troubleshoot → Remediate → Validate → Document**

---

# Business Scenario

Popfiz requires a secure and maintainable Linux infrastructure to support application services, file storage, administrative operations, and internal users.

Three Ubuntu Linux servers were deployed in Microsoft Azure, with each server assigned a specific operational role.

| Server | Role | Responsibility |
|---|---|---|
| MGMT01 | Management Server | Administrative and management operations |
| APP01 | Application Server | Apache web application hosting |
| FILE01 | File Server | Enterprise file storage and access control |

---

# Infrastructure

The environment includes:

- Microsoft Azure Virtual Machines
- Azure Virtual Network
- Azure Network Security Groups
- Azure Managed Disks
- Ubuntu Linux
- Apache HTTP Server
- OpenSSH
- UFW Firewall
- Linux users and groups
- Linux filesystem permissions
- systemd service management
- Linux monitoring and troubleshooting utilities

---

# Project Objectives

The project was designed to demonstrate practical experience with:

- Linux system administration
- Server configuration and maintenance
- User and group management
- File permissions and access control
- SSH administration
- Network security
- Azure Network Security Groups
- Linux firewall configuration
- Apache web server management
- Storage administration
- Persistent filesystem configuration
- System monitoring
- CPU troubleshooting
- Disk I/O monitoring
- Network diagnostics
- Service troubleshooting
- Root-cause analysis
- Incident response
- Technical documentation

---

# Phase 1 — Infrastructure and Server Configuration

## Objective

Establish the Linux infrastructure and verify the configuration and connectivity of each server.

## Tasks Performed

- Provisioned Ubuntu Linux virtual machines in Azure
- Defined server roles
- Verified hostnames
- Verified operating system information
- Verified network interfaces
- Verified routing configuration
- Verified administrative access

---

## APP01 Server

![APP01 Server](./screenshots/APP01.png)

---

## FILE01 Server

![FILE01 Server](./screenshots/FILE01.png)

---

## MGMT01 Server

![MGMT01 Server](./screenshots/MGMT01.png)

---

## APP01 Operating System Information

![APP01 Operating System](./screenshots/APP01%20uname.png)

---

## FILE01 Operating System Information

![FILE01 Operating System](./screenshots/FILE01%20uname.png)

---

## MGMT01 Operating System Information

![MGMT01 Operating System](./screenshots/MGMT01%20uname.png)

---

## Hostname Verification

The server hostname and operating system configuration were verified using `hostnamectl`.

![Hostname Verification](./screenshots/hostnamectl.png)

---

## Network Interface Verification

Network interfaces and assigned IP addresses were inspected using `ip addr`.

![Network Interfaces](./screenshots/ip%20addr.png)

---

## Routing Verification

The routing table was verified using `ip route`.

![Routing Table](./screenshots/ip%20route.png)

---

# Phase 2 — Enterprise Linux System Administration

## Objective

Demonstrate the day-to-day Linux administration activities performed by a Systems Administrator.

## Tasks Performed

- Created Linux user accounts
- Created security groups
- Assigned users to groups
- Created departmental roles
- Verified group membership
- Managed SSH
- Inspected system services
- Verified administrative accounts
- Checked system resources

---

## User Account Administration

Linux user accounts were created and verified on FILE01.

![FILE01 User Accounts](./screenshots/FILE01%20USER%20ACCOUNTS.png)

---

## Group Administration

Linux groups were created to support role-based access control.

![FILE01 Group Check](./screenshots/FILE01%20GROUP%20CHECK.png)

---

## Departmental Role Assignment

Departmental users and groups were configured according to their operational roles.

![Departmental Roles](./screenshots/creating%20department%20and%20assigning%20roles.png)

---

## Group Membership Verification

Group memberships were verified to ensure users had the appropriate access.

![Group Verification](./screenshots/sysadmin%20verify%20groups.png)

---

## SSH Service Administration

The SSH service was inspected as part of remote server administration.

![SSH Service](./screenshots/sysadmin%20ssh%20service.png)

---

## System Service Management

Linux services were inspected using `systemctl`.

![System Services](./screenshots/sysadmin%20systemctl%20list%20unit.png)

---

## System Resource Validation

System memory was checked during routine administration.

![System Memory](./screenshots/sysadmin%20free-h.png)

---

## Administrative Account

The administrative account configuration was verified.

![System Administrator](./screenshots/%5Bsysadmin%40FILE01.png)

---

# Phase 3 — Enterprise File Permissions and Access Control

## Objective

Implement role-based access to departmental data using Linux ownership, groups, and filesystem permissions.

## Tasks Performed

- Created departmental directories
- Created departmental access groups
- Assigned ownership
- Applied Linux permissions
- Tested authorized access
- Tested unauthorized access
- Investigated permission failures
- Used `namei` to troubleshoot directory permissions

---

## Departmental Folder Structure

Departmental folders were created to organize enterprise data.

![Departmental Folders](./screenshots/creating%20departmental%20folders.png)

---

## Permission Analysis

The `namei` command was used to inspect permissions across each directory in a file path.

![namei Permission Analysis](./screenshots/namei.png)

---

## Unauthorized Access Test

An unauthorized access attempt was performed to confirm that the configured permissions were enforcing the intended restrictions.

![Permission Denied](./screenshots/permission%20denied.png)

---

## Access Validation

File access was tested to confirm the expected permissions for authorized users.

![Access Test](./screenshots/test%20access.png)

---

## Security Principles Demonstrated

- Least privilege
- Role-based access control
- Group-based permissions
- Separation of departmental data
- Controlled access
- Permission validation
- Permission troubleshooting

---

# Phase 4 — Server Security and Service Management

## Objective

Secure APP01, manage its services, and validate the application server.

## Tasks Performed

- Configured UFW firewall
- Applied default deny inbound policy
- Allowed required HTTP traffic
- Managed SSH access
- Installed Apache
- Started Apache
- Verified Apache service status
- Inspected system services
- Tested the web application

---

## 4.1 UFW Firewall Configuration

UFW was configured to control inbound traffic to APP01.

The server was configured with:

```text
Default incoming: DENY
Default outgoing: ALLOW

Allowed services:

SSH  - TCP/22
HTTP - TCP/80

