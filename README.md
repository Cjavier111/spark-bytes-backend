# SparkBytes - Backend

The backend for SparkBytes is a **Django + Django REST Framework (DRF)** API that manages user authentication, event listings, and available food tracking.

## 🚀 Live API
Deployed on Heroku: **[Insert Backend Heroku Link]**

## 🛠️ Tech Stack
- **Django** (Backend framework)
- **Django REST Framework** (API)
- **PostgreSQL** (Database)
- **Heroku** (Deployment)

## 📦 Installation & Setup
### 1️⃣ Create a Virtual Environment
```sh
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

2️⃣ Install Dependencies
sh
Copy
Edit
pip install -r requirements.txt
3️⃣ Set Up Environment Variables
Create a .env file in the root directory and configure the following:

ini
Copy
Edit
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=your-database-url
4️⃣ Apply Migrations & Start the Server
sh
Copy
Edit
python manage.py migrate
python manage.py runserver
The API should now be running at http://127.0.0.1:8000/.

