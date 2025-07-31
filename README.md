# School Management App
Project Overview
The School Management App is a comprehensive platform designed to streamline daily academic activities for both teachers and students. It provides intuitive interfaces for managing tasks, quizzes, and monitoring student progress in real-time.

Check out here : https://school-management-system-dlj3.onrender.com

# Features
-> For Students
1) Daily Task Management: Students can update the status of their daily tasks (Not Started, In Progress, Completed) and add descriptions.

2) Daily Quiz: Students can attempt daily quizzes published by teachers.

3) Submission History: View a history of submitted tasks and quiz scores.

-> For Teachers
1) Quiz Creation: Teachers can create and publish daily multiple-choice quizzes.

2) Student Progress Monitoring: View a detailed overview of each student's daily task status, description, and quiz scores.

# Technologies Used
Frontend: React.js

Styling: Tailwind CSS

Icons: Lucide React

Backend/Database: Firebase (Authentication, Firestore)

Bundler: Webpack

Transpiler: Babel

# Getting Started
Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

# Prerequisites
Before you begin, ensure you have the following installed on your system:

Node.js: Download & Install Node.js (LTS version recommended)

npm (Node Package Manager): Comes bundled with Node.js.

Git: Download & Install Git

# Installation
Clone the repository (if you have it hosted on Git):

git clone <your-repository-url>
cd my-school-app # Navigate into your project directory

If you manually created the project structure as provided, navigate to your project folder.

Install dependencies:
In the project root directory, run:

npm install

# Firebase Setup
This application uses Firebase for authentication and data storage. You'll need your own Firebase project configuration.

Create a Firebase Project:

Go to the Firebase Console.

Click "Add project" and follow the steps to create a new project.

# Register a Web App:

In your Firebase project, click the "Web" icon (</>) to add a web app.

Follow the setup steps. When prompted, copy your Firebase configuration object. It will look something like this:

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID"
};

Enable Firebase Services:

In the Firebase Console, go to Authentication and enable "Email/Password" sign-in method.

Go to Firestore Database and create a new database. Choose "Start in production mode" for security, but remember to set up Firestore Security Rules for proper access control (e.g., allow read/write for authenticated users for users and public/data/quizzes collections).

Create a .env file:
In the root directory of your project (same level as package.json), create a new file named .env.

Add your Firebase Configuration to .env:
Paste your Firebase configuration into the .env file, prefixed with REACT_APP_ for each variable. Also, define REACT_APP_APP_ID for local development.

# .env
REACT_APP_FIREBASE_API_KEY="YOUR_API_KEY"
REACT_APP_FIREBASE_AUTH_DOMAIN="YOUR_AUTH_DOMAIN"
REACT_APP_FIREBASE_PROJECT_ID="YOUR_PROJECT_ID"
REACT_APP_FIREBASE_STORAGE_BUCKET="YOUR_STORAGE_BUCKET"
REACT_APP_FIREBASE_MESSAGING_SENDER_ID="YOUR_MESSAGING_SENDER_ID"
REACT_APP_FIREBASE_APP_ID="YOUR_APP_ID"
REACT_APP_FIREBASE_MEASUREMENT_ID="YOUR_MEASUREMENT_ID"

# A unique identifier for your application's data in Firestore
REACT_APP_APP_ID="default-school-app"

Remember to replace YOUR_API_KEY, YOUR_AUTH_DOMAIN, etc., with your actual Firebase project values.

Add .env to .gitignore:
Ensure your .env file is not committed to version control. Open (or create) .gitignore in your project root and add:

# .gitignore
.env

Running the Application
After installing dependencies and setting up Firebase:

Start the development server:

npm start

This will compile your React application and open it in your default web browser, usually at http://localhost:3000/.

Usage
Welcome Page: Choose to Continue as Student or Continue as Teacher.

Login/Sign Up: Use the provided forms to log in or create a new account.

Student Sign Up: Requires Full Name and Roll Number.

Teacher Sign Up: Requires Full Name and Subject.

Dashboard:

Student: Update daily task status, take daily quizzes, and view submission history.

Teacher: Create/edit daily quizzes and monitor student progress.

# Deployment
To deploy this application to a hosting service (e.g., Netlify, Vercel, Render):

Build the project for production:

npm run build

This will create an optimized dist folder ready for deployment.

Configure Environment Variables on your Hosting Platform:

Instead of the .env file, you will set the REACT_APP_FIREBASE_API_KEY, REACT_APP_FIREBASE_AUTH_DOMAIN, etc., directly in your hosting platform's dashboard under "Environment Variables" or "Build Settings".

Also, set the REACT_APP_APP_ID variable to a unique ID for your deployed application (e.g., production-school-app). This ensures your production data is separate from your local development data in Firebase.
