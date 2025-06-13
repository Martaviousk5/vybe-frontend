# Vybe Frontend

A modern, responsive social media web app built with vanilla JavaScript, HTML5, and CSS3.

## 🚀 Features

- **Progressive Web App (PWA)** - Install on mobile/desktop
- **Responsive Design** - Works on all devices
- **Real-time Updates** - Socket.io integration ready
- **Offline Support** - Service Worker caching
- **Modern UI** - Smooth animations and transitions
- **Dark Theme** - Easy on the eyes

## 📋 Quick Start

### Option 1: Static Hosting (Simplest)

1. Upload all files to your hosting:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - Icon files

2. Update the API URL in `index.html`:
   ```javascript
   const API_URL = 'https://your-backend-url.onrender.com';
   ```

3. Access your site!

### Option 2: Local Development

1. Install a local server:
   ```bash
   npm install -g http-server
   ```

2. Run the server:
   ```bash
   http-server -p 8080
   ```

3. Open: http://localhost:8080

## 🚀 Deployment

### Deploy to GitHub Pages

1. Create GitHub repository
2. Upload all files
3. Go to Settings → Pages
4. Select source: main branch
5. Your site will be at: `https://[username].github.io/[repo-name]`

### Deploy to Netlify

1. Drag and drop your folder to [Netlify](https://netlify.com)
2. Get instant URL
3. Custom domain available

### Deploy to Vercel

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

## 📱 PWA Setup

To make the app installable:

1. Serve over HTTPS
2. Include manifest.json
3. Register service worker
4. Add app icons

## 🎨 Customization

### Change Colors

Edit the CSS variables in `index.html`:
```css
:root {
    --primary: #667eea;    /* Main color */
    --secondary: #764ba2;  /* Secondary color */
    --dark: #0a0618;      /* Background */
}
```

### Change App Name

1. Update in `index.html`:
   - `<title>` tag
   - `.logo` class content

2. Update in `manifest.json`:
   - `name` and `short_name`

## 📱 Mobile App

To convert to mobile app:

1. **Using Capacitor:**
   ```bash
   npm install @capacitor/core @capacitor/cli
   npx cap init
   npx cap add ios
   npx cap add android
   ```

2. **Using PWA:**
   - Users can install from browser
   - Add to home screen
   - Works like native app

## 🔗 API Integration

The app expects these endpoints:

- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/posts`
- `POST /api/posts`
- `POST /api/posts/:id/like`
- `GET /api/users/:username`
- `PUT /api/users/profile`

## 🐛 Troubleshooting

### CORS Issues
Make sure your backend has CORS enabled:
```javascript
app.use(cors());
```

### Service Worker Not Working
- Must serve over HTTPS (or localhost)
- Check browser console for errors
- Clear cache and reload

### Can't Connect to Backend
- Verify API_URL is correct
- Check backend is running
- Check for typos in URL

## 📄 License

MIT License - feel free to use for any project!