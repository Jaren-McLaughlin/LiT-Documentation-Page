# Containers

This folder contains the container-side code used for the POC workflow (`token.js`, `backendBot.js`, and `mockClient.js`).

## Docs

- [API docs for container JS code](./api.md)

## Setup (POC)

Install:
- Docker
- Node.js

From this directory:

```bash
cd server/containers
npm i
sudo docker compose up
```

## Configure `LIVEKIT_URL` from ngrok

Get your ngrok public URL:

```bash
curl http://localhost:4040/api/tunnels
```

You will see something like:

`"public_url":"https://&lt;randomStuff&gt;.ngrok-free.app"`

Replace `https://` with `wss://`, then set it in your `.env` file:

`LIVEKIT_URL=&lt;your-wss-url&gt;`

## Useful commands

Generate a session token:

```bash
node token.js &lt;roomName&gt; &lt;username&gt;
```

Run the bot and join a session:

```bash
node backendBot.js &lt;roomName&gt; &lt;languages&gt;
```

`&lt;languages&gt;` is a comma-separated list such as `es,en,fr`.

Run the mock client:

1. Create `server/prerecordedAudio/`
2. Add WAV files (for example `en.wav`, `es.wav`, `fr.wav`)
3. Run:

```bash
node mockClient.js &lt;roomName&gt; &lt;languages&gt;
```

`token.js`, `backendBot.js`, and `mockClient.js` all have defaults, so arguments are optional unless you want custom values.