# flutter_frontend

A Flutter app that will send a Wikipedia URL to a backend to convert it into a Neo4j graph.

## Environment configuration

This app uses flutter_dotenv to configure the backend base URL.

1) Copy the example env file:
   cp .env.example .env

2) Set the backend URL:
   BACKEND_BASE_URL=http://10.0.2.2:3001

Notes:
- Android emulator: use http://10.0.2.2:<port> to reach services running on your host machine (localhost on host).
- iOS simulator: http://localhost:<port> usually works to reach host services.
- Physical devices: set BACKEND_BASE_URL to an address reachable from the device (e.g., your machine’s LAN IP).

## Running

- After updating .env, run:
  flutter pub get
  flutter run

## Troubleshooting

- If you get backend connection errors, verify BACKEND_BASE_URL and that the backend is running and reachable.
- Ensure the .env file is listed in pubspec.yaml assets (already configured).
