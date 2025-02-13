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
```
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```
### 2️⃣ Install Dependencies
```
pip install -r requirements.txt
```
### 3️⃣ Set Up Environment Variables
Create a .env file in the root directory and configure the following:
```
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=your-database-url
```
### 4️⃣ Apply Migrations & Start the Server
```
python manage.py migrate
python manage.py runserver
```
The API should now be running at http://127.0.0.1:8000/

## 🚀 Deployment on Heroku

### 1️⃣ Login to Heroku
```
heroku login
```
### 2️⃣ Create a Heroku App
```
heroku create sparkbytes-backend
```
### 3️⃣ Add Heroku Postgres (if needed)
```
heroku addons:create heroku-postgresql:hobby-dev
```
### 4️⃣ Set Environment Variables
```
heroku config:set SECRET_KEY=your-secret-key
heroku config:set DEBUG=False
heroku config:set ALLOWED_HOSTS=sparkbytes-backend.herokuapp.com
heroku config:set DATABASE_URL=your-database-url
```

### 5️⃣ Deploy to Heroku
```
git add .
git commit -m "Deploy backend"
git push heroku main
```
### 6️⃣ Run Database Migrations
```
heroku run python manage.py migrate
```
### 7️⃣ Open the Deployed API
```
heroku open

```
## 📊 API Endpoints

| **Method** | **Endpoint**            | **Description**          |
|-----------|-------------------------|--------------------------|
| GET       | `/api/events/`          | List all events         |
| POST      | `/api/events/`          | Create a new event      |
| GET       | `/api/events/{id}/`     | Retrieve event details  |
| POST      | `/api/auth/login/`      | User login             |
| POST      | `/api/auth/signup/`     | User registration      |


## 📜 License
This project is licensed under the MIT License.



