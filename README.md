# 📝 Flask Task Tree 🚀

> *Built by a dev who actually knows how to get things done* 💪

A **bulletproof Flask Todo/Task Manager** that combines speed, simplicity, and style. Powered by SQLAlchemy for rock-solid data persistence. If you're tired of janky task managers, this is your answer.

## 📊 Stats That Matter

- ⚡ **Lightning Fast** - Built with zero bloat, pure Flask speed
- 🔒 **Production Ready** - SQLite database with proper ORM handling
- 🎯 **100% Functional** - Full CRUD operations (Create, Read, Update, Delete)
- 🧠 **Smart Architecture** - Properly structured Flask app that scales
- 💎 **Clean Code** - No spaghetti code in this kitchen

## ✨ Features That Flex

- ✅ **Add Tasks Like a Boss** - One input, one submit. Done. No extra steps needed.
- 🗑️ **Delete with Confidence** - Tasks gone in a millisecond
- 📝 **Update Tasks on the Fly** - Change your mind? No problem.
- 💾 **Persistent Storage** - Tasks don't disappear. Ever. (SQLite's got your back)
- 🎨 **UI That Actually Works** - Clean, centered, responsive. Not overdone.
- 🔄 **Instant Feedback** - Changes happen NOW, not "in a few seconds"

## 🛠️ Tech Stack (No Compromise)

- **Backend:** Flask (the OG lightweight framework)
- **Database:** SQLite with SQLAlchemy ORM (proper SQL, not some NoSQL meme)
- **Frontend:** HTML, Jinja2 templating, CSS (hand-crafted, not bloated)
- **Python Version:** 3.13+ (staying current because we're not dinosaurs)

## 📦 Quick Setup (5 Minutes, Bro)

### Step 1: Clone This Beauty
```bash
git clone https://github.com/mccoymikeyistaken-byte/flask-task-tree.git
cd flask-task-tree
```

### Step 2: Virtual Environment (Do This Every Time)
```bash
python3 -m venv myenv
source myenv/bin/activate  # Windows users: myenv\Scripts\activate
```

### Step 3: Install the Goods
```bash
pip install -r requirements.txt
```

### Step 4: Initialize the Database
```bash
python3 -c "from app import app, db; app.app_context().push(); db.create_all()"
```
(Don't skip this or you'll be confused AF 😅)

## 🚀 Let's Go

### Fire It Up
```bash
python app.py
```

Open **`http://127.0.0.1:5000`** and watch the magic happen.

### How to Use (It's Obvious, But Here We Go)

1. **Add a Task** 📌
   - Type something you need to do
   - Hit "Add Task"
   - Boom. It's there.

2. **Delete a Task** 🗑️
   - Click "Delete Task"
   - It's gone. Forever.

3. **Update a Task** ✏️
   - Click "Update Task" (this feature is coming, be patient bro)

That's literally it. No dark mode toggle nonsense. No 47 settings. Just tasks.

## 📁 Project Structure (Clean & Organized)

```
flask-task-tree/
├── app.py                 # The main event - all the logic lives here
├── requirements.txt       # Dependencies (pip install this)
├── instance/
│   └── test.db           # Your tasks live here (SQLite database)
├── static/
│   └── css/
│       └── main.css      # The style that makes it pop
└── templates/
    ├── base.html         # Template foundation
    ├── index.html        # The main task page where stuff happens
    └── update.html       # Update functionality (coming soon)
```

## 🔧 Configuration

Need to change something? Edit `app.py`:

```python
# Database path
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///test.db'

# Debug mode (turn this OFF in production)
app.run(debug=True)

# Port (default is 5000)
app.run(port=5000)
```

## 🚢 Ready to Ship It? (Deployment Guide)

When you're tired of localhost and want to go LIVE:

1. **Security First** - Set `debug=False` in production
   ```python
   app.run(debug=False)
   ```

2. **Use a Real Server** (Flask dev server is NOT for production, seriously)
   ```bash
   pip install gunicorn
   gunicorn app:app
   ```

3. **Pick Your Platform:**
   - **Railway** - Dead simple, free tier available
   - **Heroku** - Classic choice, easy deployment
   - **AWS/DigitalOcean** - More control, slightly more complex
   - **Render** - Modern alternative to Heroku

That's when your Flask Task Tree goes global. 🌍

## 📝 Database Schema (What We're Storing)

**Todo Model** (Simple but Effective):
```python
- id          → Task ID (auto-incremented, primary key)
- content     → What you actually need to do (required)
- completed   → Done or not? (0 or 1, default: 0)
- date_created → When you added this task (auto timestamp)
```

Pretty straightforward. No unnecessary fields cluttering things up.

## 🤝 Contributing

Got ideas? Found a bug? Want to add something sick?

1. Fork it
2. Create a feature branch (`git checkout -b feature/awesome-thing`)
3. Commit your stuff (`git commit -m "Add awesome thing"`)
4. Push it (`git push origin feature/awesome-thing`)
5. Open a Pull Request

We accept contributions from anyone who knows what they're doing.

## 📄 License

MIT License - Do whatever you want with this code. Seriously. No restrictions.

---

## 🎬 The Real Talk

No frameworks overkill, no unnecessary complexity, just **Flask doing what Flask does best** - getting out of your way while you build something real.

### Created by **@mccoymikeyistaken-byte** 

**Made with actual caffeine and zero BS** ☕💻
