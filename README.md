# 📝 Task Manager API

A simple but scalable task management API built using Django REST Framework and PostgreSQL. This project is structured with reusable app modules inside an `apps/` directory and uses ViewSets for cleaner routing.

---

## 🚀 Features

- Task CRUD operations using Django REST Framework ViewSets  
- Modular app structure (`apps/tasks`)  
- PostgreSQL integration via Docker container  
- PyCharm support with CLI integration  
- Ready for Celery integration (for future background tasks)

---

## 📁 Project Structure

```
forkify/
├── apps/
│   └── tasks/
│       ├── admin.py
│       ├── apps.py
│       ├── models.py
│       ├── serializers.py
│       ├── urls.py
│       └── views.py
├── forkify/
│   └── settings.py
├── .gitignore
├── manage.py
├── README.md
└── requirements.txt
```

---

## 🐳 PostgreSQL via Docker

Run this to set up your DB container:

```bash
docker run --name task-postgres \
  -e POSTGRES_USER=admin \
  -e POSTGRES_PASSWORD=admin \
  -e POSTGRES_DB=taskdb \
  -p 5432:5432 \
  --restart=always \
  -d postgres
```

Update your Django `DATABASES` config accordingly in `settings.py`.

---

## ⚙️ How to Run the Project

1. Clone the repo:

   ```bash
   git clone https://github.com/thamjidthachu/Forkify-PixelForgeTech.git
   cd Forkify-PixelForgeTech
   ```

2. Create and activate virtualenv:

   ```bash
   python -m venv env
   .\env\Scripts\activate  # Windows
   source env/bin/activate  # Linux/macOS
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run migrations and start server:

   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

---

## 🔧 API Endpoints

| Method | Endpoint        | Description         |
|--------|------------------|---------------------|
| GET    | `/tasks/`        | List all tasks      |
| POST   | `/tasks/`        | Create a new task   |
| GET    | `/tasks/<id>/`   | Get a single task   |
| PUT    | `/tasks/<id>/`   | Update a task       |
| DELETE | `/tasks/<id>/`   | Delete a task       |

---

## 🧠 To Do (Optional Enhancements)

- Add Celery + Redis for background processing  
- Add authentication & permissions  
- Add filtering, pagination, and search  
- Write unit tests  

---

## 🧑‍💻 Author

Built with ❤️ by Thachu (a.k.a. @Thamjid M)

---
