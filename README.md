# Workflow + Calendar Intelligence Suite

**1. Automate Anything. 
2. Schedule Everything. 
3. Smartly.**

A comprehensive workflow and calendar automation platform built with React, Node.js, and modern web technologies.

## 🚀 Features

### Core Functionality

- **Smart Calendar Automation** - Automatically schedule meetings, events, and tasks
- **Workflow Automation** - Create powerful workflows that automate repetitive tasks
- **Intelligent Scheduling** - AI-powered scheduling that finds optimal time slots
- **Team Collaboration** - Seamlessly coordinate with your team
- **Analytics & Insights** - Detailed analytics on productivity and efficiency
- **Enterprise Security** - Bank-level security with end-to-end encryption

### User Experience

- **Beautiful Modern UI** - Built with Tailwind CSS and Framer Motion
- **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- **Collapsible Navigation** - Smart navigation that adapts to user state
- **Real-time Updates** - Live updates and notifications
- **Dark/Light Mode** - Coming soon

## 🛠️ Tech Stack

### Frontend

- **React 18** - Modern React with hooks and functional components
- **React Router** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Smooth animations and transitions
- **Lucide React** - Beautiful icons
- **Axios** - HTTP client for API calls

### Backend

- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **JWT** - JSON Web Tokens for authentication
- **bcryptjs** - Password hashing
- **Helmet** - Security middleware
- **CORS** - Cross-origin resource sharing
- **Rate Limiting** - API rate limiting

### Development

- **Concurrently** - Run multiple commands simultaneously
- **Nodemon** - Auto-restart server during development
- **PostCSS** - CSS processing
- **Autoprefixer** - CSS vendor prefixing

## 📦 Installation

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Quick Start

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd workflow-calendar-automation
   ```

2. **Install dependencies**

   ```bash
   # Install root dependencies
   npm install

   # Install client dependencies
   cd client && npm install
   cd ..
   ```

3. **Set up environment variables**

   ```bash
   # Create .env file in root directory
   cp .env.example .env
   ```

4. **Start development servers**

   ```bash
   # Start both frontend and backend
   npm run dev

   # Or start them separately:
   npm run server    # Backend only (port 5000)
   npm run client    # Frontend only (port 3000)
   ```

5. **Open your browser**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000
   - Health Check: http://localhost:5000/api/health

## 🏗️ Project Structure

```
workflow-calendar-automation/
├── client/                 # React frontend
│   ├── public/            # Static files
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── contexts/      # React contexts
│   │   ├── pages/         # Page components
│   │   ├── App.js         # Main app component
│   │   └── index.js       # Entry point
│   ├── package.json
│   └── tailwind.config.js
├── server/                # Node.js backend
│   ├── routes/           # API routes
│   │   ├── auth.js       # Authentication routes
│   │   ├── users.js      # User management
│   │   ├── workflows.js  # Workflow management
│   │   └── calendar.js   # Calendar management
│   └── index.js          # Server entry point
├── package.json
└── README.md
```

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key

# Client URL (for CORS)
CLIENT_URL=http://localhost:3000

# Database (for future implementation)
# DATABASE_URL=mongodb://localhost:27017/workflow-suite
```

### Tailwind CSS Configuration

The project uses a custom Tailwind configuration with:

- Custom color palette
- Custom animations
- Responsive design utilities
- Component classes

## 🚀 Available Scripts

### Root Directory

```bash
npm run dev          # Start both frontend and backend
npm run server       # Start backend only
npm run client       # Start frontend only
npm run build        # Build frontend for production
npm run install-all  # Install all dependencies
```

### Client Directory

```bash
npm start           # Start development server
npm run build       # Build for production
npm test            # Run tests
npm run eject       # Eject from Create React App
```

## 📱 Features Overview

### Authentication System

- User registration and login
- JWT-based authentication
- Password hashing with bcrypt
- Protected routes
- Social login (Google, Twitter)

### Dashboard

