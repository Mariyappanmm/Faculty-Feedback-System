# Faculty Feedback System 🎓

A **Flask-based web application** for collecting, storing, and analyzing faculty feedback from students.  
The system integrates **Google Sheets** for centralized data storage, while also maintaining a **local SQLite database** for authentication and session management.  

---

## 🚀 Features
- 🔐 **User Authentication** (Login, Logout) with Flask-Login & Bcrypt  
- 📝 **Dynamic Feedback Form** (20+ questions with faculty-specific IDs)  
- 💾 **Google Sheets Integration** for storing responses in real-time  
- 📊 **Session-based Data Handling** before submission  
- 🖥 **Role-based Dashboard** (student batches & courses mapped dynamically)  
- ✅ **Secure Password Storage** (hashed using Bcrypt)  
- 🗄 **SQLite Database Support** for storing user credentials  

---

## 🛠 Tech Stack
- **Backend**: Flask (Python)  
- **Database**: SQLite + Google Sheets  
- **Authentication**: Flask-Login, Flask-Bcrypt  
- **Frontend**: HTML, CSS (Jinja2 templates)  
- **API**: Google Sheets API via `gspread` and `oauth2client`  

---

## 📂 Project Structure
Faculty-Feedback-System/
│── app.py # Main Flask app
│── users.db # SQLite Database (auto-created)
│── templates/ # HTML Templates (login, dashboard, forms, etc.)
│── static/ # CSS/JS/Assets
│── metal-imprint-453415-q9-b5494fb00c71.json # Google API Credentials
│── README.md # Documentation

yaml
Copy
Edit

---

## ⚙️ Installation & Setup
1. **Clone the repository**
   ```bash
   git clone https://github.com/Mariyappanmm/Faculty-Feedback-System.git
   cd Faculty-Feedback-System
Create a virtual environment (recommended)

bash
Copy
Edit
python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows
Install dependencies

bash
Copy
Edit
pip install flask flask_sqlalchemy flask_bcrypt flask_login gspread oauth2client
Set up Google Sheets API

Create a Service Account in Google Cloud Console

Enable Google Sheets API & Google Drive API

Download the JSON key file & rename it as:
metal-imprint-453415-q9-b5494fb00c71.json

Share your Google Sheet with the client_email inside the JSON

Run the application

bash
Copy
Edit
python app.py
App runs at: http://127.0.0.1:5000/

🔑 Default Routes
/ → Login Page

/dashboard → Student Dashboard (dynamic based on batch & course)

/form1.html → Feedback Form (faculty-specific)

/submit → Submit feedback to Google Sheet

/logout → Logout

📊 Future Enhancements
Admin Panel for managing faculty & students

Analytics dashboard with charts (feedback trends)

Multi-course & multi-faculty support

Export feedback as Excel/PDF

🤝 Contribution
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## Screenshots

### Login Page
![Login Page](screenshots/login.png)

### Dashboard
![Dashboard](screenshots/dashboard.png)

### Feedback Form
![Feedback Form](screenshots/form.png)



