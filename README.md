# Task Manager App

A full-stack task management application built with FastAPI, React, and PostgreSQL. Features user authentication, task CRUD operations, and a modern responsive UI.

## 🚀 Features

- **User Authentication**: JWT-based signup/login system
- **Task Management**: Create, read, update, delete tasks
- **Task Completion**: Mark tasks as complete/incomplete
- **Responsive Design**: Modern UI built with Tailwind CSS
- **Real-time Updates**: Live task updates without page refresh
- **Docker Ready**: Complete containerization setup

## 🛠 Tech Stack

### Backend
- **FastAPI**: Modern Python web framework
- **PostgreSQL**: Reliable relational database
- **SQLAlchemy**: Python ORM for database operations
- **Alembic**: Database migration tool
- **JWT**: JSON Web Tokens for authentication
- **Pydantic**: Data validation and serialization

### Frontend
- **React**: Modern JavaScript library for UI
- **Tailwind CSS**: Utility-first CSS framework
- **Axios**: HTTP client for API calls
- **React Router**: Client-side routing

## 📁 Project Structure

```
task-manager-app/
├── backend/                # FastAPI backend
│   ├── app/
│   │   ├── main.py         # Entry point
│   │   ├── models.py       # SQLAlchemy models
│   │   ├── schemas.py      # Pydantic schemas
│   │   ├── database.py     # DB connection
│   │   ├── crud.py         # CRUD logic
│   │   └── routers/
│   │       ├── auth.py     # Signup/Login
│   │       └── tasks.py    # CRUD for tasks
│   ├── tests/              # Pytest unit tests
│   ├── requirements.txt    # Python dependencies
│   ├── alembic/            # DB migrations
│   └── Dockerfile
│
├── frontend/               # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/     # Task UI components
│   │   ├── pages/          # Pages (Login, Signup, Dashboard)
│   │   ├── context/        # React context for auth
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json        # JS dependencies
│   └── Dockerfile
│
├── docker-compose.yml      # Orchestration for all services
├── README.md               # Documentation
└── .env.example            # Example environment variables
```

## 🚀 Quick Start

### Prerequisites
- Docker and Docker Compose installed
- Git

### 1. Clone the Repository
```bash
git clone <repository-url>
cd task-manager-app
```

### 2. Start the Application
```bash
docker-compose up --build
```

This will start:
- PostgreSQL database on port 5433
- FastAPI backend on port 8000
- React frontend on port 3000

### 3. Access the Application
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs

## 🔧 Development Setup

### Backend Development

1. **Install Python dependencies**:
```bash
cd backend
pip install -r requirements.txt
```

2. **Set up environment variables**:
```bash
cp .env.example .env
# Edit .env with your database credentials
```

3. **Run database migrations**:
```bash
alembic upgrade head
```

4. **Start the development server**:
```bash
uvicorn app.main:app --reload
```

### Frontend Development

1. **Install Node.js dependencies**:
```bash
cd frontend
npm install
```

2. **Start the development server**:
```bash
npm start
```

## 📚 API Endpoints

### Authentication
- `POST /auth/signup` - Create a new user account
- `POST /auth/login` - Login with email and password
- `GET /auth/me` - Get current user information

### Tasks
- `GET /tasks/` - Get all tasks for the current user
- `POST /tasks/` - Create a new task
- `GET /tasks/{task_id}` - Get a specific task
- `PUT /tasks/{task_id}` - Update a task
- `DELETE /tasks/{task_id}` - Delete a task
- `PATCH /tasks/{task_id}/toggle` - Toggle task completion

## 🐳 Docker Commands

### Start all services
```bash
docker-compose up --build
```

### Start in background
```bash
docker-compose up -d --build
```

### View logs
```bash
docker-compose logs -f
```

### Stop all services
```bash
docker-compose down
```

### Remove volumes (database data)
```bash
docker-compose down -v
```

## 🧪 Testing

### Backend Tests
```bash
cd backend
pytest
```

### Frontend Tests
```bash
cd frontend
npm test
```

## 🔒 Environment Variables

Create a `.env` file in the root directory:

```env
# Database
DATABASE_URL=postgresql://postgres:password@localhost:5433/taskmanager

# JWT
SECRET_KEY=your-super-secret-key-change-in-production

# Frontend
REACT_APP_API_URL=http://localhost:8000
```

## 📝 Usage

1. **Sign Up**: Create a new account with email, username, and password
2. **Login**: Sign in with your credentials
3. **Create Tasks**: Add new tasks with title and optional description
4. **Manage Tasks**: Edit, delete, or mark tasks as complete
5. **View Progress**: See your task completion statistics

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. Check the [API documentation](http://localhost:8000/docs) when running locally
2. Review the logs: `docker-compose logs`
3. Open an issue on GitHub

## 🎯 Future Enhancements

- [ ] Task categories and tags
- [ ] Due dates and reminders
- [ ] Task sharing and collaboration
- [ ] Dark mode theme
- [ ] Mobile app
- [ ] Email notifications
- [ ] Task analytics and reports

