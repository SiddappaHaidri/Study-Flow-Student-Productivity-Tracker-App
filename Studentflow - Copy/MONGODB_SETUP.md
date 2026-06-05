# MongoDB Setup for StudentFlow

## Issue Identified
The registration is failing because MongoDB is not running locally. The backend server shows:
```
MongoDB connection error: MongooseServerSelectionError: connect ECONNREFUSED ::1:27017
```

## Quick Solutions for Hackathon

### Option 1: Use MongoDB Atlas (Recommended - Fastest)
1. Go to https://www.mongodb.com/atlas
2. Sign up for free account
3. Create a free cluster (M0 Sandbox)
4. Click "Connect" → "Connect your application"
5. Copy the connection string
6. Update your `.env` file with:
```
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/studentflow?retryWrites=true&w=majority
```

### Option 2: Install MongoDB Locally
1. Download MongoDB Community Server: https://www.mongodb.com/try/download/community
2. Install and run MongoDB service
3. The app will connect to: `mongodb://localhost:27017/studentflow`

### Option 3: Use In-Memory Database (For Demo Only)
For quick demo without database setup, the server will run but features requiring data persistence won't work.

## Current Status
✅ Backend Server: Running on http://localhost:5000
✅ Frontend App: Running on http://localhost:3000
❌ Database: Not connected (MongoDB required for registration/login)

## Next Steps
1. Choose one MongoDB setup option above
2. Restart the backend server: `cd server && npm start`
3. Test registration in the browser

The app will work perfectly once MongoDB is connected!
