# Google Drive Sync Setup Guide

To use the Google Drive Sync feature, you must configure Google Cloud Platform credentials. Since this app runs completely locally in your browser (via GitHub Pages), it requires a Client ID to communicate with Google's servers securely.

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new Project (e.g., "Trading Journal App").
3. Go to **APIs & Services** -> **Library** and search for "Google Drive API". Click **Enable**.
4. Go to **OAuth consent screen**.
   - Choose **External** and fill in the required App name and email fields.
   - Click Save and Continue. You do not need to add scopes here.
   - Publish the App (Set status to "In production").
5. Go to **Credentials**.
   - Click **Create Credentials** -> **OAuth client ID**.
   - Application type: **Web application**.
   - Under **Authorized JavaScript origins**, add your GitHub Pages URL (e.g., `https://yourusername.github.io`).
   - Click Create. Copy your **Client ID**.
   - Click **Create Credentials** -> **API Key**. Copy this key.
6. Open `index.html` in your code editor.
7. Find the `<script>` section near the bottom. Replace the placeholder values:
   ```javascript
   const CLIENT_ID = 'YOUR_GOOGLE_CLIENT_ID';
   const API_KEY = 'YOUR_GOOGLE_API_KEY';
   ```
8. Commit and push the updated code to GitHub Pages. The Drive Sync will now work!