- Real-time statistics
- Recent activities feed
- Upcoming tasks
- Quick actions
- Performance metrics

### Calendar Management

- Event creation and management
- Availability scheduling
- Meeting automation
- Calendar integration
- Time slot finding

### Workflow Automation

- Visual workflow builder
- Trigger-based automation
- Action sequences
- Template library
- Execution monitoring

### User Management

- Team collaboration
- Role-based permissions
- User profiles
- Activity tracking
- Search functionality

## 🔒 Security Features

- **JWT Authentication** - Secure token-based authentication
- **Password Hashing** - bcrypt for password security
- **CORS Protection** - Cross-origin request protection
- **Rate Limiting** - API rate limiting to prevent abuse
- **Helmet.js** - Security headers middleware
- **Input Validation** - Request validation and sanitization

## 🎨 UI/UX Features

### Design System

- **Modern Design** - Clean, professional interface
- **Responsive Layout** - Mobile-first approach
- **Smooth Animations** - Framer Motion animations
- **Accessibility** - WCAG compliant components
- **Loading States** - Skeleton screens and spinners

### Navigation

- **Collapsible Sidebar** - Space-efficient navigation
- **Breadcrumbs** - Clear navigation hierarchy
- **Search Functionality** - Global search with filters
- **Quick Actions** - Contextual action buttons

## 🔧 API Endpoints

### Authentication

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update profile
- `PUT /api/auth/change-password` - Change password

### Users

- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id/role` - Update user role
- `GET /api/users/:id/stats` - Get user statistics
- `GET /api/users/:id/team` - Get team members
- `GET /api/users/search/:query` - Search users

### Workflows

- `GET /api/workflows` - Get all workflows
- `GET /api/workflows/:id` - Get workflow by ID
- `POST /api/workflows` - Create new workflow
- `PUT /api/workflows/:id` - Update workflow
- `DELETE /api/workflows/:id` - Delete workflow
- `POST /api/workflows/:id/execute` - Execute workflow
- `GET /api/workflows/:id/stats` - Get workflow statistics
- `GET /api/workflows/templates` - Get workflow templates

### Calendar

- `GET /api/calendar/events` - Get all events
- `GET /api/calendar/events/:id` - Get event by ID
- `POST /api/calendar/events` - Create new event
- `PUT /api/calendar/events/:id` - Update event
- `DELETE /api/calendar/events/:id` - Delete event
- `GET /api/calendar/availability/:userId` - Get user availability
- `PUT /api/calendar/availability/:userId` - Update availability
- `POST /api/calendar/find-slots` - Find available time slots
- `POST /api/calendar/schedule` - Schedule meeting automatically
- `GET /api/calendar/stats` - Get calendar statistics

## 🚀 Deployment

### Frontend Deployment (Vercel/Netlify)

```bash
cd client
npm run build
# Deploy the build folder
```

### Backend Deployment (Heroku/Railway)

```bash
# Set environment variables
# Deploy the server folder
```

### Docker Deployment

```dockerfile
# Dockerfile example
FROM node:16-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 5000
CMD ["npm", "run", "server"]
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Documentation**: [Link to docs]
- **Issues**: [GitHub Issues](https://github.com/your-repo/issues)
- **Discussions**: [GitHub Discussions](https://github.com/your-repo/discussions)
- **Email**: support@workflowsuite.com

## 🗺️ Roadmap

### Phase 1 (Current)

- ✅ Basic authentication
- ✅ Dashboard with statistics
- ✅ Calendar management
- ✅ Workflow creation
- ✅ User management

### Phase 2 (Next)

- 🔄 Advanced workflow builder
- 🔄 Calendar integrations (Google, Outlook)
- 🔄 Email automation
- 🔄 Team collaboration features
- 🔄 Mobile app

### Phase 3 (Future)

- 📋 AI-powered scheduling
- 📋 Advanced analytics
- 📋 Enterprise features
- 📋 API marketplace
- 📋 White-label solutions

---

**Built with ❤️ by the WorkflowSuite Team**
