# 💸 flask-bank-app-on-aws

A simple **banking web app** built with **Flask**, showcasing full-stack development and **AWS cloud deployment** using **EC2** (and optionally RDS). This project demonstrates backend logic, database integration, and secure cloud hosting.

---

## 🚀 Features

- 🔐 User login and account management
- 💰 Deposit, withdraw, and view balances
- 📄 Transaction history
- 🖥️ Frontend rendered using Jinja2 and HTML
- ☁️ Hosted on **AWS EC2**
- 🗄️ Uses **PostgreSQL** (AWS RDS)

---

## 🧱 Tech Stack

| Layer       | Technology            |
|-------------|------------------------|
| Backend     | Python (Flask)         |
| Frontend    | HTML + Jinja2 Templates|
| Database    | PostgreSQL             |
| Hosting     | AWS EC2 (Ubuntu)       |
| Optional    | AWS RDS for PostgreSQL |
| DevOps      | Git + GitHub           |

---

## 📁 Folder Structure

<pre>
flask-bank-app-on-aws/
│
├── app.py # Flask app entrypoint
├── bank_app_frontend_flask.html # Main HTML frontend
├── bank_class.py # Banking logic (OOP)
├── Database_cred_and_func.py # DB connection & credentials
├── requirements.txt # Python dependencies
└── .gitpod.yml # (Optional) Gitpod config
</pre>
---

## 🔧 Setup Instructions

### 1. Clone the repo

<pre>
git clone https://github.com/MuhammadSarim1997/flask-bank-app-on-aws.git
cd flask-bank-app-on-aws
</pre>

### 2. Create a virtual environment (optional but recommended)

<pre>
python -m venv venv
source venv/bin/activate    # Mac/Linux
venv\Scripts\activate       # Windows
</pre>
### 3. Install dependencies

'''
pip install -r requirements.txt
'''

### 4. Set up PostgreSQL (locally or use AWS RDS)
Update your DB credentials in Database_cred_and_func.py:

<pre>
conn = psycopg2.connect(
    host="your-db-host",
    database="your-db-name",
    user="your-db-username",
    password="your-db-password"
)
</pre>
  
### 5. Run the Flask app
'python app.py'
Then visit:
'''
http://localhost:5000
'''
☁️ Hosting on AWS EC2
Launch an EC2 instance (Ubuntu recommended)

SSH into it:
'''
ssh -i your-key.pem ubuntu@<your-ec2-ip>
'''
Install dependencies:
<pre>
sudo apt update && sudo apt install python3-pip git
</pre>
Clone this repo and set up the app as above

Allow port 5000 or use nginx for production


## 🧠 Author
Muhammad Sarim
GitHub • LinkedIn

## 📄 License
This project is licensed under the MIT License. See LICENSE for details.

---
