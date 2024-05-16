# chat Application

This project is a comprehensive backend for a real-time chat application built using the MERN stack. It emphasizes Node.js and MongoDB for server-side logic and database management. 
The backend includes user authentication, real-time messaging using Socket.io, message storage in MongoDB, user online status management, and integration with a language model API for 
automated responses.
This README provides comprehensive documentation for the backend of a real-time chat application built using the MERN stack.
Setup and Run Instructions:

Clone the Repository:

bash

    git clone https://github.com/aditi28112003/chat-application
    cd real-time-chat-backend

Install Dependencies:

bash

    npm install

Set Environment Variables:
Create a .env file in the root directory and configure the following variables:

dotenv

    PORT=
    MONGO_DB_URI=
    JWT_SECRET=
    OPENAI_API_KEY=
    NODE_ENV=


Run the Server:

bash

    npm start

API Route Descriptions:

    User Authentication:

        POST /api/auth/register: Register a new user.
            Input: JSON object with email and password.
            Output: JSON object with userId and token.

        POST /api/auth/login: Log in an existing user.
            Input: JSON object with email and password.
            Output: JSON object with userId and token.

    Chat Functionality:

        GET /api/messages: Retrieve all messages.
            Output: Array of JSON objects representing messages.

        POST /api/messages: Send a new message.
            Input: JSON object with senderId, receiverId, and message.
            Output: JSON object representing the sent message.

    User Online Status and LLM Integration:

        PUT /api/users/status: Update user's online status.
            Input: JSON object with userId and status.
            Output: JSON object representing the updated user.

        POST /api/messages/llm: Send message with LLM integration.
            Input: JSON object with senderId, receiverId, and message.
            Output: JSON object representing the sent message or an automated response from LLM API.

This project is a comprehensive backend for a real-time chat application built using the MERN stack, focusing on Node.js and MongoDB for server-side logic and database management. It features user authentication, real-time messaging, user online status management, and integration with language model APIs for generating automated responses.
Features

    User Authentication:
        User registration and login with email and password.
        JWT (JSON Web Tokens) for managing authentication.

    Chat Functionality:
        Real-time messaging using Socket.io.
        Storage of all messages in MongoDB.
        Retrieval of message history for conversations between users.

    User Online Status and LLM Integration:
        Users can set their status to 'AVAILABLE' or 'BUSY'.
        Automatic generation of responses using a language model API when the recipient is 'BUSY'.
        Timely response management with a fallback message if the LLM API does not respond within 10 seconds.

    Basic Frontend (Optional):
        A simple frontend to demonstrate the backend functionalities.

Setup and Run Instructions
Prerequisites

    Node.js (v14.x or higher)
    MongoDB
    Git

Automatic Response from LLM:
        When a user with status 'BUSY' receives a message, an automatic response is generated using the LLM API.
        If the LLM API does not respond within 10 seconds, a standard message is sent indicating the user is unavailable.

Postman Collection

    Import the provided Postman collection hq_collection.json into Postman to test the API endpoints.

Necessary Environment Configurations

    Ensure the .env file contains valid configurations for MONGO_URI, JWT_SECRET, LLM_API_URL, and LLM_API_KEY
Environment Configurations:

      PORT: Port number for the server
      MONGO_DB_URI=
      JWT_SECRET=
      OPENAI_API_KEY=
      NODE_ENV=development
      


