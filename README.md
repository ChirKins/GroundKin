# GroundKin: Casual Workforce Management Platform
 <!-- logo -->

GroundKin is a comprehensive digital platform designed to bring structure, transparency, and opportunity to the casual labor market. We connect skilled tradespeople (Masons, Carpenters, Plumbers, Electricians, etc.) with contractors, streamlining the entire process from job discovery and time tracking to professional certification and verifiable work history.

Table of Contents
Overview

Key Features

For Workers (Tradespeople)

For Contractors/Foremen

Technology Stack

Installation & Setup

Usage

Worker Onboarding

Daily Workflow

Contractor Workflow

Project Structure

API Documentation

Contributing

License

Support & Contact

Overview
The informal casual labor sector often lacks the tools for workers to formally track their experience and for employers to verify a worker's history. WorkLedger solves this by providing a secure, easy-to-use application that:

Empowers Workers: Gives tradespeople a digital portfolio of their work, automates attendance and wage tracking, and generates verifiable recommendation letters.

Streamlines Hiring: Allows contractors to post jobs and find vetted workers with proven track records directly through the platform.

Promotes Professionalism: Guides uncertified workers towards official certification bodies to improve their skills and employability.

Key Features
For Workers (Tradespeople)
Self-Registration & Profile Management: Create a detailed profile showcasing your skills, experience, and portfolio of past projects.

Site & Project Registration: Register and manage the different sites and projects you are working on.

Digital Time Clock: Clock in and out of work shifts directly from your mobile device with GPS verification for accuracy.

Wage & Dues Tracker: Log daily payments received. The app automatically calculates totals and helps you keep a clear financial record.

Digital Work Report: Generate tailored reports on your earnings, attendance, and work history for personal records or to show potential employers.

Automated Recommendation Letters: Instantly generate a professional, verifiable recommendation letter based on your completed projects and tracked attendance. Contractors can confirm the letter's validity through the app.

Job Marketplace: Browse and apply for job openings posted by verified contractors directly within the app.

Certification Hub: Inquire about professional certifications. Access direct links and information to accredited skill certification bodies for your trade.

For Contractors/Foremen
Managed Team Dashboard: View all workers registered on your active sites, monitor their real-time clock-ins/outs, and track overall site attendance.

Verification Portal: Receive and verify requests for worker recommendation letters. Check a worker's historical performance before hiring.

Job Posting Board: Create and publish detailed job listings specifying required skills, location, duration, and pay rate.

Applicant Management: Review applications, check applicant profiles (including past recommendations and work history), and hire directly through the platform.

Site Management: Create and manage different work sites, assigning teams and foremen as needed.

Technology Stack
Frontend: React.js / React Native (for cross-platform mobile app) or Flutter

Backend: Node.js with Express.js or Python with Django

Database: PostgreSQL (for relational data like users, jobs) with MongoDB or Firebase (for flexible data like logs, reports)

Authentication: JWT (JSON Web Tokens) for secure login

Cloud Storage: AWS S3 or Firebase Storage (for storing portfolio images, generated PDFs)

Geolocation: Google Maps API / Geolocation API

Reporting: A library like PDFKit (for Node) or ReportLab (for Django) to generate PDF reports and letters.

Deployment: Docker, AWS EC2 / Elastic Beanstalk, or Google Cloud Platform

Installation & Setup
Prerequisites
Node.js (v16 or higher) / Python (v3.8 or higher)

npm, yarn, or pip

PostgreSQL database

A mobile device (for testing the app) or a web browser

Local Development
Clone the repository:

bash
git clone https://github.com/your-organization/workledger.git
cd workledger
Install backend dependencies:

bash
cd backend
npm install
# or
pip install -r requirements.txt
Install frontend dependencies:

bash
cd ../frontend
npm install
Environment Setup:

Copy .env.example to .env in both /backend and /frontend directories.

Configure your database connection strings, JWT secret key, API keys for cloud storage and geolocation.

Database Migration:

bash
cd ../backend
npx sequelize-cli db:migrate
# or for Django
python manage.py migrate
Start the development servers:

Backend:

bash
npm run dev
# or
python manage.py runserver
Frontend (in a new terminal):

bash
cd ../frontend
npm start
Access the application:

Web App: Open http://localhost:3000

API Server: Running on http://localhost:5000

Usage
Worker Onboarding
Download the WorkLedger app from the Google Play Store or Apple App Store.

Select "Register as a Worker."

Fill in your personal details, trade skills, and experience.

Verify your email address and phone number.

Your profile is now active. Start applying for jobs or ask your foreman for your site's unique code to register your attendance.

Daily Workflow
Arrive at the site and open the app.

Enter the site code or select the active site from your list.

Tap "Clock In." Your time and location are recorded.

At the end of the day, tap "Clock Out."

If you receive a cash payment, you can log the amount in the "Daily Dues" section.

Contractor Workflow
Log in to the web portal.

From your dashboard, create a new job posting or a new site.

Share the generated site code with your workers so they can register.

Monitor the live attendance feed for your sites.

Review job applications and worker requests for recommendations.

Project Structure
text
workledger/
├── backend/                 # Backend API Server
│   ├── controllers/        # Route controllers
│   ├── models/            # Database models
│   ├── routes/            # API routes
│   ├── middleware/        # Auth & validation middleware
│   ├── utils/             # Helpers (PDF generation, etc.)
│   └── server.js          # App entry point
├── frontend/              # Web Application (for Contractors)
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.js
│   └── package.json
├── mobile-app/            # React Native/Flutter App (for Workers)
│   ├── src/
│   │   ├── screens/
│   │   ├── components/
│   │   └── navigation/
│   └── app.js
└── README.md
API Documentation
Comprehensive API documentation, detailing all endpoints for authentication, users, jobs, attendance, and reports, is available post-installation at /api-docs (powered by Swagger/OpenAPI).

Contributing
We welcome contributions! Please read our Contributing Guidelines for details on our code of conduct and the process for submitting pull requests.

License
This project is licensed under the MIT License - see the LICENSE.md file for details.

Support & Contact
Documentation: https://docs.workledger.app

Report a Bug: GitHub Issues

Email Support: support@workledger.app

Twitter: @WorkLedgerApp

Building a more transparent and professional future for casual work, one job at a time.
