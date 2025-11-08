# Minimal Tic Tac Toe Game

A fun, minimal-size JavaScript tic tac toe game that can be deployed on a VPS using a simple Python HTTP server.

## Features

- Single HTML file with embedded CSS and JavaScript (no external dependencies)
- Fully functional tic tac toe game with human vs AI opponent
- Small file size (under 10KB)
- Responsive design that works on desktop and mobile
- Fun, engaging UI with smooth animations
- Score tracking with local storage persistence
- Smart AI opponent with strategic moves

## Quick Start

### Option 1: Python HTTP Server (Recommended)

1. Make sure you have Python 3 installed
2. Navigate to the project directory
3. Run the following command:

```bash
python3 -m http.server 8000
```

4. Open your browser and go to `http://localhost:8000`

### Option 2: Any HTTP Server

Since this is a single HTML file, you can serve it with any web server:
- Apache
- Nginx
- Node.js (with express or http-server)
- PHP built-in server
- Or even open `index.html` directly in your browser

## How to Play

- You are X (blue), the AI is O (purple)
- Click any empty cell to make your move
- The AI will automatically respond after your move
- Win by getting 3 in a row (horizontal, vertical, or diagonal)
- Your scores are saved automatically and persist between sessions

## Game Controls

- **New Game**: Start a fresh game while keeping scores
- **Reset Scores**: Clear all scores and start fresh

## Deployment on VPS

1. Upload the `index.html` file to your VPS
2. Navigate to the directory containing the file
3. Start the Python HTTP server:

```bash
python3 -m http.server 8000
```

4. For production deployment, consider:
   - Using a process manager like `systemd` or `pm2`
   - Setting up a reverse proxy with Nginx
   - Configuring HTTPS with SSL certificates

## Technical Details

- **File Size**: ~9KB (gzipped)
- **Dependencies**: None (pure HTML/CSS/JavaScript)
- **Browser Support**: Modern browsers (ES6+)
- **Responsive**: Works on desktop, tablet, and mobile
- **Storage**: Uses localStorage for score persistence

## AI Strategy

The AI opponent uses a simple but effective strategy:
1. Try to win if possible
2. Block player from winning
3. Take center position
4. Take corner positions
5. Take any available position

Enjoy the game! 🎮
