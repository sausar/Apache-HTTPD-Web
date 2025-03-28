# Apache-HTTPD-Web
Host an Apache HTTPD Web Server &amp; Deploy a CSS Template on Ubuntu
📌 Steps to Host an Apache HTTPD Web Server & Deploy a CSS Template on Ubuntu

---

✅ Step 1: Install Apache and Start the Server
1. Update package lists and install Apache 
   ```bash
   sudo apt update && sudo apt install apache2 -y
   ```
2. Enable Apache to start on boot and start it now
   ```bash
   sudo systemctl enable --now apache2
   ```
3. Check if Apache is running
   ```bash
   sudo systemctl status apache2
   ```
   - If it's running, you’ll see a **"active (running)"** status.

---

✅ **Step 2: Download and Extract the CSS Template
1. Download the template (replace URL with actual link)
   ```bash
   wget <css-template-url>
   ```
2. Install unzip utility  
   ```bash
   sudo apt install unzip -y
   ```
3. Extract the downloaded ZIP file
   ```bash
   unzip <css template.zip>
   ```
4. Check extracted files
   ```bash
   ls
   ```

---

✅ Step 3: Move Template Files to `/opt` and Deploy
1. Move extracted folder to `/opt` 
   ```bash
   sudo mv <unziped css template>/ /opt
   ```
2. Navigate to `/opt` and check files  
   ```bash
   cd /opt/
   ls
   cd <unziped css template>/
   ls
   ```
3. Copy all files to the Apache web directory
   ```bash
   sudo cp -r * /var/www/html/
   ```

---

## ✅ Step 4: Access the Website via Public IP
1. Find your public IP (for cloud instances like AWS, GCP or Azure)*
   ```bash
   curl ifconfig.me
   ```
2. Open a web browser and enter: 
   ```
   http://<your-public-ip>
   ```
   or  
   ```
   http://<your-public-ip>:80
   ```

---

✅ Important Notes:
- Make sure port 80 is open in the firewall settings of your instance (AWS Security Group).
---
