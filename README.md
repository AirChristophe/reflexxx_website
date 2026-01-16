# Reflexxx Game - Site Web Développeur

Ce site web est conçu pour répondre aux exigences de publication sur Google Play Store et Apple App Store pour l'application Reflexxx Game.

## Structure du site

```
memory_game_website/
├── index.html          # Page d'accueil présentant l'application
├── privacy.html        # Politique de confidentialité (requis par les stores)
├── terms.html          # Conditions d'utilisation (requis par les stores)
├── support.html        # Page de support et FAQ (requis par les stores)
├── app-ads.txt         # Fichier requis par Google AdMob
├── css/
│   └── style.css       # Styles du site
├── images/
│   └── .gitkeep        # Dossier pour les images (à ajouter)
└── README.md           # Ce fichier
```

## Configuration requise

### 1. Fichier app-ads.txt

Le fichier `app-ads.txt` doit être modifié avec votre Publisher ID AdMob :

1. Connectez-vous à votre compte AdMob : https://admob.google.com
2. Allez dans **Compte > Informations du compte**
3. Copiez votre **Publisher ID** (format : `pub-XXXXXXXXXXXXXXXX`)
4. Remplacez `pub-XXXXXXXXXXXXXXXX` dans le fichier `app-ads.txt`

### 2. Images à ajouter

Ajoutez les images suivantes dans le dossier `images/` :

- `favicon.png` - Favicon du site (32x32 ou 64x64 pixels)
- `app-screenshot.png` - Capture d'écran principale pour la section hero
- `screenshot-1.png`, `screenshot-2.png`, `screenshot-3.png` - Captures d'écran de l'app
- `google-play-badge.png` - Badge Google Play Store
- `app-store-badge.png` - Badge Apple App Store

Vous pouvez télécharger les badges officiels ici :
- Google Play : https://play.google.com/intl/en_us/badges/
- App Store : https://developer.apple.com/app-store/marketing/guidelines/

### 3. Personnalisation

Modifiez les éléments suivants selon vos besoins :

- **Adresses email** : Remplacez les emails `support@memorygame.app`, `privacy@memorygame.app`, etc.
- **Liens des stores** : Ajoutez les vrais liens vers vos applications une fois publiées
- **Nom du développeur** : Vérifiez que votre nom est correct dans `support.html`

## Déploiement

### Option 1 : Firebase Hosting (Recommandé)

```bash
# Installer Firebase CLI
npm install -g firebase-tools

# Se connecter à Firebase
firebase login

# Initialiser le projet
firebase init hosting

# Déployer
firebase deploy
```

### Option 2 : GitHub Pages

1. Créez un repository GitHub
2. Poussez les fichiers
3. Activez GitHub Pages dans les paramètres

### Option 3 : Netlify / Vercel

Connectez votre repository et le déploiement sera automatique.

## Exigences des Stores

### Google Play Store

- ✅ Politique de confidentialité (`privacy.html`)
- ✅ Page de support avec informations de contact (`support.html`)
- ✅ Site web développeur pour app-ads.txt

### Apple App Store

- ✅ Politique de confidentialité (`privacy.html`)
- ✅ URL marketing (page d'accueil `index.html`)
- ✅ URL de support (`support.html`)
- ✅ Conditions d'utilisation (`terms.html`)

### Google AdMob

- ✅ Fichier `app-ads.txt` à la racine du site
- ⚠️ **Important** : Remplacez le Publisher ID avec le vôtre

## Vérification app-ads.txt

Une fois le site déployé, vérifiez que le fichier est accessible :

```
https://votredomaine.com/app-ads.txt
```

Dans AdMob :
1. Allez dans **Applications > Voir toutes les applications**
2. Cliquez sur **app-ads.txt**
3. Vérifiez le statut de votre fichier

## Contact

Pour toute question, consultez la documentation :
- [Google AdMob app-ads.txt](https://support.google.com/admob/answer/9363762)
- [Google Play Console](https://play.google.com/console)
- [App Store Connect](https://appstoreconnect.apple.com)
