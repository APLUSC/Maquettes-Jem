# 🚀 Guide de démarrage rapide - Maquettes Jem

## Étape 1 : Mettre en ligne sur GitHub (5 minutes)

### A. Créer un repo sur GitHub
1. Va sur https://github.com/new
2. Nom du repo : `maquettes-jem`
3. Sélectionne **Public**
4. Ne coche **RIEN** (pas de README, pas de .gitignore)
5. Clique sur **Create repository**

### B. Lier ton dossier local
Ouvre ton terminal et exécute :

```bash
cd [chemin-vers-ton-dossier]/maquettes-jem
git init
git add .
git commit -m "Initial commit - Portail Maquettes Jem"
git branch -M main
git remote add origin https://github.com/TON-USERNAME/maquettes-jem.git
git push -u origin main
```

### C. Activer GitHub Pages
1. Va sur ton repo : `https://github.com/TON-USERNAME/maquettes-jem`
2. Clique sur **Settings** (⚙️)
3. Dans le menu de gauche, clique sur **Pages**
4. Sous "Source", sélectionne **main**
5. Clique sur **Save**
6. Attends 1-2 minutes

✅ Ton site sera disponible à : `https://TON-USERNAME.github.io/maquettes-jem/`

---

## Étape 2 : Ajouter ta première vraie maquette

### A. Prépare ton fichier HTML
Place ton fichier HTML dans le bon dossier :
```bash
cp ma-maquette.html maquettes/equipe/ma-maquette-v1.html
```

### B. Modifie data.json
Ouvre `data.json` avec ton éditeur de texte et ajoute ta maquette :

```json
{
  "id": "equipe",
  "nom": "Page équipe",
  "description": "Refonte de la page de gestion d'équipe",
  "maquettes": [
    {
      "id": "ma-maquette-v1",
      "nom": "Ma première maquette",
      "fichier": "maquettes/equipe/ma-maquette-v1.html",
      "images": [],
      "date": "2026-01-29",
      "commentaires": [
        {
          "date": "2026-01-29",
          "texte": "Première version de la maquette"
        }
      ]
    }
  ]
}
```

### C. Envoie sur GitHub
```bash
git add .
git commit -m "Ajout de ma première maquette"
git push
```

Attends 30 secondes et rafraîchis ton site !

---

## Étape 3 : Ajouter un commentaire (plus tard)

1. Ouvre `data.json`
2. Trouve ta maquette
3. Ajoute un commentaire dans le tableau `commentaires` :

```json
{
  "date": "2026-01-30",
  "texte": "J'ai ajouté les boutons d'action en bas de page"
}
```

4. Commit et push :
```bash
git add data.json
git commit -m "Ajout commentaire sur maquette"
git push
```

---

## 💡 Astuces

### Pour supprimer l'exemple
Tu peux supprimer la maquette d'exemple en :
1. Supprimant le fichier `maquettes/equipe/exemple-dashboard.html`
2. Retirant l'entrée correspondante dans `data.json`

### Dates dans data.json
Utilise toujours le format `YYYY-MM-DD` (ex: `2026-01-29`)

### Vérifier que JSON est valide
Va sur https://jsonlint.com/ et colle ton JSON pour vérifier qu'il n'y a pas d'erreurs

---

## ❓ Problèmes fréquents

**Le site ne se met pas à jour ?**
→ Attends 1-2 minutes puis vide le cache : `Ctrl+F5` (Windows) ou `Cmd+Shift+R` (Mac)

**Erreur "404 Not Found" ?**
→ Vérifie que GitHub Pages est activé et que tu vas bien sur `TON-USERNAME.github.io/maquettes-jem/`

**Les maquettes ne s'affichent pas ?**
→ Vérifie le chemin dans `data.json` (il doit commencer par `maquettes/`)

**Erreur JSON ?**
→ Vérifie les virgules et accolades dans `data.json` avec https://jsonlint.com/

---

## 📞 Besoin d'aide ?

Si tu es bloqué, envoie-moi le message d'erreur et je t'aide ! 🚀
