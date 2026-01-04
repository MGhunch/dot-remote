# Dot Remote

Phone-based remote trigger for Hunch Dot system via n8n webhooks.

## Setup

1. Create a new GitHub repo called `Dot_Remote`
2. Upload these files
3. Connect to Railway (New Project → Deploy from GitHub)
4. Railway auto-deploys on push

## Configuration

Edit `public/index.html` and update the webhook URLs:

```javascript
const WEBHOOKS = {
    todo: 'https://your-n8n.app/webhook/dot-todo',
    wip: 'https://your-n8n.app/webhook/dot-wip',
    update: 'https://your-n8n.app/webhook/dot-update'
};
```

## Structure

```
dot-remote/
├── index.js           ← Express server
├── package.json
├── README.md
└── public/
    ├── index.html     ← The remote interface
    ├── fonts/
    │   └── BebasNeue-Regular.ttf
    └── images/
        ├── header-logo.png
        └── ai2-logo.png
```

## Adding to Home Screen (iOS)

1. Open the Railway URL in Safari
2. Tap Share → Add to Home Screen
3. Name it "Dot Remote"
