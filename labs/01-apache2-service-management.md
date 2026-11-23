# Lab 01 — Apache2 Service Management

## 1. Overview

This lab demonstrates how to install, start, check the status of, test and stop the Apache2 web server using Ubuntu Linux.

## 2. Objective

The objective of this practical lab is to understand basic Linux service management and package installation using `apt` and `systemctl`.

## 3. Environment

- Operating System: Ubuntu Linux
- Virtualization: UTM Virtual Machine
- Web Server: Apache2
- Terminal: Ubuntu Terminal

## 4. Commands Used

| Command | Description |
|---|---|
| `sudo apt update` | Updates package information |
| `sudo apt install apache2` | Installs Apache2 |
| `sudo systemctl status apache2` | Checks Apache2 service status |
| `sudo systemctl start apache2` | Starts Apache2 |
| `sudo systemctl stop apache2` | Stops Apache2 |
| `sudo systemctl enable apache2` | Enables Apache2 to start at boot |
| `curl -I http://localhost` | Tests the local web server response |

## 5. Practical Implementation

### Step 1 — Update Package Information

```bash
sudo apt update
```

Updated the package information before installing Apache2.

### Step 2 — Install Apache2

```bash
sudo apt install apache2
```

Installed the Apache2 web server using the APT package manager.

### Step 3 — Check Initial Service Status

```bash
sudo systemctl status apache2 --no-pager
```

Checked the initial status of the Apache2 service.

### Step 4 — Start Apache2

```bash
sudo systemctl start apache2
```

Started the Apache2 service.

### Step 5 — Verify Active Status

```bash
sudo systemctl status apache2 --no-pager
```

Verified that the Apache2 service was running.

Expected status:

```text
Active: active (running)
```

### Step 6 — Test the Local Web Server

```bash
curl -I http://localhost
```

Tested the local Apache2 web server using curl.

Expected response includes:

```text
HTTP/1.1 200 OK
```

### Step 7 — Stop Apache2

```bash
sudo systemctl stop apache2
```

Stopped the Apache2 service.

### Step 8 — Verify Final Service Status

```bash
sudo systemctl status apache2 --no-pager
```

Verified that the Apache2 service had stopped.

Expected status:

```text
Active: inactive (dead)
```

## 6. Screenshots

Screenshots for this practical lab are stored in:

`screenshots/lab-01-apache2/`

| No. | Screenshot |
|---|---|
| 1 | `01-apache-installation.png` |
| 2 | `02-apache-initial-status.png` |
| 3 | `03-apache-service-start.png` |
| 4 | `04-apache-active-status.png` |
| 5 | `05-apache-localhost-test.png` |
| 6 | `06-apache-service-stop.png` |
| 7 | `07-apache-final-status.png` |

## 7. Troubleshooting

### Issue 1 — Apache2 service not found

Error:

```text
Unit apache2.service could not be found.
```

Solution:

```bash
sudo apt update
sudo apt install apache2
```

### Issue 2 — Curl command not found

Error:

```text
Command 'curl' not found
```

Solution:

```bash
sudo apt install curl -y
```

Then test again:

```bash
curl -I http://localhost
```

## 8. Key Learnings

Through this lab, I learned:

- How to update package information using APT.
- How to install Apache2 on Ubuntu.
- How to check Linux service status using systemctl.
- How to start and stop a Linux service.
- How to enable a service at system startup.
- How to test a local web server using curl.
- How to identify and resolve basic installation issues.

## 9. Conclusion

Successfully practised Apache2 installation and service management in Ubuntu Linux.

This practical exercise helped me understand Linux package management, service control and basic web server troubleshooting.
