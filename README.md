# Reflexxx Game - Developer Website

This website is designed to meet the publication requirements for Google Play Store and Apple App Store for the Reflexxx Game application.

## Site Structure

```
reflexxx_game_website/
├── index.html          # Home page presenting the app
├── privacy.html        # Privacy policy (required by the stores)
├── terms.html          # Terms of Use (required by the stores)
├── support.html        # Support and FAQ page (required by the stores)
├── app-ads.txt         # File required by Google AdMob
├── css/
│   └── style.css       # Site styles
├── images/
│   └── .gitkeep        # Folder for images (to add)
└── README.md           # This file
```

## Required Configuration

### 1. `app-ads.txt` File

The `app-ads.txt` file must be updated with your AdMob Publisher ID:

1. Sign in to your AdMob account: https://admob.google.com
2. Go to **Account > Account information**
3. Copy your **Publisher ID** (format: `pub-XXXXXXXXXXXXXXXX`)
4. Replace `pub-XXXXXXXXXXXXXXXX` in the `app-ads.txt` file

### 2. Images to Add

Add the following images to the `images/` folder:

- `favicon.png` — Site favicon (32x32 or 64x64 pixels)
- `app-screenshot.png` — Main screenshot for the hero section
- `screenshot-1.png`, `screenshot-2.png`, `screenshot-3.png` — App screenshots
- `google-play-badge.png` — Google Play Store badge
- `app-store-badge.png` — Apple App Store badge

You can download official badges here:
- Google Play: https://play.google.com/intl/en_us/badges/
- App Store: https://developer.apple.com/app-store/marketing/guidelines/

### 3. Customization

Update the following items as needed:

- **Email addresses**: Replace `support@memorygame.app`, `privacy@memorygame.app`, etc.
- **Store links**: Add the real links to your apps once published
- **Developer name**: Verify your name is correct in `support.html`

## Deployment

### Option 1: Firebase Hosting (Recommended)

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Sign in to Firebase
firebase login

# Initialize the project
firebase init hosting

# Deploy
firebase deploy
```

### Option 2: GitHub Pages

1. Create a GitHub repository
2. Push the files
3. Enable GitHub Pages in settings

### Option 3: Netlify / Vercel

Connect your repository and deployment will be automatic.

## Store Requirements

### Google Play Store

- ✅ Privacy policy (`privacy.html`)
- ✅ Support page with contact information (`support.html`)
- ✅ Developer website for app-ads.txt

### Apple App Store

- ✅ Privacy policy (`privacy.html`)
- ✅ Marketing URL (home page `index.html`)
- ✅ Support URL (`support.html`)
- ✅ Terms of Use (`terms.html`)

### Google AdMob

- ✅ `app-ads.txt` file at the site root
- ⚠️ **Important**: Replace the Publisher ID with yours

## Verify `app-ads.txt`

Once the site is deployed, verify that the file is accessible:

```
https://yourdomain.com/app-ads.txt
```

In AdMob:
1. Go to **Apps > View all apps**
2. Click **app-ads.txt**
3. Check your file status

## Contact

For any questions, see the documentation:
- [Google AdMob app-ads.txt](https://support.google.com/admob/answer/9363762)
- [Google Play Console](https://play.google.com/console)
- [App Store Connect](https://appstoreconnect.apple.com)
