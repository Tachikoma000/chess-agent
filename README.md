# AI-Powered Chess Game

This is an interactive chess game that runs in the browser. Users can play against an AI agent powered by OpenAI's GPT-4. The backend is built in Rust using the Rig library, which manages the LLM interactions and handles API calls to OpenAI. The frontend is built with JavaScript, HTML, and CSS, using `chessboard.js` for the chessboard interface.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Play Against AI**: Engage in a chess game against an AI agent powered by GPT-4, providing challenging and dynamic gameplay.
- **Interactive Chessboard**: A user-friendly, draggable chessboard built with `chessboard.js`.
- **Real-Time API Interaction**: The frontend communicates with the Rust backend to get AI moves based on the current game state.
- **Responsive Design**: A sleek and responsive design that works across different devices.

## Tech Stack

- **Rust**: Backend server and AI agent management using the Rig library.
- **JavaScript**: Frontend logic and interaction with the chessboard.
- **HTML/CSS**: Structure and styling of the web interface.
- **`chessboard.js`**: JavaScript library for the chessboard interface.
- **OpenAI GPT-4**: AI model for generating chess moves.

## Installation

### Prerequisites

- Rust (latest stable version)
- Node.js and npm
- OpenAI API key

### Backend Setup

1. Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/ai-powered-chess-game.git](https://github.com/Tachikoma000/chess-agent.git)
    cd ai-powered-chess-game/backend
    ```

2. Install dependencies:
    ```bash
    cargo build
    ```

3. Set up environment variables:
    ```bash
    export OPENAI_API_KEY=your_openai_api_key
    ```

4. Run the backend server:
    ```bash
    cargo run
    ```

### Frontend Setup

1. Navigate to the frontend directory:
    ```bash
    cd ../frontend
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Start the development server:
    ```bash
    npm start
    ```

## Usage

Once the backend and frontend servers are running, open your browser and navigate to `http://localhost:3000` to start playing the chess game. Make your move, and the AI will respond in real time!

## API Documentation

### `POST /make_move`

- **Description**: Receives the current board state from the frontend and returns the AI's move.
- **Request Body**: JSON object containing the board state in FEN format.
    ```json
    {
        "board_state": "rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1"
    }
    ```
- **Response**: JSON object containing the AI's move.
    ```json
    {
        "move": "e2e4"
    }
    ```

## Development

### Setting Up the Development Environment

1. Ensure Rust and Node.js are installed on your machine.
2. Clone the repository and follow the installation instructions above for both backend and frontend.
3. Modify the backend code to change the AI behavior or frontend code to customize the UI.

### File Structure

- **backend/**: Contains the Rust code, including AI agent management and API server.
- **frontend/**: Contains the JavaScript, HTML, and CSS files for the web interface.
- **docs/**: Documentation and design specs.

### Key Components

- **Rust AI Agent**: Manages the interaction with GPT-4 and processes AI moves.
- **Chessboard Interface**: Built with `chessboard.js`, handles user interactions.
- **API Endpoints**: Facilitate communication between frontend and backend.

### Testing

- Manual testing: Play games against the AI to ensure smooth operation.
- Unit tests: Add unit tests for critical functions in both frontend and backend.

## Contributing

We welcome contributions! Please fork the repository, create a new branch for your feature or bug fix, and submit a pull request.
