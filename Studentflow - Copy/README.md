# 🚀 StudentFlow - AI-Powered Student Productivity Tracker

A comprehensive productivity tracking application designed specifically for students, featuring AI-powered task management, study sessions, goal tracking, and detailed analytics.

## ✨ Features

### 📋 Task Management
- **Smart Task Scheduling** with AI-based priority ranking
- **Categories & Tags** for better organization
- **Due Date Management** with overdue alerts
- **Subtasks** for breaking down complex assignments
- **Progress Tracking** with visual indicators

### 🎯 Goal Setting
- **Long-term Goals** with milestone tracking
- **Progress Visualization** with percentage completion
- **Custom Categories** (Study Time, Tasks, Grades, Skills, Health)
- **Deadline Management** with automatic reminders

### ⏱️ Study Timer
- **Pomodoro Technique** with customizable intervals
- **Focus Score Calculation** based on interruptions
- **Session Notes** for reflection
- **Productivity Analytics** per session
- **Auto-switch** between work and break periods

### 📊 Analytics & Insights
- **Dashboard Overview** with key metrics
- **Study Time Tracking** with daily/weekly/monthly views
- **Productivity Trends** with visual charts
- **Task Completion Statistics**
- **AI-powered Insights** for optimization
- **Comparison Analytics** (current vs previous periods)

### 🎮 Gamification
- **Experience Points (XP)** for completed tasks and sessions
- **Level System** with progression tracking
- **Achievement Badges** for milestones
- **Study Streaks** for consistency
- **Leaderboard** (future feature)

### 🎨 Modern UI/UX
- **Responsive Design** for all devices
- **Dark/Light Mode** toggle
- **Real-time Notifications**
- **Smooth Animations** and micro-interactions
- **Accessibility Features**

## 🛠️ Tech Stack

### Frontend
- **React 18** with TypeScript
- **Tailwind CSS** for styling
- **Framer Motion** for animations
- **Chart.js** for data visualization
- **React Router** for navigation
- **Axios** for API calls
- **Socket.io Client** for real-time features

### Backend
- **Node.js** with Express
- **MongoDB** with Mongoose ODM
- **JWT** for authentication
- **Socket.io** for real-time communication
- **bcryptjs** for password hashing
- **Helmet** for security
- **Rate Limiting** for API protection

## 🚀 Quick Start

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd Studentflow
```

2. **Install dependencies**
```bash
# Install root dependencies
npm install

# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install
```

3. **Set up environment variables**
```bash
# Copy environment template
cp .env.example .env

# Edit .env with your configuration
# Set MONGODB_URI, JWT_SECRET, etc.
```

4. **Start the application**
```bash
# From root directory - runs both server and client
npm run dev

