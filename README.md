# 🎓 Edusphere
Empowering careers through interactive placement preparation.
EduSphere is a comprehensive, modern e-learning platform specifically designed for placement preparation. Built with cutting-edge technologies, it provides an immersive learning experience that bridges the gap between academic knowledge and industry requirements.

📋 Table of Contents
🌟 Overview
✨ Key Features
🛠️ Technology Stack
🚀 Quick Start
📖 Detailed Setup
🎯 Usage Guide
📚 API Documentation
🏗️ Architecture
🧪 Testing
🚀 Deployment
🤝 Contributing
📄 License
📞 Support & Contact
🌟 Overview
EduSphere revolutionizes placement preparation by offering:

**Comprehensive Curriculum**: Covers technical skills, aptitude, HR preparation, and soft skills
**Industry-Aligned Content**: Updated regularly to match current market demands
**Interactive Learning**: Engaging multimedia content and hands-on practice
**Performance Analytics**: Detailed insights into learning progress and weak areas
**Community Learning**:Collaborative environment with peer discussions and mentorship
🎯 Mission Statement
To democratize quality placement preparation and help students achieve their career aspirations through technology-driven, accessible education.

✨ Key Features
👤 User Experience
🔐 Advanced Authentication: Multi-factor authentication with social login options
📱 Responsive Design: Seamless experience across all devices
🌙 Dark/Light Mode: Customizable UI themes
🔔 Smart Notifications: Personalized reminders and updates
♿ Accessibility: WCAG 2.1 compliant for inclusive learning
📚 Learning Management
📖 Dynamic Course Catalog: Categorized courses with difficulty levels
🎥 Rich Media Content: HD videos, interactive coding environments, and visual aids
📝 Adaptive Assessments: AI-powered quizzes that adjust to learning pace
📊 Progress Analytics: Detailed performance tracking and insights
🏆 Gamification: Badges, leaderboards, and achievement systems
💬 Community & Collaboration
💭 Discussion Forums: Topic-based forums with threaded conversations
👥 Study Groups: Form and join study groups with peers
🎯 Mentorship Program: Connect with industry professionals
📋 Doubt Resolution: 24/7 doubt clearing sessions
🔧 Administrative Tools
📊 Analytics Dashboard: Comprehensive insights for administrators
👥 User Management: Advanced user roles and permissions
📚 Content Management: Drag-and-drop course builder
💰 Revenue Tracking: Integrated payment and revenue analytics
🔌 Integrations
💳 Payment Gateway: Secure payments via Stripe and Razorpay
📧 Email Service: Automated notifications via SendGrid
☁️ Cloud Storage: AWS S3 for media content
📊 Analytics: Google Analytics and custom tracking
🛠️ Technology Stack
Frontend
⚛️ React 18 - Modern React with Concurrent Features
🔄 Next.js 13 - App Router with Server Components
📘 TypeScript - Type-safe development
🎨 Tailwind CSS - Utility-first styling
📊 Recharts - Interactive data visualizations
🔄 React Query - Powerful data synchronization
📱 Framer Motion - Smooth animations
Backend
🟢 Node.js - Runtime environment
⚡ Express.js - Web application framework
🗄️ MongoDB - NoSQL database with Mongoose ODM
🔒 JWT & Passport.js - Authentication and authorization
📧 Nodemailer - Email services
🔍 Elasticsearch - Advanced search capabilities
DevOps & Deployment
🐳 Docker - Containerization
☁️ AWS/Vercel - Cloud hosting
🔄 GitHub Actions - CI/CD pipeline
📊 Monitoring - Sentry for error tracking
🗄️ Redis - Caching and session storage
Development Tools
📏 ESLint & Prettier - Code quality and formatting
🧪 Jest & React Testing Library - Comprehensive testing
📚 Storybook - Component documentation
🔍 Husky - Git hooks for code quality
🚀 Quick Start
Get EduSphere running locally in 5 minutes:

# Clone the repository
git clone https://github.com/N-nishita/placement-preparation-app.git
cd placement-preparation-app

# Install dependencies and start development
npm run setup && npm run dev
Access the application at http://localhost:3000

Default Admin Credentials:

