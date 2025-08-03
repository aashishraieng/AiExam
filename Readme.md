
Live Demo 🌐
The application is deployed on Render and can be accessed at: https://ai-exam-frontend.onrender.com


AiEXAM: The AI-Powered Examination Platform

AiEXAM is a comprehensive, full-stack web application designed to modernize the academic examination process. It provides a seamless and intuitive platform for both students and teachers, incorporating features for exam creation, scheduling, AI-powered evaluation, and real-time feedback.

Key Features 📚
Role-Based Dashboards: Separate, feature-rich dashboards for students and teachers provide a personalized experience.

Dynamic Exam Creation: Teachers can create exams with various question types, including multiple-choice and subjective questions.

AI-Powered Evaluation: The platform leverages AI to automatically evaluate subjective answers, providing instant feedback and saving valuable time for educators.

Secure, Real-Time Exams: Students can take exams in a secure, full-screen environment with real-time monitoring for violations.

Instant Results and Analytics: Get immediate results and detailed analytics to track performance and identify areas for improvement.

Comprehensive Timetabling: A centralized system for scheduling and viewing exam timetables.

Issue Reporting System: A built-in ticketing system allows students to report any issues directly to their teachers.

Tech Stack 💻
Category	Technology
Frontend	React, Framer Motion, Tailwind CSS, Recharts
Backend	Node.js, Express.js
Database	MongoDB
Deployment	Render

Export to Sheets
Getting Started 🚀
Prerequisites
Node.js

npm (or yarn)

MongoDB

Installation
Clone the repository:

Bash

git clone https://github.com/your-repo/aiexam.git
cd aiexam
Install backend dependencies:

Bash

cd src 
npm install
Install frontend dependencies:

Bash

cd ../src
npm install
Configuration
Backend Environment Variables: Create a .env file in the src directory and add the following:

MONGO_URI: Your MongoDB connection string.

JWT_SECRET: A secret key for JWT token generation.

Frontend Environment Variables: Create a .env file in the src directory and add your backend API URL:

VITE_API_BASE_URL: The URL of your backend server.

Running the Application
Start the backend server:

Bash

cd src
npm start
Start the frontend development server:

Bash

cd ../src
npm run dev
Project Structure 📁
├── src               # Frontend
│   ├── assets
│   ├── components
│   ├── context
│   ├── hooks
│   ├── pages
│   ├── routes
│   └── services
├── src              # Backend
│   ├── controllers
│   ├── middlewares
│   ├── models
│   ├── routes
│   └── utils
└── server.js         # Backend server entry point








Of course, here is a brief description of each file and folder in your project.

Backend (src directory)
server.js: The main entry point for your backend application. It sets up the Express server, connects to MongoDB, and registers all the API routes.

controllers: This folder contains the business logic of your application. Each file corresponds to a specific part of your application (e.g., authController.js for handling user authentication, examController.js for managing exams).

authController.js: Handles user registration, login, and fetching user data.

dashboardController.js: Manages the data for the teacher's dashboard, including statistics, recent activity, and to-do lists.

examController.js: Contains the logic for creating and managing exams.

issueController.js: Handles the creation and management of student-reported issues.

questionController.js: Manages the creation of questions for exams.

studentController.js: Contains the logic for student-specific actions, such as fetching timetables, starting exams, and viewing results.

teacherController.js: Manages teacher-specific actions, like creating exams, evaluating submissions, and publishing results.

middlewares: This folder contains functions that run between the request and the response.

authmiddleware.js: Verifies JWT tokens to protect routes and authorizes users based on their roles (student or teacher).

multer.middleware.js: Handles file uploads.

validator.middleware.js: Validates incoming request data.

models: This folder defines the structure of your data in the MongoDB database. Each file represents a collection in the database.

exam.model.js: Defines the schema for exams.

evaluation.model.js: Defines the schema for AI and teacher evaluations.

issue.model.js: Defines the schema for student-reported issues.

question.model.js: Defines the schema for questions within an exam.

student.model.js: Defines the schema for student data.

submission.model.js: Defines the schema for student exam submissions.

teacher.model.js: Defines the schema for teacher data.

todo.model.js: Defines the schema for the teacher's to-do list.

routes: This folder defines the API endpoints for your application.

authRoutes.js: Defines the routes for user authentication (login, register).

dashboardRoutes.js: Defines the routes for the teacher dashboard.

examRoutes.js: Defines the routes for creating exams.

issueRoutes.js: Defines the routes for managing student-reported issues.

questionRoutes.js: Defines the routes for adding questions to exams.

studentRoutes.js: Defines the routes for student-specific actions.

teacherRoutes.js: Defines the routes for teacher-specific actions.

utils: This folder contains helper functions and classes that can be used throughout the application.

ApiError.js: A custom error class for handling API errors.

ApiResponse.js: A helper class for sending standardized API responses.

asyncHandler.js: A wrapper for handling asynchronous functions in Express to catch errors.

cloudinary.js: A helper for uploading files to Cloudinary.

Frontend (src directory)
App.jsx: The main component of your React application. It sets up the routing for the entire application.

