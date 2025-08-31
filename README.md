# Task Manager App

A full-stack task management application built with modern technologies. Users can register, login, and manage their tasks with a clean, intuitive interface.

## 🚀 Live Demo

- **Frontend**: [https://task-manager-app-iota-teal.vercel.app](https://task-manager-app-iota-teal.vercel.app)
- **Backend API**: [https://p01--task-manager-backend--6s6kwy85s9yl.code.run](https://p01--task-manager-backend--6s6kwy85s9yl.code.run)
- **API Documentation**: [https://p01--task-manager-backend--6s6kwy85s9yl.code.run/docs](https://p01--task-manager-backend--6s6kwy85s9yl.code.run/docs)

## 🏆 Badges

![CI/CD](https://github.com/dera-delis/task-manager-app/actions/workflows/ci.yml/badge.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

## 📸 Screenshots

### 🔐 Login Page
![Login](screenshots/login.png)

### 📝 Signup Page
![Signup](screenshots/signup.png)

### 📋 Dashboard with Tasks
![Dashboard](screenshots/dashboard.png)

### 📚 API Documentation (Swagger)
![Swagger](screenshots/swagger-ui.png)

### 🐳 Docker Running
![Docker](screenshots/docker.png)

### ➕ Task Creation
![Task Creation](screenshots/create-task.png)

### 🔧 API Testing
![API Testing](screenshots/api-testing.png)

## Features

- **User Authentication**: Secure signup and login with JWT tokens
- **Task Management**: Create, read, update, and delete tasks
- **Task Status**: Mark tasks as complete or incomplete
- **User Dashboard**: Personalized task view for each user
- **Responsive Design**: Works on desktop and mobile devices

## Tech Stack

### Backend
- **FastAPI**: Modern Python web framework
- **PostgreSQL**: Reliable relational database
- **SQLAlchemy**: Python ORM for database operations
- **JWT**: Secure authentication system
- **Alembic**: Database migrations

### Frontend
- **React**: Modern JavaScript framework
- **Tailwind CSS**: Utility-first CSS framework
- **Axios**: HTTP client for API calls
- **React Router**: Client-side routing

### Deployment
- **Vercel**: Frontend hosting
- **Northflank**: Backend and database hosting
- **Docker**: Containerization
- **GitHub Actions**: CI/CD pipeline

## Project Structure

```
task-manager-app/
├── backend/                 # FastAPI backend
│   ├── app/
│   │   ├── models.py       # Database models
│   │   ├── schemas.py      # Pydantic schemas
│   │   ├── crud.py         # Database operations
│   │   ├── routers/        # API endpoints
│   │   └── main.py         # FastAPI application
│   ├── tests/              # Backend tests
│   ├── requirements.txt    # Python dependencies
│   └── Dockerfile         # Backend container
├── frontend/               # React frontend
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/          # Page components
│   │   ├── context/        # React context
│   │   └── App.js          # Main app component
│   ├── package.json        # Node.js dependencies
│   └── Dockerfile          # Frontend container
├── docker-compose.yml      # Local development
└── README.md               # This file
```

## Getting Started

### Prerequisites
- Python 3.11+
- Node.js 18+
- Docker and Docker Compose
- PostgreSQL

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/dera-delis/task-manager-app.git
   cd task-manager-app
   ```

2. **Start the services**
   ```bash
   docker-compose up -d
   ```

3. **Access the application**
   - Frontend: http://localhost:3000
   - Backend: http://localhost:8000
   - API Docs: http://localhost:8000/docs

### Environment Variables

Create a `.env` file in the root directory:

```bash
# Backend
DATABASE_URL=postgresql://postgres:password@localhost:5433/taskmanager
SECRET_KEY=your-secret-key-here

# Frontend
REACT_APP_API_URL=http://localhost:8000
```

## API Endpoints

### Authentication
- `POST /auth/signup` - User registration
- `POST /auth/login` - User login
- `GET /auth/me` - Get current user

### Tasks
- `GET /tasks/` - Get user's tasks
- `POST /tasks/` - Create new task
- `PUT /tasks/{task_id}` - Update task
- `DELETE /tasks/{task_id}` - Delete task
- `PUT /tasks/{task_id}/toggle` - Toggle task completion

## Development

### Backend Development
```bash
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### Frontend Development
```bash
cd frontend
npm install
npm start
```

### Running Tests
```bash
# Backend tests
cd backend
python -m pytest tests/ -v

# Frontend tests
cd frontend
npm test
```

## Deployment

The application is deployed using:
- **Frontend**: Vercel for static hosting
- **Backend**: Northflank for container hosting
- **Database**: Northflank PostgreSQL addon

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 🎯 Future Enhancements

- [ ] Task categories and tags
- [ ] Due dates and reminders
- [ ] Dark mode theme
- [ ] Task collaboration (shared tasks)
- [ ] Email notifications
- [ ] Task analytics and reports
- [ ] Mobile app
- [ ] Task templates
- [ ] Bulk operations
- [ ] Export/import functionality

## 💼 Portfolio Projects

This project is part of my **Full-Stack Portfolio** showcasing modern development skills.

**🔗 Connect with me:**
- [GitHub Profile](https://github.com/dera-delis)
- [LinkedIn](https://linkedin.com/in/dera-delis) *(Update with your actual LinkedIn)*

**🚀 Other Portfolio Projects:**
- [Blog API](https://github.com/dera-delis/blog-api) – Backend-focused FastAPI project
- [Task Manager App](https://github.com/dera-delis/task-manager-app) – Full-stack application *(This project)*

**💡 Why This Project?**
This full-stack application demonstrates:
- **End-to-end development** from database design to UI implementation
- **Modern architecture** with microservices and containerization
- **Production practices** including testing, CI/CD, and documentation
- **User experience** with responsive design and real-time updates

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

- **GitHub**: [@dera-delis](https://github.com/dera-delis)
- **Project**: [Task Manager App](https://github.com/dera-delis/task-manager-app)