Email: admin@edusphere.com
Password: admin123
📖 Detailed Setup
Prerequisites
Ensure you have the following installed:

Node.js (v16.0.0 or higher) - Download
MongoDB (v5.0 or higher) - Download
Git - Download
Docker (optional) - Download
Environment Configuration
Create environment files for different environments:

.env.development
# Application
NODE_ENV=development
PORT=5000
CLIENT_URL=http://localhost:3000

# Database
MONGO_URI=mongodb://localhost:27017/edusphere_dev
REDIS_URL=redis://localhost:6379

# Authentication
JWT_SECRET=your_super_secret_jwt_key_here
JWT_EXPIRE=7d
REFRESH_TOKEN_SECRET=your_refresh_token_secret

# Email Configuration
EMAIL_SERVICE=gmail
EMAIL_USERNAME=your_email@gmail.com
EMAIL_PASSWORD=your_app_password

# Payment Gateway
STRIPE_PUBLISHABLE_KEY=pk_test_your_stripe_key
STRIPE_SECRET_KEY=sk_test_your_stripe_secret
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_SECRET=your_razorpay_secret

# Cloud Storage
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret
AWS_BUCKET_NAME=edusphere-media

# External APIs
GOOGLE_ANALYTICS_ID=GA_MEASUREMENT_ID
SENTRY_DSN=your_sentry_dsn
Installation Steps
Clone and Setup

git clone https://github.com/N-nishita/placement-preparation-app.git
cd placement-preparation-app

Install Dependencies
# Install root dependencies
npm install

# Install frontend dependencies
cd client && npm install

# Install backend dependencies
cd ../server && npm install

Database Setup
# Start MongoDB (if running locally)
mongod

# Seed the database with initial data
npm run seed
Start Development Servers

# Start both frontend and backend
npm run dev

# Or start individually
npm run dev:client  # Frontend only
npm run dev:server  # Backend only

Docker Setup (Alternative)
# Build and run with Docker Compose
docker-compose up -d

# View logs
docker-compose logs -f


🎯 Usage Guide
For Students
Getting Started

Sign up with email or social login
Complete profile setup and skill assessment
Browse recommended courses based on your goals
Learning Path

Follow personalized learning paths
Complete modules in sequence or skip to specific topics
Practice with coding challenges and mock interviews
Track Progress

Monitor completion rates and performance scores
Review detailed analytics and improvement suggestions
Earn certificates upon course completion
For Instructors
Content Creation

Use the intuitive course builder
Upload videos, create quizzes, and assignments
Set up automated grading and feedback
Student Management

Monitor student progress and engagement
Provide personalized feedback and mentorship
Conduct live sessions and webinars
For Administrators
Platform Management

Access comprehensive analytics dashboard
Manage users, courses, and content
Configure system settings and integrations
Business Intelligence

Track revenue and user growth metrics
Analyze course effectiveness and student outcomes
Generate custom reports and insights
📚 API Documentation
Base URL
Development: http://localhost:5000/api/v1
Production: https://api.edusphere.com/v1
Authentication
All API requests require authentication via JWT tokens:

Authorization: Bearer <your_jwt_token>
Core Endpoints
Authentication
POST /auth/register          # User registration
POST /auth/login            # User login
POST /auth/refresh          # Refresh JWT token
POST /auth/forgot-password  # Password reset request
PUT  /auth/reset-password   # Reset password
Users
GET    /users/profile       # Get user profile
PUT    /users/profile       # Update user profile
GET    /users/progress      # Get learning progress
POST   /users/avatar        # Upload profile picture
Courses
GET    /courses             # List all courses
GET    /courses/:id         # Get course details
POST   /courses/:id/enroll  # Enroll in course
GET    /courses/:id/content # Get course content
POST   /courses/:id/review  # Add course review
Assessments
GET    /assessments/:courseId    # Get course assessments
POST   /assessments/submit       # Submit assessment
GET    /assessments/results/:id  # Get assessment results
For complete API documentation with examples, visit: API Docs