main.jsx: The entry point for your React application. It renders the App component and sets up the AuthProvider and BrowserRouter.

assets: This folder contains static assets like images.

components: This folder contains reusable React components that are used across different pages.

Footer.jsx: The footer component for the application.

Login.jsx: The login modal component.

LoginParticles.jsx: A component for the particle animation on the login screen.

RoleSelector.jsx: The initial page where users select their role (student or teacher).

StudentLogin.jsx: The login page for students.

TeacherLogin.jsx: The login page for teachers.

TestimonialChat.jsx: A component that displays testimonials in a chat-like interface.

context: This folder contains React context providers for managing global state.

AuthContext.jsx: Manages user authentication state and provides login, logout, and signup functions.

hooks: This folder contains custom React hooks for reusing component logic.

useAuth.js: A hook for accessing the AuthContext.

useExam.js: A hook for creating exams.

useQuestion.js: A hook for adding questions to exams.

pages: This folder contains the main pages of your application, which are rendered by the router.

StudentDashboard.jsx: The main dashboard for students.

StudentExam.jsx: The page where students can take exams.

StudentIssue.jsx: The page where students can report issues.

StudentProfile.jsx: The student's profile page.

StudentResult.jsx: The page where students can view their exam results.

StudentTimetable.jsx: The page where students can view their exam timetable.

TeacherDashboard.jsx: The main dashboard for teachers.

TeacherEvaluate.jsx: The page where teachers can evaluate student submissions.

TeacherEvaluation.jsx: The page where teachers can view and manage exam submissions for evaluation.

TeacherExam.jsx: The page where teachers can create and manage exams.

TeacherIssue.jsx: The page where teachers can view and respond to student-reported issues.

TeacherMainDashboard.jsx: The main dashboard page for teachers, showing stats and recent activity.

TeacherPreviousPapers.jsx: The page where teachers can view previously created exams.

TeacherProfile.jsx: The teacher's profile page.

TeacherStatistics.jsx: A page displaying statistics for teachers.

TeacherSubmissions.jsx: A page for viewing all submissions for a specific exam.

TeacherTimetable.jsx: The page where teachers can schedule exams.

routes: This folder contains the routing configuration for the application.

AppRoutes.jsx: Defines all the routes for the application, including public and protected routes.

services: This folder contains functions for making API calls to the backend.

api.js: Sets up the Axios client for making API requests.

apiServices.js: Contains all the functions for making API calls to the backend.

utils: This folder contains utility functions for the frontend.

handleToken.js: Contains functions for managing JWT tokens in local storage.







Prerequisites
Before you begin, make sure you have the following installed on your computer:

Git: To clone the repository. Download Git

Node.js and npm: To run the JavaScript code for both frontend and backend. Download Node.js (npm is included).

MongoDB: The database for your application. You can install it locally or use a free cloud service like MongoDB Atlas. Get MongoDB

Step 1: Clone the Repository
First, open your terminal or command prompt and clone the project from GitHub. Replace your-github-username/your-repo-name.git with the actual URL of your repository.

Bash

git clone https://github.com/your-github-username/your-repo-name.git

# Navigate into the newly created project folder
cd your-repo-name
Step 2: Set Up and Run the Backend
The backend server needs to be running first so the frontend can communicate with it.

Navigate to the Backend Directory:

Bash

cd src1
Install Dependencies:
This command reads the package.json file and installs all the necessary Node.js modules.

Bash

npm install
Create Environment File:
Create a new file named .env in the src1 directory. This file will store your secret keys and database connection string. Add the following content to it:

Code snippet

# Your MongoDB connection string (replace with your actual string)
MONGO_URI=mongodb://localhost:27017/aiexam

# A strong, random string for signing tokens
JWT_SECRET=your_super_secret_jwt_key_that_is_long_and_random
Important: If you're using MongoDB Atlas, get the connection string from your cluster's dashboard.

Start the Backend Server:

Bash

npm start
If everything is set up correctly, you should see a message in your terminal like:

MongoDB connected ✅
Server running on port 3003 🚀
Leave this terminal window open. The backend is now running and listening for requests.

Step 3: Set Up and Run the Frontend
Now, let's get the user interface running. Open a new terminal window or tab.

Navigate to the Frontend Directory:
From the project's root directory:

Bash

cd src
Install Dependencies:
Just like the backend, the frontend also has its own set of dependencies.

Bash

npm install
Create Environment File:
Create a new file named .env in the src directory. This tells your frontend where to find the backend API.

Code snippet

# The URL where your backend server is running
VITE_API_BASE_URL=http://localhost:3003
Start the Frontend Development Server:

Bash

npm run dev
This will start the Vite development server. Your terminal will show a message similar to this:

  VITE v5.x.x  ready in xxx ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
Step 4: Use the Website
You're all set!

Open your web browser (like Chrome, Firefox, or Edge).

Go to the Local URL provided by the frontend server, which is typically http://localhost:5173.

You should now see your AiEXAM website's homepage. You can register new student or teacher accounts, log in, and use all the features of your application locally.