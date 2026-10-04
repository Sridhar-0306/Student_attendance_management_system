# 🎓 Student Attendance Management System

> A modern, full-stack web application for efficient student attendance tracking and management built with the MERN stack.

## ✨ Features

- **👥 Student Management**: Complete CRUD operations for student records
- **📚 Class Management**: Create and manage classes with subjects and teachers  
- **✅ Attendance Tracking**: Mark daily attendance (Present/Absent/Late) for students
- **📊 Real-time Dashboard**: Overview with statistics and quick actions
- **📱 Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **🔔 Toast Notifications**: Instant feedback for all operations
- **🛡️ Data Validation**: Comprehensive input validation and error handling
- **📈 Attendance Reports**: Generate attendance statistics and summaries
- **🔍 Search & Filter**: Easy navigation and data retrieval
- **⚡ Performance Optimized**: Fast and efficient data operations

## 🛠️ Tech Stack

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Fast, unopinionated web framework
- **MongoDB** - NoSQL database for flexible data storage
- **Mongoose** - MongoDB object modeling for Node.js
- **Express Validator** - Input validation and sanitization
- **CORS** - Cross-origin resource sharing support

### Frontend
- **React 18** - Modern UI library with hooks
- **React Router** - Client-side routing and navigation
- **Axios** - Promise-based HTTP client for API calls
- **TailwindCSS** - Utility-first CSS framework for rapid UI development
- **React Toastify** - Elegant toast notifications
- **Responsive Design** - Mobile-first approach

### Development Tools
- **Concurrently** - Run multiple commands simultaneously
- **Nodemon** - Auto-restart server during development
- **ESLint** - Code quality and consistency

## 🚀 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas account)
- npm or yarn package manager

### Step-by-Step Setup

1. **Clone the Repository**
   ```bash
   git clone <your-repo-url>
   cd Student_Attendance_System
   ```

2. **Install Dependencies**
   ```bash
   # Install root dependencies
   npm install
   
   # Install backend dependencies
   cd backend && npm install
   
   # Install frontend dependencies
   cd ../frontend && npm install
   
   # Return to root directory
   cd ..
   ```

3. **Environment Configuration**
   ```bash
   # Navigate to backend directory
   cd backend
   
   # Create config.env file
   cp config.env.example config.env
   
   # Edit config.env with your MongoDB connection string
   MONGODB_URI=mongodb://localhost:27017/student_attendance
   PORT=5000
   NODE_ENV=development
   ```

4. **Start MongoDB**
   - **Local MongoDB**: Ensure MongoDB service is running
   - **MongoDB Atlas**: Use your cloud connection string in config.env

5. **Run the Application**
   ```bash
   # Development mode (both backend and frontend)
   npm run dev
   
   # Or run separately:
   npm run server    # Backend only (port 5000)
   npm run client    # Frontend only (port 3000)
   ```

6. **Access the Application**
   - **Frontend**: http://localhost:3000
   - **Backend API**: http://localhost:5000
   - **Health Check**: http://localhost:5000/api/health

## 📱 Screenshots

### 🏠 Homepage Dashboard

<img width="1920" height="1080" alt="Screenshot (281)" src="https://github.com/user-attachments/assets/2dcbc821-b3e4-48dd-95e1-6e59068dee7b" />


### 👥 Students Management

<img width="1920" height="1080" alt="Screenshot (282)" src="https://github.com/user-attachments/assets/8460e06b-2ce1-401e-8656-c9085ade95c8" />


### 📚 Classes Management  

<img width="1920" height="1080" alt="Screenshot (283)" src="https://github.com/user-attachments/assets/6de86f9b-e776-470d-846f-19d7f8b9db05" />


### ✅ Attendance Tracking

<img width="1920" height="1080" alt="Screenshot (284)" src="https://github.com/user-attachments/assets/714a54d6-c404-4c23-8949-9775519f563e" />


## 🌐 API Endpoints

### Students
- `GET /api/students` - Get all students
- `GET /api/students/:id` - Get student by ID
- `POST /api/students` - Create new student
- `PUT /api/students/:id` - Update student
- `DELETE /api/students/:id` - Delete student
- `GET /api/students/:id/attendance` - Get student attendance statistics

### Classes
- `GET /api/classes` - Get all classes
- `GET /api/classes/:id` - Get class by ID
- `POST /api/classes` - Create new class
- `PUT /api/classes/:id` - Update class
- `DELETE /api/classes/:id` - Delete class
- `GET /api/classes/:id/attendance-summary` - Get class attendance summary

### Attendance
- `GET /api/attendance` - Get all attendance records
- `GET /api/attendance/:id` - Get attendance record by ID
- `POST /api/attendance` - Mark attendance
- `PUT /api/attendance/:id` - Update attendance
- `DELETE /api/attendance/:id` - Delete attendance record
- `POST /api/attendance/bulk` - Bulk mark attendance
- `GET /api/attendance/stats/overview` - Get attendance statistics

