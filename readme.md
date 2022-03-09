
### page HTML/CSS
#### présentant 3 cards
Un peu de Tailwind pour me faire la main

![screenshot](screenshot.jpg)

### *Notes pour installer Tailwind :*

#### - Commandes d'installation
**Run** : `npm init -y `<br>
**Run** : `npm install -D tailwindcss postcss-cli autoprefixer`<br>
**Run** : `npx tailwindcss init -p`

#### - Installer éventuellement *Tailwind CSS IntelliSense* pour les suggestions de class

#### - Ajouter @tilwind rule pour éviter à VScode de bugger dans certains cas
https://stackoverflow.com/questions/47607602/how-to-add-a-tailwind-css-rule-to-css-checker

#### - Créer dossier et fichiers
public/index.html<br>
src/tailwind.css

#### - Dans tailwind.css, ajouter
```
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
}

@layer components {
}
```

#### - Build
**Ajouter** dans le package.json : script => ``"build": "postcss -w src/tailwind.css -o public/style.css"``<br>
**Run** : ``npm run build``

#### - Purge
**Ajouter** dans tailwind.config.js : purge => `./public/index.html`<br>
**Run** : `$env:NODE_ENV="production"`<br>
**Run** : `npm run build`
