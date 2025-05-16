# AI Chatbot Frontend

A modern, responsive React frontend for interacting with the Spring Boot Chatbot API.

## Features

- Real-time chat interface with the AI chatbot
- Session management for persistent conversations
- Chat history retrieval
- Responsive design for desktop and mobile devices
- API health status monitoring
- Loading indicators for better user experience

## Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)
- Spring Boot Chatbot API running (default: http://localhost:8080)

## Installation

1. Clone the repository:
   ```
   git clone <repository-url>
   cd chatbot-frontend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Configure the API endpoint:
   - Open `src/services/ChatService.js`
   - Update the `API_BASE_URL` constant if your Spring Boot API is running on a different URL

## Running the Application

Start the development server:
```
npm start
```

The application will be available at [http://localhost:3000](http://localhost:3000).

## Building for Production

Create a production build:
```
npm run build
```

The build artifacts will be stored in the `build/` directory.

## API Integration

This frontend is designed to work with the Spring Boot Chatbot API. It communicates with the following endpoints:

- `POST /api/chat/send` - Send a message to the chatbot
- `GET /api/chat/history` - Retrieve conversation history
- `GET /api/chat/health` - Check API health status
- `GET /api/chat/config` - Get API configuration

## Project Structure

- `src/App.js` - Main application component
- `src/App.css` - Application styles
- `src/components/` - Reusable UI components
- `src/services/` - API service layer

## Session Management

The application uses browser localStorage to persist the session ID between page reloads. This allows users to continue their conversations even after closing and reopening the browser.

## Customization

- Colors and styling can be modified in `src/App.css`
- API endpoint configuration is in `src/services/ChatService.js`

## License

This project is licensed under the MIT License - see the LICENSE file for details.
