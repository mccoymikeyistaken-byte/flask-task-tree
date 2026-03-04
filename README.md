# 📝 Flask Task Tree

A simple yet powerful **Flask Todo/Task Manager** application built with SQLAlchemy for persistent storage. Add, update, and delete your tasks with a beautiful, responsive UI.

## ✨ Features

- ✅ **Add Tasks** - Quickly add new tasks to your to-do list
- 🗑️ **Delete Tasks** - Remove completed or unwanted tasks
- 📝 **Update Tasks** - Edit existing tasks
- 💾 **Persistent Storage** - Tasks saved to SQLite database
- 🎨 **Clean UI** - Simple, centered, and easy-to-use interface
- 🔄 **Real-time Updates** - No page refresh needed for task management

## 🛠️ Tech Stack

- **Backend:** Flask
- **Database:** SQLite with SQLAlchemy ORM
- **Frontend:** HTML, Jinja2 templating, CSS
- **Python Version:** 3.13+

## 📦 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/mccoymikeyistaken-byte/flask-task-tree.git
cd flask-task-tree
```

### 2. Create Virtual Environment
```bash
python3 -m venv myenv
source myenv/bin/activate  # On Windows: myenv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Create Database
```bash
python3 -c "from app import app, db; app.app_context().push(); db.create_all()"
```

## 🚀 Usage

### Start the Application
```bash
python app.py
```

Visit **`http://127.0.0.1:5000`** in your browser.

### Add a Task
1. Type your task in the input field
2. Click **"Add Task"**

### Delete a Task
- Click the **"Delete Task"** link next to any task

### Update a Task
- Click the **"Update Task"** link (feature coming soon)

## 📁 Project Structure

```
flask-task-tree/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── instance/
│   └── test.db           # SQLite Database
├── static/
│   └── css/
│       └── main.css      # Styling
└── templates/
    ├── base.html         # Base template
    ├── index.html        # Main task page
    └── update.html       # Task update page
```

## 🔧 Configuration

Edit `app.py` to customize:
- Database URI: `app.config['SQLALCHEMY_DATABASE_URI']`
- Debug mode: `app.run(debug=True)`
- Port: `app.run(port=5000)`

## 🚢 Deployment

For production deployment:

1. Set `debug=False` in app.py
2. Use a production WSGI server:
   ```bash
   pip install gunicorn
   gunicorn app:app
   ```
3. Deploy to: Heroku, AWS, DigitalOcean, Railway, etc.

## 📝 Database Schema

**Todo Model:**
```python
- id (Integer, Primary Key)
- content (String, Required)
- completed (Integer, Default: 0)
- date_created (DateTime, Default: Current Time)
```

## 🤝 Contributing

Feel free to fork, submit issues, and create pull requests!

## 📄 License

MIT License - Feel free to use this project however you want.

## 👨‍💻 Author

**@mccoymikeyistaken-byte**

---

**Made with ❤️ using Flask**
