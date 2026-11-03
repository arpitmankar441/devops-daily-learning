# EC2 – Deploy a Web Server

## Objective

Install a web server on an EC2 Linux instance and access the test page through a browser.

## Part A – NGINX on Ubuntu

### 1. Update package information

```bash
sudo apt update
```

### 2. Install NGINX

```bash
sudo apt install nginx -y
```

### 3. Start and enable NGINX

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

### 4. Check service status

```bash
sudo systemctl status nginx
```

### 5. Allow web traffic

In the EC2 security group, add inbound rules for:
- HTTP – TCP 80 – source appropriate for your test (for a public demo, `0.0.0.0/0`).
- HTTPS – TCP 443 – only if HTTPS is configured.

If UFW is enabled on the Ubuntu instance, the training notes use:

```bash
sudo ufw allow 'Nginx Full'
sudo ufw status
```

### 6. Add a simple page

```bash
sudo nano /var/www/html/index.html
```

Example HTML:

```html
<h1>Hello from NGINX on AWS EC2</h1>
<p>My first cloud web server.</p>
```

Save the file and visit `http://PUBLIC_IP_ADDRESS` in a browser.

## Part B – Apache HTTPD on Amazon Linux / RHEL-family systems

The following commands are for systems that use `yum` and `firewalld`; commands may differ on newer distributions.

### 1. Update packages

```bash
sudo yum update -y
```

### 2. Install HTTPD

```bash
sudo yum install httpd -y
```

### 3. Start and enable HTTPD

```bash
sudo systemctl start httpd
sudo systemctl enable httpd
```

### 4. Configure firewalld if it is active

```bash
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --permanent --add-service=https
sudo firewall-cmd --reload
```

### 5. Create a test page

```bash
cd /var/www/html
sudo nano index.html
```

Example:

```html
<h1>Hello from Apache HTTPD on AWS EC2</h1>
```

Then visit `http://PUBLIC_IP_ADDRESS`.

## Troubleshooting

- Check the EC2 instance is running.
- Check the security group allows TCP 80.
- Check the service with `systemctl status nginx` or `systemctl status httpd`.
- Check the instance has a route and public address if accessing it from the internet.
- Check the operating system firewall if enabled.

## Cleanup

Stop or terminate resources when finished. Remember that stopping an instance does not necessarily remove every charge, such as attached storage or allocated public IPv4 resources.
