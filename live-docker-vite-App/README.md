## 🚀 Vite + React + Docker (Live Reload)
A simple setup to run a Vite React application inside Docker with live reload, without Docker Compose or Nginx.

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

## Project Structure
project/
├── Dockerfile
├── .dockerignore
├── vite.config.js
├── package.json
├── src/
│   ├── App.jsx
│   └── main.jsx
└── README.md

$mkdir vite-docker-app
$cd vite-docker-app
$npm create vite@latest . -- --template react
$npm install 

## Verify the app runs locally
# run dev server
$npm run dev

Open the shown URL (usually http://localhost:5173) and confirm the app loads. Stop server with Ctrl+C.

## Build Image
$docker build -t vite-live .

## Run Container (Live Reload)
Windows PowerShell:

$docker  run -d  -p  5173:5173  -v  ${PWD}:/app vite-live

Linux/Mac:

$docker run -it -p "$PWD":/app vite-live

## Open in Browser
http://localhost:5173

## Check container logs:

$docker logs <container_id>