## 📁 Project Structure

```
Student_Attendance_System/
├── backend/                 # Backend server
│   ├── models/             # MongoDB schemas
│   │   ├── Student.js      # Student model
│   │   ├── Class.js        # Class model
│   │   └── Attendance.js   # Attendance model
│   ├── routes/             # API endpoints
│   │   ├── students.js     # Student routes
│   │   ├── classes.js      # Class routes
│   │   └── attendance.js   # Attendance routes
│   ├── config.env          # Environment variables
│   ├── package.json        # Backend dependencies
│   └── server.js           # Express server
├── frontend/               # React application
│   ├── public/             # Static files
│   │   ├── index.html      # Main HTML file
│   │   ├── favicon.ico     # App icon
│   │   └── manifest.json   # PWA manifest
│   ├── src/                # Source code
│   │   ├── components/     # Reusable components
│   │   │   └── Navbar.js   # Navigation component
│   │   ├── pages/          # Page components
│   │   │   ├── Dashboard.js    # Dashboard page
│   │   │   ├── Students.js     # Students page
│   │   │   ├── Classes.js      # Classes page
│   │   │   └── Attendance.js   # Attendance page
│   │   ├── services/       # API services
│   │   │   └── api.js      # HTTP client setup
│   │   ├── App.js          # Main app component
│   │   ├── index.js        # App entry point
│   │   └── index.css       # Global styles
│   ├── package.json        # Frontend dependencies
│   ├── tailwind.config.js  # TailwindCSS configuration
│   └── postcss.config.js   # PostCSS configuration
├── package.json            # Root dependencies
└── README.md              # Project documentation
```

## 🧪 Testing

### Backend Testing
```bash
# Test backend connectivity and endpoints
node test-backend.js
```

### Frontend Testing
```bash
cd frontend
npm test
```

## 🚀 Quick Start Scripts

### Windows
```bash
# Double-click start.bat or run:
start.bat
```

### PowerShell
```powershell
# Run PowerShell script:
.\start.ps1
```

### Manual Start
```bash
# Start both servers
npm run dev

# Start backend only
npm run server

# Start frontend only  
npm run client
```

## 🔧 Configuration Options

### Environment Variables
```env
# Backend Configuration
MONGODB_URI=mongodb://localhost:27017/student_attendance
PORT=5000
NODE_ENV=development

# Frontend Configuration (optional)
REACT_APP_API_URL=http://localhost:5000/api
```

### MongoDB Connection
- **Local MongoDB**: `mongodb://localhost:27017/student_attendance`
- **MongoDB Atlas**: `mongodb+srv://username:password@cluster.mongodb.net/database`

## 🚨 Troubleshooting

### Common Issues

**Backend won't start**
- Check if MongoDB is running
- Verify MongoDB connection string in config.env
- Ensure port 5000 is available

**Frontend won't start**
- Check if backend is running on port 5000
- Verify all dependencies are installed
- Check for port conflicts on 3000

**Database connection errors**
- Verify MongoDB URI format
- Check network connectivity
- Ensure database user has proper permissions

**CORS errors**
- Backend has CORS enabled by default
- Check if backend is running before frontend

## 🚀 Deployment

### Backend Deployment
1. Set `NODE_ENV=production` in environment variables
2. Update MongoDB connection string for production
3. Deploy to platforms like Heroku, Railway, or AWS

### Frontend Deployment
1. Build the application: `npm run build`
2. Deploy the `build` folder to Netlify, Vercel, or AWS S3

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow existing code style and conventions
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. Check the existing [Issues](../../issues) section
2. Create a new issue with detailed information
3. Include error logs and steps to reproduce
4. Provide your environment details (OS, Node.js version, etc.)

## 🔮 Future Enhancements

- **🔐 User Authentication**: Login/logout with role-based access
- **👨‍🏫 Role Management**: Admin, Teacher, and Student roles
- **📧 Email Notifications**: Automated attendance reminders
- **📱 Mobile App**: Native mobile application
- **📊 Advanced Analytics**: Detailed reports and insights
- **🔄 Bulk Operations**: Import/export functionality
- **🔍 Advanced Search**: Filtering and search capabilities
- **📈 Attendance Trends**: Pattern analysis and predictions
- **🔗 API Integration**: Connect with other school systems

## 🙏 Acknowledgments

- Built with ❤️ using the MERN stack
- Inspired by the need for efficient attendance management
- Special thanks to the open-source community

---

**⭐ Star this repository if you find it helpful!**

**🔗 Connect with us**: [GitHub](https://github.com/Sridhar-0306) | [LinkedIn](https://www.linkedin.com/in/usridhar/)

**📧 Contact**: sridhar.u2007@gmail.com

---

*Made with ❤️  By Sridhar💕*
