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
