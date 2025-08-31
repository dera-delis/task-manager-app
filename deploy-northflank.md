# 🚀 Deploy to Northflank - Full Stack Guide

## 📋 Prerequisites
- Northflank account (free tier)
- Docker images ready
- Environment variables configured

## 🎯 Northflank Advantages
- **Full-stack support** (FastAPI + React + PostgreSQL)
- **Container-native** (perfect for your Docker setup)
- **Free tier available**
- **Easy scaling**

## 🚀 Step-by-Step Deployment

### 1. **Create Northflank Account**
- Go to [northflank.com](https://northflank.com)
- Sign up for free tier
- Verify email if required

### 2. **Create New Project**
- Click "New Project"
- Name: `task-manager-app`
- Description: `Full-stack task manager with FastAPI, React, and PostgreSQL`

### 3. **Deploy PostgreSQL Database**
- Click "New Service" → "Database"
- Choose **PostgreSQL**
- Service name: `taskmanager-db`
- Version: `15`
- Environment variables:
  ```
  POSTGRES_DB=taskmanager
  POSTGRES_USER=postgres
  POSTGRES_PASSWORD=your-secure-password
  ```
- Click "Deploy"

### 4. **Deploy FastAPI Backend**
- Click "New Service" → "Container"
- Service name: `taskmanager-backend`
- **Source**: Connect to your GitHub repository (`dera-delis/task-manager-app`)
- **Build context**: `backend/` (relative to repo root)
- **Dockerfile location**: `backend/Dockerfile`
- Run command: `uvicorn app.main:app --host 0.0.0.0 --port 8000`
- Port: `8000`
- Environment variables:
  ```
  DATABASE_URL=postgresql://postgres:your-password@taskmanager-db:5432/taskmanager
  SECRET_KEY=your-super-secret-key-change-in-production
  ```
- Dependencies: Add `taskmanager-db`
- Click "Deploy"

### 5. **Deploy React Frontend**
- Click "New Service" → "Container"
- Service name: `taskmanager-frontend`
- Source: Upload your frontend folder or connect GitHub
- Build command: `npm install && npm run build`
- Run command: `npx serve -s build -l 3000`
- Port: `3000`
- Environment variables:
  ```
  REACT_APP_API_URL=https://your-backend-url.northflank.app
  ```
- Dependencies: Add `taskmanager-backend`
- Click "Deploy"

### 6. **Configure Domains**
- Backend: `api.yourdomain.com` or Northflank subdomain
- Frontend: `app.yourdomain.com` or Northflank subdomain

## 🔧 Environment Variables

### Backend (.env)
```bash
DATABASE_URL=postgresql://postgres:your-password@taskmanager-db:5432/taskmanager
SECRET_KEY=your-super-secret-key-change-in-production
```

### Frontend (.env)
```bash
REACT_APP_API_URL=https://your-backend-url.northflank.app
```

## 🌐 Update CORS Settings

In `backend/app/main.py`, add your frontend domain:
```python
origins = [
    "http://localhost:3000",
    "https://your-frontend-domain.northflank.app",
    "https://your-custom-domain.com"
]
```

## ✅ Verification Steps

1. **Database**: Check connection in Northflank logs
2. **Backend**: Test API endpoints
3. **Frontend**: Verify API calls work
4. **Full Flow**: Test user registration → login → task creation

## 🚨 Troubleshooting

### Common Issues:
- **Database connection failed**: Check service dependencies
- **CORS errors**: Verify frontend domain in CORS settings
- **Build failures**: Check Dockerfile and build commands
- **Port conflicts**: Ensure correct port mappings

### Support:
- Northflank documentation
- Service logs in dashboard
- Health checks status

## 🎉 Success!
Once deployed, you'll have:
- ✅ Live backend API
- ✅ Live frontend app
- ✅ Live PostgreSQL database
- ✅ Full-stack portfolio project!

## 🔗 Next Steps
1. Update README.md with live URLs
2. Test all functionality
3. Share with potential employers!
4. Monitor performance and costs

---
*This guide assumes Northflank accepts your payment method. If not, see `deploy-backend.md` for alternatives.*
