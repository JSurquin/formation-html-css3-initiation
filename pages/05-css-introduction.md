---
layout: new-section
routeAlias: 'css-introduction'
---

<a name="css-introduction" id="css-introduction"></a>

# 🎨 Module 5
## Introduction au CSS

### Donner du style à vos pages web

---

# Qu'est-ce que le CSS ? 🎨

**CSS** = Cascading Style Sheets (Feuilles de style en cascade)

**Rôle :** Définir l'apparence visuelle d'une page web.

**3 façons d'ajouter du CSS :**
1. **Inline** : dans l'attribut `style` (à éviter)
2. **Interne** : dans une balise `<style>` dans le head
3. **Externe** : dans un fichier `.css` séparé (recommandé !)

---

# CSS externe (recommandé) 📁

```html
<!-- Dans le <head> du HTML -->
<link rel="stylesheet" href="style.css">
```

```css
/* style.css */
h1 {
  color: blue;
  font-size: 32px;
}

p {
  color: #333;
  line-height: 1.6;
}
```

---

# Syntaxe CSS 📐

```css
sélecteur {
  propriété: valeur;
  propriété: valeur;
}
```

**Exemple :**

```css
h1 {
  color: #2563eb;      /* Couleur du texte */
  font-size: 2rem;     /* Taille de police */
  text-align: center;  /* Alignement */
  margin-bottom: 20px; /* Marge en bas */
}
```

---

# Les sélecteurs de base 🎯

```css
/* Sélecteur d'élément */
p { color: black; }

/* Sélecteur de classe (.) */
.important { color: red; font-weight: bold; }

/* Sélecteur d'ID (#) */
#header { background-color: navy; }

/* Sélecteur universel */
* { margin: 0; padding: 0; }

/* Sélecteur de groupe */
h1, h2, h3 { font-family: 'Arial', sans-serif; }
```

---

# Sélecteurs avancés 🔍

```css
/* Descendant (espace) */
nav a { text-decoration: none; }

/* Enfant direct (>) */
ul > li { list-style: square; }

/* Adjacent (+) */
h2 + p { font-size: 1.1rem; }

/* Attribut */
input[type="email"] { border-color: blue; }

/* Pseudo-classes */
a:hover { color: red; }
button:focus { outline: 2px solid blue; }
li:first-child { font-weight: bold; }
```

---

# Les couleurs en CSS 🌈

```css
/* Par nom */
color: red;
color: navy;

/* Hexadécimal */
color: #ff0000;     /* Rouge */
color: #2563eb;     /* Bleu */
color: #333;        /* Gris foncé (raccourci) */

/* RGB */
color: rgb(37, 99, 235);

/* RGBA (avec transparence) */
color: rgba(0, 0, 0, 0.5);  /* Noir 50% */

/* HSL */
color: hsl(220, 83%, 53%);
```

---

# Les unités CSS 📏

| Unité | Type | Description |
|-------|------|-------------|
| `px` | Absolue | Pixels (le plus courant) |
| `rem` | Relative | Par rapport à la taille de base (16px) |
| `em` | Relative | Par rapport au parent |
| `%` | Relative | Pourcentage du parent |
| `vw` | Viewport | 1% de la largeur de l'écran |
| `vh` | Viewport | 1% de la hauteur de l'écran |

**Recommandation :** Utilisez `rem` pour les tailles de texte et `px` ou `%` pour les layouts.

---

# Typographie web 🔤

```css
body {
  /* Police avec fallback */
  font-family: 'Inter', 'Arial', sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}

h1 {
  font-size: 2.5rem;
  font-weight: 700;
  letter-spacing: -0.02em;
}

.citation {
  font-style: italic;
  text-transform: uppercase;
  text-decoration: underline;
}
```

---

# Google Fonts 🅰️

```html
<!-- Dans le <head> -->
<link rel="preconnect"
      href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap"
      rel="stylesheet">
```

```css
body {
  font-family: 'Inter', sans-serif;
}
```

---

# Les variables CSS (Custom Properties) 🎨

```css
/* Déclaration dans :root (global) */
:root {
  --primary: #2563eb;
  --secondary: #7c3aed;
  --dark: #1a1a2e;
  --light: #f8fafc;
  --text: #334155;
  --radius: 12px;
  --shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

/* Utilisation avec var() */
.button {
  background: var(--primary);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
}

h1 { color: var(--primary); }
```

**Avantage :** Changer 1 variable = changer tout le thème !

---

# Pseudo-éléments et pseudo-classes 🎭

```css
/* Pseudo-classes : état de l'élément */
a:hover { color: red; }
a:active { color: darkred; }
input:focus { border-color: blue; }
li:first-child { font-weight: bold; }
li:nth-child(even) { background: #f0f0f0; }
button:disabled { opacity: 0.5; }

/* Pseudo-éléments : parties virtuelles */
p::first-line { font-weight: bold; }
p::first-letter { font-size: 2rem; }
.required::after {
  content: " *";
  color: red;
}
```

---

# La spécificité CSS 🏋️

**Quand 2 règles s'appliquent au même élément, laquelle gagne ?**

| Sélecteur | Spécificité | Exemple |
|-----------|-------------|---------|
| `!important` | 10000 | À éviter ! |
| Style inline | 1000 | `style="..."` |
| ID `#` | 100 | `#header` |
| Classe `.` | 10 | `.card` |
| Élément | 1 | `p`, `h1` |

```css
/* Spécificité 1 */
p { color: black; }

/* Spécificité 10 → gagne */
.intro { color: blue; }

/* Spécificité 100 → gagne */
#hero { color: red; }
```

---

# En résumé 📝

- CSS = **style** et **mise en forme** du HTML
- Fichier `.css` externe (recommandé)
- Syntaxe : `sélecteur { propriété: valeur; }`
- Sélecteurs : élément, `.classe`, `#id`
- Couleurs : noms, hex, rgb, hsl
- Unités : px, rem, em, %, vw, vh
- **Variables CSS** : `--name` et `var(--name)`
- **Spécificité** : ID > classe > élément
- Google Fonts pour les polices personnalisées
