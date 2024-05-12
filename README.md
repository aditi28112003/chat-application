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

Environment Configurations:

      PORT: Port number for the server
      MONGO_DB_URI=
      JWT_SECRET=
      OPENAI_API_KEY=
      NODE_ENV=development
      


