## NLP to SQL System

A powerful natural language to SQL conversion system with multi-user support, workspace management, and persistent conversation history.

## Overview
This system allows users to interact with databases using natural language. It converts natural language questions into SQL queries, executes them, and returns the results along with natural language explanations. The system supports multiple users, each with their own workspaces connected to different databases, and maintains conversation history for context-aware responses.

## Features
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
## The system consists of two main components:

## Backend API: A FastAPI application that handles:

User authentication 

Workspace and session management 

Natural language to SQL conversion

Database querying

Context management

## Frontend Application: A Next.js application that provides:

User registration and login

Workspace and session management

Chat interface for natural language queries

SQL and results display

Pagination for large result sets

Setup



