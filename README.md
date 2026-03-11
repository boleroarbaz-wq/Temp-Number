# Webhook Server

A simple GitHub webhook server built with Express.js

## Setup

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file from `.env.example` and add your configuration:
```bash
cp .env.example .env
```

3. Run the server:
```bash
npm start
```

The server will listen on port 3000 by default.

## GitHub Webhook Configuration

1. Go to your repository Settings → Webhooks
2. Click "Add webhook"
3. Set the Payload URL to your server (e.g., https://your-domain.com/webhook)
4. Select "application/json" as Content type
5. Add your webhook secret
6. Select events to trigger the webhook
7. Click "Add webhook"

## Testing

Send a POST request to the webhook endpoint:
```bash
curl -X POST http://localhost:3000/webhook \
  -H "Content-Type: application/json" \
  -d '{"action": "opened"}'
```