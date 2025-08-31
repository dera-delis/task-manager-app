# 🚀 Backend Deployment Guide - Render

## 📋 **Prerequisites**
- GitHub account connected to Render
- Repository: `dera-delis/task-manager-app`

## 🎯 **Step-by-Step Deployment**

### **1. Create Web Service**
- **Type**: Web Service
- **Repository**: `dera-delis/task-manager-app`
- **Branch**: `main`

### **2. Service Configuration**
- **Name**: `task-manager-backend`
- **Environment**: `Python 3`
- **Build Command**: `pip install -r backend/requirements.txt`
- **Start Command**: `cd backend && uvicorn app.main:app --host 0.0.0.0 --port $PORT`
- **Root Directory**: (leave empty)

### **3. Environment Variables**
```
SECRET_KEY=your-super-secret-production-key-here
DATABASE_URL=postgresql://postgres:password@your-db-host:5432/taskmanager
```

### **4. Create PostgreSQL Database**
- **Type**: PostgreSQL
- **Name**: `task-manager-db`
- **Database**: `taskmanager`
- **User**: `postgres`
- **Plan**: Free

### **5. Update CORS Origins**
The backend is already configured to allow:
- Vercel frontend: `https://task-manager-k1mi43d8y-pedros-projects-da4369b0.vercel.app`
- Render domains: `https://*.onrender.com`
- Vercel domains: `https://*.vercel.app`

## 🔗 **After Deployment**
1. Copy the backend URL (e.g., `https://task-manager-backend.onrender.com`)
2. Update frontend environment variable `REACT_APP_API_URL`
3. Test the connection between frontend and backend

## 📚 **Useful Render URLs**
- **Dashboard**: https://dashboard.render.com
- **Documentation**: https://render.com/docs
- **Status Page**: https://status.render.com

