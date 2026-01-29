# 🎨 Maquettes Jem

Portail de gestion des maquettes pour la refonte de Jemanage.com

## 📁 Structure du projet

```
maquettes-jem/
├── index.html          # Page d'accueil avec tous les thèmes
├── theme.html          # Page de détail d'un thème
├── style.css           # Styles Jemanage
├── data.json           # Données (thèmes, maquettes, commentaires)
├── README.md           # Ce fichier
└── maquettes/          # Dossier pour toutes les maquettes HTML
    ├── equipe/
    ├── expertises/
    ├── objectifs/
    ├── site-web/
    ├── sondages/
    ├── formations/
    └── admin/
```

## 🚀 Démarrage rapide

### 1. Initialiser le projet sur GitHub

```bash
# Dans ton dossier local
cd maquettes-jem
git init
git add .
git commit -m "Initial commit - Portail Maquettes Jem"

# Créer le repo sur GitHub (via l'interface web)
# Puis lier ton repo local
git remote add origin https://github.com/TON-USERNAME/maquettes-jem.git
git push -u origin main
```

### 2. Activer GitHub Pages

1. Va sur ton repo GitHub
2. Clique sur **Settings** (⚙️)
3. Dans le menu à gauche, clique sur **Pages**
4. Dans "Source", sélectionne **main** (ou **master**)
5. Clique sur **Save**
6. Ton site sera disponible à : `https://TON-USERNAME.github.io/maquettes-jem/`

## ✏️ Comment ajouter une maquette ?

### Étape 1 : Ajoute ton fichier HTML

Place ton fichier HTML dans le bon dossier :

```bash
# Par exemple, pour une maquette de la page équipe
cp ma-maquette.html maquettes/equipe/dashboard-v1.html
```

### Étape 2 : Mets à jour data.json

Ouvre `data.json` et ajoute ta maquette dans le thème correspondant :

```json
{
  "themes": [
    {
      "id": "equipe",
      "nom": "Page équipe",
      "description": "Refonte de la page de gestion d'équipe",
      "maquettes": [
        {
          "id": "dashboard-v1",
          "nom": "Dashboard Manager v1",
          "fichier": "maquettes/equipe/dashboard-v1.html",
          "images": ["maquettes/equipe/screenshot-dashboard.png"],
          "date": "2026-01-29",
          "commentaires": [
            {
              "date": "2026-01-29",
              "texte": "Première version du dashboard avec KPIs et graphiques"
            },
            {
              "date": "2026-01-30",
              "texte": "À améliorer : ajouter un filtre par période"
            }
          ]
        }
      ]
    }
  ]
}
```

### Étape 3 : Ajoute des images (optionnel)

Si tu veux ajouter des captures d'écran :

```bash
# Place tes images dans le même dossier que ta maquette
cp screenshot.png maquettes/equipe/screenshot-dashboard.png
```

### Étape 4 : Push sur GitHub

```bash
git add .
git commit -m "Ajout maquette dashboard équipe v1"
git push
```

Attends 1-2 minutes et rafraîchis ton site GitHub Pages !

## 📝 Ajouter un commentaire à une maquette existante

1. Ouvre `data.json`
2. Trouve ta maquette
3. Ajoute un objet dans le tableau `commentaires` :

```json
{
  "date": "2026-01-30",
  "texte": "Amélioration des couleurs et ajout du bouton export"
}
```

4. Commit et push

## ➕ Ajouter un nouveau thème

### Étape 1 : Ajoute le thème dans data.json

```json
{
  "id": "mon-nouveau-theme",
  "nom": "Mon nouveau thème",
  "description": "Description du thème",
  "maquettes": []
}
```

### Étape 2 : Crée le dossier correspondant

```bash
mkdir maquettes/mon-nouveau-theme
```

### Étape 3 : Commit et push

```bash
git add .
git commit -m "Ajout du thème Mon nouveau thème"
git push
```

## 🎨 Les couleurs de Jemanage

Les couleurs sont définies dans `style.css` :

- **Rouge corail** : `#E72B58` (logo, boutons principaux)
- **Bleu marine** : `#0F3A4C` (header, titres)
- **Bleu** : `#2E86AB` (liens, boutons secondaires)
- **Turquoise** : `#4ECDC4` (accents, hover)
- **Gris clair** : `#F5F7FA` (fond)

## 🔧 Structure du fichier data.json

```json
{
  "themes": [
    {
      "id": "identifiant-unique",           // Utilisé dans l'URL
      "nom": "Nom affiché",                 // Titre du thème
      "description": "Description courte",   // Sous-titre
      "maquettes": [                        // Tableau des maquettes
        {
          "id": "id-maquette",
          "nom": "Nom de la maquette",
          "fichier": "maquettes/theme/fichier.html",  // Chemin vers le HTML
          "images": [                                  // Optionnel : captures d'écran
            "maquettes/theme/image1.png",
            "maquettes/theme/image2.png"
          ],
          "date": "2026-01-29",                        // Format YYYY-MM-DD
          "commentaires": [                            // Optionnel : tes notes
            {
              "date": "2026-01-29",
              "texte": "Ton commentaire ici"
            }
          ]
        }
      ]
    }
  ]
}
```

## ❓ Besoin d'aide ?

- **Le site ne se met pas à jour ?** Attends 1-2 minutes après le push, puis vide le cache de ton navigateur (Ctrl+F5)
- **Erreur JSON ?** Vérifie que tu n'as pas oublié une virgule ou une accolade dans `data.json`
- **Image qui ne s'affiche pas ?** Vérifie le chemin dans `data.json` (il doit commencer par `maquettes/`)

## 🎯 Prochaines étapes possibles

Si tu veux aller plus loin (mais pas obligatoire) :
- Ajouter une vraie fonctionnalité "Ajouter un thème" avec formulaire (nécessite backend)
- Héberger sur un vrai serveur avec base de données
- Ajouter un système de versions pour les maquettes

---

Créé avec ❤️ pour la refonte de Jemanage.com
