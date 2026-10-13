# Apache2 Service Management on Ubuntu

## Objective

Learn how to install Apache2, manage its service using `systemctl`, and troubleshoot a missing service error on Ubuntu Linux.

## Environment

- Operating System: Ubuntu Linux
- Web Server: Apache2
- Package Manager: APT
- Service Manager:systemd
- Tools: Linux Terminal, Git, GitHub

## Step 1: Update Package Information

First, I updated the package information using:

```bash
sudo apt update
```

What I learned: This command refreshes the package information from the configured Ubuntu repositories. It does not install or upgrade packages by itself.

## Step 2: Install Apache2

I installed the Apache2 web server using:

```bash
sudo apt install apache2
```

What I learned:This command installs Apache2 and the required dependencies on Ubuntu.

## Step 3: Start the Apache2 Service

After installation, I started the service:

```bash
sudo systemctl start apache2
```

What I learned: The `start` command starts the service immediately.

## Step 4: Check the Service Status

I checked whether Apache2 was running:

```bash
sudo systemctl status apache2
```

Expected result:

```text
Active: active (running)
```

This indicates that the Apache2 service is running.

## Step 5: Enable Apache2 at Boot

I enabled Apache2 to start automatically when the system boots:

```bash
sudo systemctl enable apache2
```

What I learned: The `enable` command configures the service to start automatically during boot. It does not necessarily start the service immediately.

---

## Troubleshooting: Apache2 Service Not Found

### Problem

Initially, I ran the following command to check the Apache2 service status:

```bash
sudo systemctl status apache2
```

The system returned this error:

```text
Unit apache2.service could not be found.
```

### What Does This Error Mean?

The system could not find the Apache2 service unit. One possible cause is that Apache2 has not been installed.

In my exercise, I addressed this by installing Apache2 before checking the service again.

### Solution

Step 1: Update package information

```bash
sudo apt update
```

Step 2: Install Apache2

```bash
sudo apt install apache2
```

Step 3: Start the service

```bash
sudo systemctl start apache2
```

Step 4: Check the service status again

```bash
sudo systemctl status apache2
```

Step 5: Enable the service at boot

```bash
sudo systemctl enable apache2
```

### Verification

After installing Apache2, I checked the service again using `systemctl status apache2`.

The expected status is:

```text
Active: active (running)
```

If the error continues after installation, further troubleshooting may be required to check the package installation, service name, and system logs.

### What I Learned from Troubleshooting

- How to read a Linux service error.
- Why a service may be unavailable before its software is installed.
- How to install packages using APT.
- How to manage services using `systemctl`.
- How to verify whether a service is running.

---

## Verify Apache2 in a Browser

After confirming that Apache2 is running, open the following address in the Ubuntu browser:

```text
http://localhost
```

The Apache2 Ubuntu Default Page should appear if the web server is working correctly.

## Commands Practiced

```bash
sudo apt update
sudo apt install apache2
sudo systemctl start apache2
sudo systemctl status apache2
sudo systemctl enable apache2
```

## Key Takeaways

This exercise helped me understand the basic Linux service-management workflow:

Install → Start → Check Status → Enable at Boot → Verify

I also practiced troubleshooting an error and documenting the steps taken to resolve it.

## Next Steps

- Practice stopping and restarting services.
- Explore Apache2 log files.
- Learn Linux users and groups.
- Practice file permissions.
- Learn process management and networking commands.
