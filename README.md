# DBFuzz Implementation on DAMS

## Team Members
- Sandeep Khachariya (2023UCP1628)
- Dhiraj Chouhan (2023UCP1591)

---

## Project Overview
This project implements **DBFuzz** on a vulnerable web application called **Doctor Appointment Management System (DAMS)**.

The objective was to:
- Deploy DAMS using Docker
- Configure database
- Automate login
- Crawl authenticated pages
- Perform fuzz testing
- Detect vulnerabilities/errors

---

## Technologies Used
- Python
- Selenium
- Docker
- MariaDB
- Apache
- phpMyAdmin
- DBFuzz
- BlackWidow Crawler

---

## Project Workflow

### 1. Docker Deployment
Started containers using:

```bash
cd docker/dams
sudo docker-compose up -d
