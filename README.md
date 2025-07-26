# easy-tsd.ru

**easy-tsd.ru** is a free and open-source web-based data collection terminal for working with marked goods (DataMatrix codes).  
Built with **React + Django REST Framework**, it turns any smartphone into a simple yet powerful terminal for:

- ✅ Receiving goods with code verification  
- ✅ Shipping with reconciliation  
- ✅ Quick inventory tasks  

🧩 Works entirely in the browser – no apps, no hardware, no registration.

---

## 🖥 Tech Stack

| Component        | Technology                 |
|------------------|-----------------------------|
| Frontend         | React (Vite or CRA)         |
| Backend          | Django + Django REST        |
| State Persistence| Django session storage      |
| Auth / Identity  | Anonymous session + cookies |
| Data Store       | SQLite / PostgreSQL         |
| API Security     | CORS-enabled, CSRF-protected|

---

## 🌐 How It Works

1. Open [https://easy-tsd.ru](https://easy-tsd.ru) in Google Chrome on any device with a camera.
2. Upload a file with marked codes (`xml`, `xlsx`, `csv`, `txt`, or `pdf`)
3. Start scanning product codes with your smartphone camera.
4. View live progress and scan history tied to your session.
5. Download results in a compatible format: `xml`, `xlsx`, `csv`, `txt`, or `pdf`.

Your session data is preserved — even if the page is reloaded.

---

## 📦 Use Cases

- Small & Medium Business (SMB)
- Retail stores, warehouses, logistics hubs
- Fulfillment & drop-shipping operators
- Remote inventory checks & temporary setups
- Staff using personal devices (BYOD)

---

## 🛠 Project Structure

backend/ → Django project with API, session store and file parsers
frontend/ → React client using Fetch/Axios, Web API (camera, file, etc)

yaml
Копировать
Редактировать

Key modules include:
- `/api/session/` – Create & persist anonymous sessions
- `/api/scan/` – Append scanned codes to current session
- `/api/history/` – Retrieve and export scanning results

---

## 🔐 Sessions & Privacy

- Every user is tracked via a secure, anonymous cookie.
- All scanning activity is tied to their session (server-side).
- No user registration or external analytics.
- Data is stored temporarily and never shared.

---

## 🧪 Local Development

```bash
# Backend
cd backend
python manage.py runserver

# Frontend
cd frontend
npm install
npm run dev

---

## 🚀 Deployment
This project can be deployed using:

Docker (docker-compose)

Heroku / Render / Fly.io

Nginx + Gunicorn + Django + React (build artifacts)

---

## 📜 License
MIT License – free for commercial and personal use.

---

## 🤝 Contributing
Pull requests and ideas are welcome!
Feel free to file issues or submit improvements.

Made with ❤️ for developers, retailers, and warehouses that just want it to work.
