# Cahier de classe — obtenir le fichier .apk

Ce dossier contient tout ce qu'il faut pour que **GitHub** compile pour vous
un vrai fichier `.apk` installable sur Android, gratuitement, en quelques
minutes. Cette étape ne peut pas se faire ici (dans Claude) : la compilation
Android nécessite les outils Google (SDK/Gradle) qui ne sont pas accessibles
depuis cet environnement. GitHub, en revanche, les fournit gratuitement sur
ses machines de compilation ("GitHub Actions").

## Étapes (une fois, ~5 minutes)

1. Créez un compte gratuit sur [github.com](https://github.com) si vous n'en
   avez pas déjà un.
2. Créez un nouveau dépôt (bouton **New repository**), par exemple nommé
   `cahier-de-classe`. Laissez-le **public** ou **privé**, peu importe.
3. Sur la page du dépôt vide, cliquez sur **uploading an existing file** et
   glissez-déposez **tout le contenu de ce dossier** (en conservant la
   structure : `www/index.html`, `.github/workflows/build-apk.yml`,
   `package.json`, `capacitor.config.json`). Validez ("Commit changes").
4. Allez dans l'onglet **Actions** du dépôt. Une compilation ("Build Android
   APK") se lance automatiquement — comptez 3 à 5 minutes.
5. Une fois le cercle vert affiché, cliquez sur cette exécution, puis tout en
   bas sur **cahier-de-classe-apk** pour télécharger un fichier `.zip`.
   À l'intérieur se trouve `app-debug.apk` : c'est votre application.
6. Transférez ce `.apk` sur votre téléphone Android (par mail, Drive, câble
   USB...), ouvrez-le, et autorisez l'installation depuis une source inconnue
   si Android le demande.

## À savoir

- Il s'agit d'un APK de **debug** (non signé pour le Play Store), ce qui est
  très bien pour une installation personnelle mais ne suffit pas pour publier
  l'appli sur le Play Store — cela demanderait une étape de signature
  supplémentaire.
- Les données (élèves, notes, points...) sont stockées **dans la mémoire du
  téléphone**, à l'intérieur de l'application elle-même : tout fonctionne
  hors ligne, y compris juste après l'installation.
- Pour toute modification future de l'application, il suffira de me
  redemander la mise à jour, de remplacer `www/index.html` dans le dépôt, et
  la compilation se relancera automatiquement.
