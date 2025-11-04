NLP to SQL System
A powerful natural language to SQL conversion system with multi-user support, workspace management, and persistent conversation history.

Overview
This system allows users to interact with databases using natural language. It converts natural language questions into SQL queries, executes them, and returns the results along with natural language explanations. The system supports multiple users, each with their own workspaces connected to different databases, and maintains conversation history for context-aware responses.

Features
Natural Language to SQL: Convert natural language questions into SQL queries
Multi-user Authentication: JWT-based authentication system
Workspace Management: Each user can create multiple workspaces connected to different databases
Session Management: Each workspace can have multiple chat sessions (conversations)
Persistent Context: Conversation history is stored in a vector database for context-aware responses
Pagination: Large result sets are paginated for better performance
MongoDB Integration: User data, workspaces, and sessions are stored in MongoDB
Vector Database: Conversation context is stored in a vector database for semantic search
Intelligent Query Analysis:
Handles conversational queries without SQL
Detects and processes "why" questions with causal analysis
Supports multi-query analysis for complex questions
Handles pagination for large result sets
Architecture
The system consists of two main components:

Backend API: A FastAPI application that handles:

User authentication
Workspace and session management
Natural language to SQL conversion
Database querying
Context management
Frontend Application: A Next.js application that provides:

User registration and login
Workspace and session management
Chat interface for natural language queries
SQL and results display
Pagination for large result sets
Setup
Prerequisites
Python 3.8+
MongoDB 4.4+
PostgreSQL (for the target databases)
Node.js 16+ (for frontend)
Backend Setup
Clone the repository
Install dependencies:
pip install -r requirements.txt
Create a .env file with the required environment variables (see BACKEND_README.md)
Start the server:
uvicorn api:app --reload
For more details, see BACKEND_README.md.

Frontend Setup
Navigate to the frontend directory:
cd nlp-sql-chatbot
Install dependencies:
npm install
Create a .env.local file with the required environment variables (see FRONTEND_README.md)
Start the development server:
npm run dev
For more details, see FRONTEND_README.md.

Usage
Register a new user account
Create a workspace connected to your database
Create a session within the workspace
Start asking questions in natural language
View the generated SQL, results, and explanations
API Documentation
The API documentation is available at /docs when the backend server is running.

Security Considerations
Database passwords are stored in MongoDB. In a production environment, consider encrypting these passwords.
JWT tokens have a 24-hour expiration by default. Adjust this as needed for your security requirements.
The API uses CORS with "*" as the allowed origin. In production, specify your frontend domains.
