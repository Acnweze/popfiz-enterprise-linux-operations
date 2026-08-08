# Popfiz Enterprise Linux Operations

![Azure](https://img.shields.io/badge/Microsoft%20Azure-Infrastructure-blue)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-orange)
![Security](https://img.shields.io/badge/Security-UFW%20%7C%20NSG-red)
![Monitoring](https://img.shields.io/badge/Monitoring-System%20Performance-green)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

## Project Overview

The **Popfiz Enterprise Linux Operations** project is a hands-on systems administration and IT operations environment built on Microsoft Azure.

The project simulates the responsibilities of an enterprise Systems Administrator supporting application servers, file services, management infrastructure, network security, storage, users, services, and system performance.

The environment was designed around a practical operational lifecycle:

> **Configure → Secure → Monitor → Troubleshoot → Remediate → Validate → Document**

The project demonstrates not only how systems are configured, but also how an administrator investigates problems, identifies root causes, applies controlled remediation, and validates system recovery.

---

# Infrastructure Architecture

The environment contains three Ubuntu Linux servers with defined operational responsibilities.

| Server | Role | Primary Responsibilities |
|---|---|---|
| **MGMT01** | Management Server | Administrative access and IT operations |
| **APP01** | Application Server | Apache web service and application hosting |
| **FILE01** | File Server | Enterprise storage, permissions, and file access |

### Core Technologies

- Microsoft Azure
- Azure Virtual Machines
- Azure Virtual Network
- Azure Network Security Groups
- Azure Managed Disks
- Ubuntu Linux
- Apache HTTP Server
- OpenSSH
- UFW
- systemd
- Linux users and groups
- Linux filesystem permissions
- `fdisk`
- `findmnt`
- `top`
- `ps`
- `uptime`
- `free`
- `df`
- `iostat`
- `ss`
- `ip`
- `curl`

---

# Project Objectives

The project was designed to demonstrate practical ability in:

- Enterprise Linux administration
- Server configuration and maintenance
- User and group management
- File permissions and access control
- SSH administration
- Firewall configuration
- Azure network security
- Apache service management
- Storage administration
- Persistent filesystem configuration
- System monitoring
- Performance troubleshooting
- Network troubleshooting
- Root-cause analysis
- Incident response
- Technical validation and documentation

---

# Phase 1 — Infrastructure and Server Configuration

## Objective

Establish the Linux server environment and verify that each server is correctly configured and reachable.

### Tasks Completed

- Provisioned Ubuntu Linux servers in Azure
- Defined server roles
- Verified hostnames
- Verified operating system information
- Verified network interfaces
- Verified routing configuration
- Established administrative connectivity

## Server Identification

### APP01

![APP01 Server](./screenshots/app01-server.png)

### FILE01

![FILE01 Server](./screenshots/file01-server.png)

### MGMT01

![MGMT01 Server](./screenshots/mgmt01-server.png)

## System Information

### APP01

![APP01 System Information](./screenshots/app01-system-info.png)

### FILE01

![FILE01 System Information](./screenshots/file01-system-info.png)

### MGMT01

![MGMT01 System Information](./screenshots/mgmt01-system-info.png)

### Hostname and System Information

![Hostname System Information](./screenshots/hostname-system-info.png)

---

# Phase 2 — Enterprise Linux System Administration

## Objective

Demonstrate the day-to-day administrative tasks performed by a Linux Systems Administrator.

### Tasks Completed

- Created Linux user accounts
- Created security groups
- Assigned users to groups
- Created departmental roles
- Verified group membership
- Managed SSH
- Inspected system services with `systemctl`
- Verified administrative accounts
- Checked system resources

## User and Group Administration

### User Accounts

![FILE01 User Accounts](./screenshots/file01-user-accounts.png)

### Group Membership

![FILE01 Group Membership](./screenshots/file01-group-membership.png)

### Departmental Roles

![Departmental Roles](./screenshots/departmental-roles-assigned.png)

### Group Verification

![Group Verification](./screenshots/file01-group-verification.png)

## Service Administration

SSH and system services were inspected using `systemctl` and related Linux administration commands.

### SSH Service

![SSH Service](./screenshots/file01-ssh-service.png)

### System Services

![System Services](./screenshots/file01-system-services.png)

### Administrative Account

![Administrative Account](./screenshots/file01-sysadmin-account.png)

---

# Phase 3 — Enterprise File Permissions and Access Control

## Objective

Implement role-based access to departmental data using Linux ownership, groups, and filesystem permissions.

### Tasks Completed

- Created departmental directories
- Created departmental roles
- Assigned group ownership
- Applied Linux permissions
- Tested authorized access
- Tested unauthorized access
- Investigated permission failures
- Used `namei` to analyze directory permissions

## Departmental File Structure

![Departmental Folders](./screenshots/departmental-folders-created.png)

## Role Assignment

![Departmental Roles](./screenshots/departmental-roles-assigned.png)

## Permission Testing

An unauthorized access attempt was deliberately tested to verify that the permission model was enforcing the intended restrictions.

![Permission Denied](./screenshots/file-permission-denied.png)

## Permission Troubleshooting

`namei` was used to examine the permissions of each directory component in the path.

![namei Permission Analysis](./screenshots/namei-permission-analysis.png)

## Access Validation

![File Access Test](./screenshots/file-access-test.png)

### Security Principles Demonstrated

- Least privilege
- Role-based access control
- Group-based permissions
- Separation of departmental data
- Access validation
- Permission troubleshooting

---

# Phase 4 — Server Security and Service Management

## Objective

Secure the application server and manage the services required to provide application access.

### Tasks Completed

- Configured UFW
- Applied default inbound restrictions
- Allowed required services
- Managed SSH access
- Configured HTTP access
- Installed Apache
- Enabled Apache
- Verified Apache service status
- Verified listening ports
- Tested the application

## UFW Firewall

The application server was configured with a restrictive inbound firewall policy.

```text
Default: deny incoming
Default: allow outgoing

HTTP: TCP/80
SSH: TCP/22