🏗️ Architecture
System Architecture
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   React Client  │───▶│   Next.js API   │───▶│   Express API   │
│   (Frontend)    │    │   (Middleware)  │    │   (Backend)     │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                                                       │
                       ┌─────────────────┐            │
                       │     Redis       │◀───────────┤
                       │   (Caching)     │            │
                       └─────────────────┘            │
                                                       │
                       ┌─────────────────┐            │
                       │    MongoDB      │◀───────────┘
                       │   (Database)    │
                       └─────────────────┘
Database Schema
Users Collection
{
  _id: ObjectId,
  email: String,
  password: String (hashed),
  profile: {
    firstName: String,
    lastName: String,
    avatar: String,
    bio: String,
    skills: [String],
    experience: String
  },
  role: String, // 'student', 'instructor', 'admin'
  preferences: {
    theme: String,
    notifications: Boolean,
    language: String
  },
  progress: {
    coursesEnrolled: [ObjectId],
    coursesCompleted: [ObjectId],
    totalPoints: Number,
    achievements: [ObjectId]
  },
  createdAt: Date,
  updatedAt: Date
}
Courses Collection
{
  _id: ObjectId,
  title: String,
  description: String,
  instructor: ObjectId,
  category: String,
  level: String, // 'beginner', 'intermediate', 'advanced'
  duration: Number, // in hours
  price: Number,
  thumbnail: String,
  curriculum: [{
    module: String,
    lessons: [{
      title: String,
      type: String, // 'video', 'article', 'quiz'
      content: String,
      duration: Number,
      resources: [String]
    }]
  }],
  ratings: {
    average: Number,
    count: Number
  },
  enrollmentCount: Number,
  isPublished: Boolean,
  createdAt: Date,
  updatedAt: Date
}

🧪 Testing
Running Tests
# Run all tests
npm test

# Run tests with coverage
npm run test:coverage

# Run tests in watch mode
npm run test:watch

# Run specific test suite
npm run test -- --testNamePattern="User Authentication"
Test Structure
tests/
├── unit/           # Unit tests for individual functions
├── integration/    # Integration tests for API endpoints
├── e2e/           # End-to-end tests with Cypress
└── __mocks__/     # Mock files for testing
Testing Strategy
Unit Tests: Jest for business logic and utility functions
Component Tests: React Testing Library for UI components
Integration Tests: Supertest for API endpoint testing
E2E Tests: Cypress for complete user workflows
Performance Tests: Lighthouse CI for performance monitoring

🚀 Deployment
Production Deployment

Using Vercel (Recommended for Frontend)
# Install Vercel CLI
npm i -g vercel

# Deploy to Vercel
vercel --prod


Using Docker
# Build production images
docker build -t edusphere-client ./client
docker build -t edusphere-server ./server

# Run with docker-compose
docker-compose -f docker-compose.prod.yml up -d
Environment Variables for Production
NODE_ENV=production
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/edusphere
REDIS_URL=redis://redis-server:6379
JWT_SECRET=your_production_jwt_secret
# ... other production variables
Monitoring & Logging
Error Tracking: Sentry integration for real-time error monitoring
Performance: New Relic for application performance monitoring
Logs: Winston for structured logging
Uptime: Pingdom for service availability monitoring
🤝 Contributing
We welcome contributions from the community! Here's how you can help:

Getting Started

Fork the Repository
git clone https://github.com/N-nishita/placement-preparation-app.git
cd placement-preparation-app
Create Feature Branch

git checkout -b feature/amazing-feature
Make Changes

Follow our coding standards
Add tests for new features
Update documentation
Submit Pull Request

git commit -m "Add amazing feature"
git push origin feature/amazing-feature
Development Guidelines
Code Style
Use TypeScript for type safety
Follow ESLint and Prettier configurations
Write meaningful commit messages using Conventional Commits
Maintain test coverage above 80%
Commit Message Format
type(scope): subject

body

footer
Example:

feat(auth): add social login integration

- Implement Google OAuth 2.0
- Add Facebook login support
- Update user schema for social profiles

Closes #123
Issue Templates
🐛 Bug Report: Report bugs with detailed reproduction steps
✨ Feature Request: Suggest new features or improvements
📚 Documentation: Improvements to documentation
❓ Question: Ask questions about the project
Recognition
Contributors are recognized in our Hall of Fame and receive special badges on the platform.

