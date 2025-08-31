# 🚀 Deploy with ngrok - Instant Public Access

## ⚡ **Why ngrok?**
- **100% FREE** - No credit cards, no limits
- **Instant deployment** - Works in 5 minutes
- **Public URLs** - Share with employers immediately
- **No platform restrictions** - Works from your local machine

## 🎯 **What You Get**
- ✅ **Live backend API** (publicly accessible)
- ✅ **Live frontend** (already on Vercel)
- ✅ **Full functionality** (employers can test everything)
- ✅ **Professional URLs** (looks like real deployment)

## 🚀 **Quick Setup (5 minutes)**

### **Step 1: Install ngrok**
```bash
# Install globally
npm install -g ngrok

# Or download from ngrok.com
```

### **Step 2: Start Your App Locally**
```bash
# Start all services
docker-compose up -d

# Verify they're running
docker-compose ps
```

### **Step 3: Expose Backend Publicly**
```bash
# Expose backend on port 8000
ngrok http 8000

# You'll get a URL like: https://abc123.ngrok.io
```

### **Step 4: Update Frontend API URL**
In your Vercel frontend, update the API URL to your ngrok URL.

## 🔗 **Your Live URLs**
- **Frontend**: `https://your-app.vercel.app` ✅ (Already live!)
- **Backend**: `https://abc123.ngrok.io` ✅ (From ngrok)
- **Database**: Local (PostgreSQL running in Docker)

## 🌐 **Update CORS for ngrok**
Add your ngrok URL to `backend/app/main.py`:
```python
origins = [
    "http://localhost:3000",
    "https://your-app.vercel.app",
    "https://abc123.ngrok.io"  # Your ngrok URL
]
```

## ✅ **Test Everything**
1. **Frontend**: Visit your Vercel URL
2. **Backend**: Test API at `https://abc123.ngrok.io/docs`
3. **Full Flow**: Register → Login → Create Tasks

## 🎉 **Benefits for Employers**
- **Live demo** they can use immediately
- **Professional appearance** (looks like real deployment)
- **Full functionality** (all features working)
- **No setup required** (just visit URLs)

## 🔄 **Keep ngrok Running**
- **Free tier**: 8 hours per session
- **Restart**: Just run `ngrok http 8000` again
- **Custom domains**: Available with paid plans

## 🚨 **Important Notes**
- **Keep your computer running** while sharing
- **Restart ngrok** if you need a fresh URL
- **Update frontend** when ngrok URL changes

## 💡 **Perfect for Portfolio**
This gives you a **fully functional live application** that employers can:
- ✅ **Visit immediately**
- ✅ **Test all features**
- ✅ **See your full-stack skills**
- ✅ **Use as a reference**

---
*This is your backup plan if Northflank doesn't work. It's actually a great solution for portfolio projects!*
