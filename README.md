# NLC Integrated Gate Pass System (IGPS)

![Live Status](https://img.shields.io/badge/Status-Live-success)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Flask](https://img.shields.io/badge/Flask-Backend-black)
![MySQL](https://img.shields.io/badge/MySQL-Database-orange)

A Full-Stack, Role-Based Access Control (RBAC) web application designed to digitize and streamline the process of issuing, approving, and verifying gate passes for employees, visitors, and materials at NLC India Limited.

## 🚀 Live Demo

You can test the fully functional live application here:
**[Live Website](https://nlc-integrated-gatepass-system.onrender.com)**

> **Note on Performance:** The live demo is hosted on free tiers (Render & Neon.tech). If the application hasn't been accessed in the last 15 minutes, the server goes to sleep. **The initial page load may take 40-50 seconds** to wake the server up. Subsequent requests will be extremely fast!

### Demo Credentials
To explore the different role-based dashboards, you can log in using any of the following test accounts:

| Role | Email | Password |
| :--- | :--- | :--- |
| **Admin** | `admin@nlcindia.com` | `password123` |
| **Manager** | `manager@nlcindia.com` | `password123` |
| **Security** | `security@nlcindia.com` | `password123` |
| **Employee** | `employee@nlcindia.com` | `password123` |

---

## ✨ Key Features

- **Role-Based Dashboards**: Distinct, secure portals tailored for Employees, Managers, Security Personnel, and System Admins.
- **Unified Timeline Generation**: Merges diverse database models (Gate Passes, Visitor Passes, Material Passes) into a single, chronologically sorted API stream.
- **Secure Authentication**: Built entirely with JWT (JSON Web Tokens) and Werkzeug password hashing.
- **Non-Destructive Data Retention**: Implements soft-deletion (is_active toggling) to maintain historical database integrity for security audits.
- **Dynamic Frontend**: A Single Page Application (SPA) feel built with Vanilla JavaScript and dynamic DOM manipulation.

## 🛠️ Technology Stack

* **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6)
* **Backend**: Python, Flask, Flask-JWT-Extended
* **Database Engine**: MySQL / PostgreSQL
* **ORM**: SQLAlchemy
* **Deployment**: Render (Web Service) + Neon.tech (Serverless PostgreSQL)

## 💻 Running Locally

If you want to run this project on your own machine:

1. **Clone the repository**
   ```bash
   git clone https://github.com/Zuko-Lee/nlc-integrated-gatepass-system.git
   cd nlc-integrated-gatepass-system
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up Environment Variables**
   Create a `.env` file in the root directory:
   ```env
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_password
   DB_NAME=igps_db
   JWT_SECRET_KEY=your_secret_key
   ```

4. **Initialize the Database**
   ```bash
   python init_db.py
   ```

5. **Run the Server**
   ```bash
   python app.py
   ```
   Navigate to `http://localhost:5000` in your browser.
