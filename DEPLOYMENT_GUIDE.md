# HealthBridge Deployment Guide

## ✅ Frontend Ready for Vercel

Your frontend is **100% ready** to deploy on Vercel!

### Steps to Deploy Frontend on Vercel:

1. **Push to GitHub:**
```bash
git add .
git commit -m "Ready for Vercel deployment"
git push origin main
```

2. **Deploy on Vercel:**
   - Go to https://vercel.com/
   - Click "New Project"
   - Import your GitHub repository
   - Environment Variables:
     - `VITE_API_URL` = Your backend URL (e.g., https://your-backend.com/api)
   - Click "Deploy"

### Frontend Configuration:
✅ `vercel.json` - Automatically configured
✅ `.vercelignore` - Build files excluded
✅ `package.json` - Updated with latest dependencies
✅ Build command: `npm run build`
✅ Framework: Vite (optimal for Vercel)

---

## ⚠️ Backend Deployment (Choose One Option)

Your backend uses **Express + Socket.IO** which requires a persistent server.
Vercel supports serverless but requires setup modifications.

### Option 1: Deploy on Railway (Recommended) ⭐
Railway is the easiest alternative to Heroku.

**Steps:**
1. Go to https://railway.app/
2. Create a new project → Deploy from GitHub
3. Add environment variables from your `.env` file:
   - `MONGO_URI`
   - `JWT_SECRET`
   - `GEMINI_API_KEY`
   - `PORT` (optional, Railway sets it)
4. Deploy!

**Cost:** Free tier available, $5/month paid tier

### Option 2: Deploy on Render
1. Go to https://render.com/
2. Create new Web Service
3. Connect GitHub repository
4. Build command: `npm install`
5. Start command: `npm start`
6. Add environment variables
7. Deploy!

**Cost:** Free tier available

### Option 3: Deploy Backend on Vercel (with modifications)
If you want everything on Vercel, the backend needs conversion to serverless functions.
This requires restructuring the code (more complex).

---

## 📋 Pre-Deployment Checklist

- [x] Frontend dependencies updated
- [x] Backend dependencies updated
- [x] AI Assistant removed
- [x] `.env` file configured locally
- [ ] Push to GitHub
- [ ] Set environment variables on hosting platform
- [ ] Test the deployed URLs

---

## 🚀 Quick Deployment Summary

**Frontend:** Vercel (automatic)
**Backend:** Railway or Render (recommended)
**Database:** MongoDB Atlas (already configured)

Once both are deployed:
- Update `VITE_API_URL` in Vercel to your backend URL
- Backend will have a unique URL from Railway/Render
- Connect frontend to backend via environment variables

**Estimated deployment time:** 5-10 minutes per service
