# collaborative-board

A real-time shared drawing board: everyone who opens the page draws on the same canvas, and each stroke appears on the other screens straight away.

## How it works

- **Client (`client/`)**: React with an HTML canvas. After each stroke it sends the canvas image over Socket.IO and redraws when another user's image arrives.
- **Server (`server/`)**: Express and Socket.IO. It relays `canvas-data` from one user to all the others.

## Run

```bash
cd server && npm install && npm start    # http://localhost:5000
cd client && npm install && npm start    # http://localhost:3000
```

Open the client in two browser windows and draw in one.
