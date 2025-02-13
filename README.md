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
To run the backend locally:

1. **Clone the repository**  
   ```sh
   git clone https://github.com/yourusername/sparkbytes-backend.git
   cd sparkbytes-backend
Create a virtual environment

sh
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
Install dependencies

sh
Copy
Edit
pip install -r requirements.txt
Set up environment variables
Create a .env file in the root directory and configure the following:

sh
Copy
Edit
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=your-database-url
Apply migrations & start the server

sh
Copy
Edit
python manage.py migrate
python manage.py runserver
The API should now be running at http://127.0.0.1:8000/.

🚀 Deployment on Heroku
Login to Heroku

sh
Copy
Edit
heroku login
Create a Heroku app

sh
Copy
Edit
heroku create sparkbytes-backend
Add Heroku Postgres (if needed)

sh
Copy
Edit
heroku addons:create heroku-postgresql:hobby-dev
Set environment variables

sh
Copy
Edit
heroku config:set SECRET_KEY=your-secret-key
heroku config:set DEBUG=False
heroku config:set ALLOWED_HOSTS=sparkbytes-backend.herokuapp.com
heroku config:set DATABASE_URL=your-database-url
Deploy to Heroku

sh
Copy
Edit
git add .
git commit -m "Deploy backend"
git push heroku main
Run database migrations

sh
Copy
Edit
heroku run python manage.py migrate
Open the deployed API

sh
Copy
Edit
heroku open
📊 API Endpoints
Method	Endpoint	Description
GET	/api/events/	List all events
POST	/api/events/	Create a new event
GET	/api/events/{id}/	Retrieve event details
POST	/api/auth/login/	User login
POST	/api/auth/signup/	User registration
📜 License
This project is licensed under the MIT License.
