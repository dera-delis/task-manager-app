# Task Manager App

A full-stack task management application built with FastAPI, React, and PostgreSQL.

## 🚀 Live Demo

**Frontend (React):** [Live App - Coming Soon](https://github.com/dera-delis/task-manager-app) *(Deploy to Vercel/Netlify)*
**Backend (FastAPI):** [Live API - Coming Soon](https://github.com/dera-delis/task-manager-app) *(Deploy to Render/Railway)*

*Note: Currently points to GitHub. Once deployed, these will link to live applications.*

## 🏆 Portfolio Project

This project demonstrates:
- **Full-Stack Development** - Backend API + Frontend UI
- **Modern Tech Stack** - FastAPI, React, PostgreSQL, Docker
- **Authentication System** - JWT-based user management
- **Database Design** - SQLAlchemy ORM with migrations
- **Containerization** - Production-ready Docker setup
- **Professional Development** - Clean commit history and testing

## 🚀 Features

## 📊 Project Status

![CI/CD](https://github.com/dera-delis/task-manager-app/actions/workflows/ci.yml/badge.svg)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

## 📸 Screenshots

### 🔐 Login Page
![Login Page](screenshots/login.png)

### 📝 Signup Page
![Signup Page](screenshots/signup.png)

### 📋 Dashboard with Tasks
![Dashboard](screenshots/dashboard.png)

### ➕ Task Creation
![Task Creation](screenshots/create-task.png)

### 📚 API Documentation (Swagger)
![Swagger Docs](screenshots/swagger-ui.png)

### 🐳 Docker Containers Running
![Docker Status](screenshots/docker.png)

### 🔧 API Testing
![API Testing](screenshots/api-testing.png)

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

## 🚀 Deployment

### Frontend Deployment (Vercel/Netlify)
```bash
# Build the frontend
cd frontend
npm run build

# Deploy to Vercel
vercel --prod

# Or deploy to Netlify
netlify deploy --prod
```

### Backend Deployment (Render/Railway)
```bash
# Set environment variables in your deployment platform
DATABASE_URL=your-production-postgres-url
SECRET_KEY=your-production-secret-key

# Deploy using Docker
docker build -t task-manager-backend ./backend
docker push your-registry/task-manager-backend
```

### Environment Variables for Production
```env
# Production Database
DATABASE_URL=postgresql://user:password@host:port/database

# Production JWT Secret
SECRET_KEY=your-super-secure-production-secret-key

# CORS Origins
ALLOWED_ORIGINS=https://your-frontend-domain.com
```

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

## 💼 Portfolio Project

This project is part of my **Full-Stack Portfolio** showcasing modern development skills.

**🔗 Connect with me:**
- [GitHub Profile](https://github.com/dera-delis)
- [LinkedIn](https://linkedin.com/in/dera-delis) *(Update with your actual LinkedIn)*

**🚀 Other Portfolio Projects:**
- [Blog API](https://github.com/dera-delis/blog-api) - Backend-focused FastAPI project
- [Task Manager App](https://github.com/dera-delis/task-manager-app) - Full-stack application *(This project)*

**💡 Why This Project?**
This full-stack application demonstrates:
- **End-to-end development** from database design to UI implementation
- **Modern architecture** with microservices and containerization
- **Production practices** including testing, CI/CD, and documentation
- **User experience** with responsive design and real-time updates

