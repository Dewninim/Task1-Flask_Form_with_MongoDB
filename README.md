# Ai-Developer.Task-4
# 📝 Task 1 - Flask Form with MongoDB

This project is a simple task submission web application built using **Flask (Python)** as the backend, **HTML + JavaScript** for the frontend, and **MongoDB** for data storage.

---

## 📌 Features

- 🧾 5-field task submission form
- ⚙️ Flask backend with API endpoint
- 📦 MongoDB integration (local or Atlas cloud)
- 🖥️ Simple HTML/JavaScript frontend
- 📡 AJAX-based form submission (no page reload)

---

## 🛠️ Tech Stack

- **Frontend**: HTML, JavaScript (Fetch API)
- **Backend**: Python, Flask
- **Database**: MongoDB (Local or Cloud)
- **Others**: dotenv for managing environment variables

---

## 📁 Project Structure

task1_form/
│
├── app.py # Main Flask app
├── db.py # MongoDB connection
├── requirements.txt # Python dependencies
├── .env # (Optional) MongoDB URI
│
├── templates/
│ └── index.html # HTML form
│
├── static/
│ └── script.js # JavaScript (form submission)



---

## 🚀 Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/Dewninim/Ai-Developer.Task-4.git
cd Ai-Developer.Task-4/task1_form
----
```
# 2. Create and Activate Python Virtual Environment

python -m venv venv
venv\Scripts\activate


# 3. Install Python Dependencies

pip install -r requirements.txt

# 4. (Optional) Configure .env File
Create a .env file in the project root:
MONGO_URI=mongodb://localhost:27017

If using MongoDB Atlas:

MONGO_URI=mongodb+srv://<user>:<password>@cluster.mongodb.net/task_manager

# 5. Start MongoDB
Local MongoDB: run mongod in your terminal

Atlas: ensure cluster is accessible and your IP is whitelisted

# 6. Run Flask Application
python app.py

Navigate to:
➡️ http://localhost:5000

7. Submit a Task and View Database
Fill out the form fields

Submit; see success or error message

Check task_manager.submitted_tasks collection in MongoDB

🔍 How it Works
app.py: Defines Flask routes / (renders form) and /submit (handles JSON POST, validation, DB insertion, and JSON response)

db.py: Loads MongoDB URI (from .env or default), connects with pymongo, defines collection

index.html: Basic form with five inputs and a submit button

script.js: Captures form submission, sends JSON to Flask backend, handles response




