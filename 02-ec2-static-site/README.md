## 📘 Overview & Approach

A Free Tier **EC2 instance** running Ubuntu was deployed in the **public subnet** so it receives a public IP and can host a public-facing website.  
I installed **Nginx** using a simple user-data script and replaced the default index page with a static HTML resume.  
To ensure security, I allowed only HTTP (port 80) from anywhere and restricted SSH (port 22) to my personal IP. Password authentication was disabled, and only key-based authentication is allowed.

This setup follows AWS recommendations for lightweight static content hosting.
