# Popfiz Enterprise Linux Operations

## Project Overview

This project demonstrates hands-on enterprise Linux systems administration and IT operations using Azure-hosted Ubuntu Linux servers.

The environment was designed to simulate a production-style IT infrastructure where a systems administrator is responsible for server administration, network security, access control, storage, service management, monitoring, troubleshooting, and incident response.

The project follows an operational approach:

**Configure → Secure → Monitor → Troubleshoot → Remediate → Validate → Document**

---

## Business Scenario

Popfiz requires a secure and maintainable Linux infrastructure to support internal users, application services, file storage, and IT operations.

The environment consists of multiple Linux servers with different operational responsibilities.

### Server Roles

| Server | Role | Purpose |
|---|---|---|
| MGMT01 | Management Server | Administrative access and management operations |
| APP01 | Application Server | Apache web application hosting |
| FILE01 | File Server | Enterprise file storage and access control |

---

# Project Objectives

The objectives of this project were to demonstrate practical experience with:

- Linux system administration
- Server configuration and maintenance
- User and group administration
- File permissions and access control
- SSH administration
- Linux firewall configuration
- Azure Network Security Groups
- Apache web server management
- Azure managed disk administration
- Linux filesystem management
- Persistent storage configuration
- CPU and memory monitoring
- Disk I/O monitoring
- Network troubleshooting
- Service troubleshooting
- Root-cause analysis
- Incident response
- System validation and documentation

---

# Phase 1 — Infrastructure and Server Configuration

The initial phase established the Linux server environment and verified the basic infrastructure.

### Activities

- Provisioned Ubuntu Linux servers in Microsoft Azure
- Configured server roles
- Verified hostnames
- Verified operating system information
- Verified network interfaces
- Verified routing configuration
- Established administrative connectivity

### Evidence

Relevant screenshots are available in the `screenshots/` directory.

Examples:

- `app01-server.png`
- `file01-server.png`
- `mgmt01-server.png`
- `app01-system-info.png`
- `file01-system-info.png`
- `mgmt01-system-info.png`
- `hostname-system-info.png`
- `file01-network-interfaces.png`
- `file01-routing-table.png`

---

# Phase 2 — Enterprise Linux System Administration

This phase focused on day-to-day Linux administration tasks performed by a systems administrator.

### Activities

- Created and managed Linux users
- Created groups
- Assigned users to appropriate groups
- Created departmental roles
- Verified group membership
- Managed SSH services
- Used `systemctl` to inspect services
- Verified system resources
- Performed administrative account validation

### Skills Demonstrated

- `useradd`
- `groupadd`
- `usermod`
- `id`
- `groups`
- `systemctl`
- `ssh`
- `hostnamectl`
- Linux administrative commands

### Evidence

- `file01-user-accounts.png`
- `file01-group-membership.png`
- `departmental-roles-assigned.png`
- `file01-group-verification.png`
- `file01-ssh-service.png`
- `file01-system-services.png`
- `file01-sysadmin-account.png`

---

# Phase 3 — Enterprise File Permissions and Access Control

This phase demonstrated how Linux permissions can be used to protect departmental data and enforce least-privilege access.

### Activities

- Created departmental directories
- Created role-based access structures
- Assigned ownership and group permissions
- Tested authorized access
- Tested unauthorized access
- Investigated permission failures
- Used `namei` to troubleshoot directory permissions

### Security Principles

The configuration followed:

- Least privilege
- Role-based access
- Separation of departmental data
- Controlled group membership
- Permission validation

### Evidence

- `departmental-folders-created.png`
- `departmental-roles-assigned.png`
- `file-permission-denied.png`
- `namei-permission-analysis.png`
- `file-access-test.png`

---

# Phase 4 — Server Security and Service Management

This phase focused on protecting the application server and managing its services.

### Activities

- Configured UFW
- Applied default firewall policies
- Controlled inbound traffic
- Configured HTTP access
- Managed SSH access
- Installed and configured Apache
- Verified Apache service status
- Verified listening ports
- Tested the application locally and remotely

### Security Controls

The application server was configured with:

```text
Default inbound policy: DENY
Default outbound policy: ALLOW
HTTP: TCP/80
SSH: TCP/22

# Evidence and Screenshots

The following screenshots provide visual evidence of the implementation, testing, troubleshooting, and validation performed throughout the project.

All screenshots are stored in the [`screenshots/`](./screenshots/) directory.

---

## Phase 1 — Infrastructure and Server Configuration

### APP01 Server

![APP01 Server](./screenshots/app01-server.png)

### FILE01 Server

![FILE01 Server](./screenshots/file01-server.png)

### MGMT01 Server

![MGMT01 Server](./screenshots/mgmt01-server.png)

### APP01 System Information

![APP01 System Information](./screenshots/app01-system-info.png)

### FILE01 System Information

![FILE01 System Information](./screenshots/file01-system-info.png)

### MGMT01 System Information

![MGMT01 System Information](./screenshots/mgmt01-system-info.png)

### Hostname and System Information

![Hostname System Information](./screenshots/hostname-system-info.png)

---

## Phase 2 — Linux System Administration

### User Accounts

![FILE01 User Accounts](./screenshots/file01-user-accounts.png)

### Group Membership

![FILE01 Group Membership](./screenshots/file01-group-membership.png)

### Departmental Roles

![Departmental Roles](./screenshots/departmental-roles-assigned.png)

### SSH Service

![SSH Service](./screenshots/file01-ssh-service.png)

### System Services

![System Services](./screenshots/file01-system-services.png)

### Group Verification

![Group Verification](./screenshots/file01-group-verification.png)

### Administrative Account

![Administrative Account](./screenshots/file01-sysadmin-account.png)

---

## Phase 3 — File Permissions and Access Control

### Departmental Folders

![Departmental Folders](./screenshots/departmental-folders-created.png)

### Permission Denied Test

![Permission Denied](./screenshots/file-permission-denied.png)

### Permission Analysis with namei

![namei Permission Analysis](./screenshots/namei-permission-analysis.png)

### Access Control Test

![File Access Test](./screenshots/file-access-test.png)

---

## Phase 4 — Security and Service Management

### UFW Firewall

![APP01 UFW Firewall](./screenshots/app01-ufw-firewall.png)

### Apache Service

![Apache Service](./screenshots/app01-apache-service.png)

### Apache Web Portal

![APP01 Web Portal](./screenshots/app01-web-portal.png)

### APP01 System Services

![APP01 System Services](./screenshots/app01-system-services.png)

---

## Phase 5 — Enterprise Storage Administration

### Disk Partitioning

![FILE01 Disk Partitioning](./screenshots/file01-disk-partitioning.png)

### Data Disk Mount

![FILE01 Data Disk Mounted](./screenshots/file01-data-disk-mounted.png)

### Persistent Storage Test

![FILE01 Data Storage Test](./screenshots/file01-data-storage-test.png)

---

## Phase 6 — Monitoring and Troubleshooting

### Memory Baseline

![FILE01 Memory Baseline](./screenshots/file01-memory-baseline.png)

### CPU Monitoring

![FILE01 CPU Monitoring](./screenshots/file01-cpu-monitoring.png)

### Memory Validation

![FILE01 Memory Check](./screenshots/file01-memory-check.png)

---

## Network Diagnostics

### Network Interfaces

![Network Interfaces](./screenshots/file01-network-interfaces.png)

### Routing Table

![Routing Table](./screenshots/file01-routing-table.png)

---

## Helpdesk and IT Operations

### Helpdesk Support

![Helpdesk Support](./screenshots/helpdesk-support.png)