# Or run separately:
npm run server  # Starts backend on port 5000
npm run client  # Starts frontend on port 3000
```

5. **Access the application**
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000
- API Health Check: http://localhost:5000/api/health

## 📁 Project Structure

```
Studentflow/
├── client/                 # React frontend
│   ├── public/            # Static assets
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── contexts/       # React contexts
│   │   ├── pages/          # Page components
│   │   ├── App.js          # Main app component
│   │   └── index.js        # Entry point
│   ├── package.json
│   └── tailwind.config.js
├── server/                 # Node.js backend
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── index.js           # Server entry point
│   └── package.json
├── .env.example           # Environment template
├── package.json           # Root package.json
└── README.md
```

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update profile

### Tasks
- `GET /api/tasks` - Get user tasks
- `POST /api/tasks` - Create task
- `PUT /api/tasks/:id` - Update task
- `DELETE /api/tasks/:id` - Delete task
- `GET /api/tasks/stats/overview` - Task statistics

### Goals
- `GET /api/goals` - Get user goals
- `POST /api/goals` - Create goal
- `PUT /api/goals/:id` - Update goal
- `DELETE /api/goals/:id` - Delete goal
- `POST /api/goals/:id/progress` - Add progress

### Study Sessions
- `GET /api/sessions` - Get study sessions
- `POST /api/sessions` - Create session
- `POST /api/sessions/:id/end` - End session
- `GET /api/sessions/active/current` - Get active session

### Analytics
- `GET /api/analytics/dashboard` - Dashboard analytics
- `GET /api/analytics/insights` - AI insights
- `GET /api/analytics/comparison` - Period comparison

## 🎯 MVP Features (Hackathon Ready)

### Core Features (24-hour build)
- ✅ User authentication & profile management
- ✅ Task CRUD operations with AI priority
- ✅ Goal setting with progress tracking
- ✅ Study timer with Pomodoro technique
- ✅ Basic analytics dashboard
- ✅ Responsive UI with modern design

### Advanced Features (Post-hackathon)
- 🔄 Real-time notifications
- 🔄 AI study recommendations
- 🔄 Social features & leaderboards
- 🔄 Advanced analytics & insights
- 🔄 Mobile app (React Native)

## 🏗️ Architecture

### Database Schema
- **Users**: Authentication, profile, stats, preferences
- **Tasks**: Title, description, category, priority, due date, AI priority
- **Goals**: Title, target, progress, milestones, deadlines
- **Study Sessions**: Duration, focus score, productivity rating
- **Achievements**: Gamification elements

### AI Features
- **Task Priority Algorithm**: Calculates urgency based on due date, priority, and user patterns
- **Study Recommendations**: Suggests optimal study times based on performance data
- **Productivity Insights**: Analyzes patterns and provides optimization tips

### Real-time Features
- **Live Notifications**: Session updates, reminders, achievements
- **Real-time Analytics**: Dashboard updates without page refresh
- **Collaborative Features** (future): Study groups, shared goals

## 🎨 UI/UX Design Principles

### Design System
- **Color Palette**: Blue (primary), Purple (accent), Green (success), Orange (warning)
- **Typography**: Inter font family for readability
- **Spacing**: Consistent 8px grid system
- **Components**: Reusable card, button, form components

### User Experience
- **Intuitive Navigation**: Clear menu structure with breadcrumbs
- **Progressive Disclosure**: Show relevant information based on context
- **Micro-interactions**: Subtle animations for better engagement
- **Accessibility**: WCAG 2.1 AA compliance

## 🚀 Deployment

### Frontend (Vercel)
```bash
# Build for production
cd client
npm run build

# Deploy to Vercel
vercel --prod
```

### Backend (Railway/Heroku)
```bash
# Set environment variables
# MONGODB_URI, JWT_SECRET, NODE_ENV=production

# Deploy
git push heroku main
```

### Environment Variables
- `MONGODB_URI`: MongoDB connection string
- `JWT_SECRET`: Secret for JWT token signing
- `CLIENT_URL`: Frontend URL for CORS
- `NODE_ENV`: Environment (development/production)

## 🧪 Testing

### Frontend Tests
```bash
cd client
npm test
```

### Backend Tests
```bash
cd server
npm test
```

### API Testing
Use Postman collection or similar tools to test API endpoints.

## 📈 Performance Optimization

### Frontend
- **Code Splitting**: Lazy loading for routes
- **Image Optimization**: WebP format, lazy loading
- **Bundle Analysis**: Regular bundle size monitoring
- **Caching**: Service worker for offline support

### Backend
- **Database Indexing**: Optimized queries
- **Rate Limiting**: API protection
- **Caching**: Redis for frequently accessed data
- **Compression**: Gzip for API responses

## 🔒 Security Features

- **JWT Authentication**: Secure token-based auth
- **Password Hashing**: bcryptjs for password security
- **Rate Limiting**: Prevent API abuse
- **CORS Configuration**: Proper cross-origin setup
- **Input Validation**: Sanitize all user inputs
- **Helmet.js**: Security headers

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🏆 Hackathon Success Metrics

### Technical Excellence
- ✅ Clean, maintainable code
- ✅ Responsive design
- ✅ Real-time features
- ✅ Modern tech stack

### User Experience
- ✅ Intuitive interface
- ✅ Smooth animations
- ✅ Accessibility features
- ✅ Mobile responsiveness

### Innovation
- ✅ AI-powered features
- ✅ Gamification elements
- ✅ Advanced analytics
- ✅ Productivity insights

## 🎯 Demo Script

1. **Registration & Login** - Show user authentication flow
2. **Dashboard Overview** - Display key metrics and quick actions
3. **Task Management** - Create, prioritize, and complete tasks
4. **Study Timer** - Start Pomodoro session with focus tracking
5. **Goal Setting** - Create goals with milestones and track progress
6. **Analytics** - Show productivity insights and trends
7. **Profile & Settings** - Demonstrate personalization options

## 📞 Support

For questions, issues, or contributions:
- Create an issue on GitHub
- Email: support@studentflow.app
- Documentation: [Wiki](https://github.com/username/studentflow/wiki)

---

**Built with ❤️ for students who want to study smarter, not harder!**
