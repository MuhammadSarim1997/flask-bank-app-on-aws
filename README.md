# 💸 flask-bank-app-on-aws

A simple **banking web app** built with **Flask**, showcasing full-stack development and **AWS cloud deployment** using **EC2** (and optionally RDS). This project demonstrates backend logic, database integration, and secure cloud hosting using Nginx, DuckDNS, and HTTPS.

---

## 🚀 Features

- 🔐 User login and account management
- 💰 Deposit, withdraw, and view balances
- 📄 Transaction history
- 🖥️ Frontend rendered using Jinja2 and HTML
- ☁️ Hosted on **AWS EC2**
- 🗄️ Uses **PostgreSQL** (local or AWS RDS)

---

## 🧱 Tech Stack

| Layer       | Technology             |
|-------------|-------------------------|
| Backend     | Python (Flask)          |
| Frontend    | HTML + Jinja2 Templates |
| Database    | PostgreSQL              |
| Hosting     | AWS EC2 (Ubuntu)        |
| Optional    | AWS RDS for PostgreSQL  |
| DevOps      | Git + GitHub + Nginx    |

---

## 📁 Folder Structure

<pre>
flask-bank-app-on-aws/
│
├── app.py                       # Flask app entrypoint
├── bank_app_frontend_flask.html # Main HTML frontend
├── bank_class.py               # Banking logic (OOP)
├── Database_cred_and_func.py   # DB connection & credentials
├── requirements.txt            # Python dependencies
└── .gitpod.yml                 # (Optional) Gitpod config
</pre>

---

## 🔧 Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/MuhammadSarim1997/flask-bank-app-on-aws.git
cd flask-bank-app-on-aws
```

### 2. Create a virtual environment (optional but recommended)

```bash
python -m venv venv
source venv/bin/activate    # Mac/Linux
venv\Scripts\activate       # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set up PostgreSQL (locally or on AWS RDS)

Update your DB credentials in `Database_cred_and_func.py`:

```python
conn = psycopg2.connect(
    host="your-db-host",
    database="your-db-name",
    user="your-db-username",
    password="your-db-password"
)
```

### 5. Run the Flask app

```bash
python app.py
```

Then visit [http://localhost:5000](http://localhost:5000)

---

## 🌐 Live Demo

The app is deployed and publicly accessible at:

🔗 https://rcbbanking.duckdns.org

> Hosted on an AWS EC2 instance with a custom domain via DuckDNS and HTTPS enabled using Let's Encrypt SSL certificates.

---

## ☁️ Hosting Details

| Feature            | Description                                     |
|--------------------|-------------------------------------------------|
| **Domain**         | rcbbanking.duckdns.org via DuckDNS             |
| **Server**         | AWS EC2 (Ubuntu)                                |
| **Web Framework**  | Flask (Python)                                  |
| **Database**       | PostgreSQL (local or AWS RDS optional)          |
| **HTTPS**          | Enabled using Certbot + Nginx + DuckDNS cert    |
| **Port**           | Served on https:// via Nginx reverse proxy      |

---

## 🔌 Manual Deployment on AWS EC2

1. Launch an EC2 instance (Ubuntu recommended)
2. SSH into the instance:

```bash
ssh -i your-key.pem ubuntu@<your-ec2-ip>
```

3. Install required packages:

```bash
sudo apt update && sudo apt install python3-pip git
```

4. Clone this repo and follow the setup instructions above
5. Configure `nginx` for reverse proxy (recommended) and enable port `443` (HTTPS)

---

## 🧠 Author

**Muhammad Sarim**  
GitHub: https://github.com/MuhammadSarim1997  
LinkedIn: https://linkedin.com/in/msarim

---

## 📄 License

This project is licensed under the MIT License. See `LICENSE` for details.
