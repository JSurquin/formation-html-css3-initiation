---
layout: new-section
routeAlias: 'html-structure'
---

<a name="html-structure" id="html-structure"></a>

# 🏗️ Module 2
## Structure HTML

### Anatomie d'un document HTML5

---

# Qu'est-ce qu'une balise HTML ? 🏷️

Une **balise** (tag) est un élément de base du HTML.

**Balise ouvrante + contenu + balise fermante :**

```html
<p>Ceci est un paragraphe</p>
```

**Balises auto-fermantes (pas de contenu) :**

```html
<br>
<img src="photo.jpg" alt="Ma photo">
<input type="text">
```

---

# Les attributs HTML 📋

Les **attributs** ajoutent des informations aux balises :

```html
<a href="https://google.com" target="_blank">
  Cliquez ici
</a>

<img src="photo.jpg" alt="Description"
     width="300" height="200">

<input type="email" placeholder="Votre email"
       required>
```

**Attributs globaux (sur toutes les balises) :**
- `id` : identifiant unique
- `class` : classe CSS
- `style` : style inline
- `title` : info-bulle

---

# Structure d'un document HTML5 📄

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width,
                 initial-scale=1.0">
  <title>Ma première page</title>
</head>
<body>
  <h1>Bonjour le monde !</h1>
  <p>Ma première page web.</p>
</body>
</html>
```

---

# Explication de chaque partie 🔍

- `<!DOCTYPE html>` : déclare que c'est du HTML5
- `<html lang="fr">` : racine du document, langue française
- `<head>` : métadonnées (pas visible à l'écran)
  - `charset="UTF-8"` : encodage des caractères (accents)
  - `viewport` : adapte l'affichage mobile
  - `<title>` : titre dans l'onglet du navigateur
- `<body>` : contenu visible de la page

---

# HTML5 sémantique 🧩

**Le HTML sémantique** donne du sens au contenu :

```html
<header>En-tête du site</header>
<nav>Navigation principale</nav>
<main>
  <article>
    <section>
      <h2>Titre de section</h2>
      <p>Contenu...</p>
    </section>
  </article>
  <aside>Barre latérale</aside>
</main>
<footer>Pied de page</footer>
```

---

# Pourquoi le sémantique ? 🤔

**Avantages du HTML sémantique :**
- **Accessibilité** : les lecteurs d'écran comprennent la structure
- **SEO** : Google comprend mieux le contenu
- **Maintenabilité** : code plus lisible pour les développeurs
- **Standards** : respect des bonnes pratiques W3C

**À éviter :**

```html
<!-- ❌ Non sémantique -->
<div class="header">...</div>
<div class="nav">...</div>

<!-- ✅ Sémantique -->
<header>...</header>
<nav>...</nav>
```

---

# Les commentaires HTML 💬

```html
<!-- Ceci est un commentaire HTML -->
<!-- Il n'est pas visible à l'écran -->

<!-- TODO: ajouter le menu -->
<nav>
  <!-- Menu principal -->
</nav>
```

**Raccourci VSCode :** `Ctrl + /` (ou `Cmd + /` sur Mac)

---

# Accessibilité (a11y) ♿

**Pourquoi c'est important :**
- 15% de la population mondiale a un handicap
- Obligation légale (RGAA en France)
- Améliore le SEO et l'UX pour tous

**Bonnes pratiques de base :**
- Toujours mettre un attribut `alt` sur les images
- Utiliser les balises sémantiques (pas des `div` partout)
- Assurer un contraste suffisant (ratio 4.5:1 minimum)
- Les formulaires doivent avoir des `<label>`
- Le site doit être navigable au clavier

---

# Balises meta pour le SEO 🔍

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width, initial-scale=1.0">
  <title>Mon Site - Mot clé principal</title>
  <meta name="description"
        content="Description de 150-160 caractères
                 pour Google">
  <meta name="author" content="Votre nom">

  <!-- Open Graph (réseaux sociaux) -->
  <meta property="og:title" content="Mon Site">
  <meta property="og:description"
        content="Description pour le partage">
  <meta property="og:image"
        content="https://monsite.com/preview.jpg">

  <!-- Favicon -->
  <link rel="icon" href="favicon.ico">
</head>
```

---

# En résumé 📝

- Les **balises** structurent le contenu
- Les **attributs** ajoutent des informations
- Le **DOCTYPE** déclare le HTML5
- Le **head** contient les métadonnées
- Le **body** contient le contenu visible
- Le **HTML sémantique** donne du sens (header, nav, main, footer)
- **Accessibilité** : alt, labels, contraste, navigation clavier
- **SEO** : title, meta description, Open Graph
