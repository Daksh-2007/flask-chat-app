# 💬 Real-Time Chat Rooms Application

A lightweight, high-performance real-time chat web application built with **Flask**, **Flask-SocketIO**, and **WebSockets**. Users can instantly create or join private chat rooms using auto-generated 4-letter room codes, with no user registration required.

---

## 🚀 Live Demo

[[Live Demo](https://flask-chat-app-u4hq.onrender.com)  


---

## ✨ Features

* **⚡ Real-Time Bi-directional Messaging:** Instant message broadcasting powered by WebSockets via `Flask-SocketIO`.
* **🔑 Dynamic Room Management:** Users can generate unique 4-character room codes or join existing ones.
* **🧹 Automatic Cleanup & State Management:** In-memory tracking of members and active message history; automatically cleans up empty rooms when all users disconnect.
* **⌨️ Intuitive UX Keyboard Shortcuts:**
  * `Enter`: Send message instantly.
  * `Shift + Enter`: Insert a newline character without sending.
* **📱 Responsive Fixed Layout:** Chat message box remains auto-scrolling with a fixed bottom input control area across various screen resolutions.

---

## 🛠️ Tech Stack & Dependencies

* **Backend:** Python, Flask, Flask-SocketIO
* **WSGI / ASGI Server:** Gunicorn with Gevent (`gevent`, `gevent-websocket`)
* **Frontend:** HTML5, CSS3, JavaScript (Vanilla JS), Socket.IO Client Library
* **Deployment:** Render PaaS

---

## 📁 Project Structure

```text
flask-chat-app/
├── static/
│   └── css/
│       └── style.css       # Layout positioning and responsive chat UI styling
├── templates/
│   ├── base.html          # Base Jinja2 layout template with Socket.IO dependencies
│   ├── home.html          # Landing page for creating or joining rooms
│   └── room.html          # Dynamic room view and WebSocket event handlers
├── .gitignore             # Git exclusion rules
├── .python-version        # Version pinning for production environment (Python 3.12)
├── main.py                # Flask server, routing logic, and SocketIO event handling
├── Procfile               # Production WSGI startup configuration
└── requirements.txt       # Python package requirements
