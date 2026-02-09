---

# Exercices Module 2 : Structure HTML 🎯

---

# Exercice 1 : Créer une page HTML5 (10 min)

**Consigne :** Créez un fichier `index.html` avec :
1. Le DOCTYPE HTML5
2. La langue en français
3. L'encodage UTF-8
4. Le viewport pour mobile
5. Un titre "Mon premier site"
6. Un h1 et un paragraphe dans le body

---

# Exercice 1 : Solution ✅

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width,
                 initial-scale=1.0">
  <title>Mon premier site</title>
</head>
<body>
  <h1>Bienvenue sur mon site !</h1>
  <p>Ceci est ma première page web.</p>
</body>
</html>
```

---

# Exercice 2 : Structure sémantique (15 min)

**Consigne :** Créez la structure sémantique d'un blog avec :
- Un header avec le titre du blog
- Un nav avec 3 liens
- Un main avec un article contenant 2 sections
- Un aside avec des liens utiles
- Un footer

---

# Exercice 2 : Solution ✅

```html
<header>
  <h1>Mon Blog Tech</h1>
</header>
<nav>
  <a href="#">Accueil</a>
  <a href="#">Articles</a>
  <a href="#">Contact</a>
</nav>
<main>
  <article>
    <section>
      <h2>Introduction</h2>
      <p>Bienvenue sur mon blog.</p>
    </section>
    <section>
      <h2>Dernier article</h2>
      <p>Contenu de l'article...</p>
    </section>
  </article>
  <aside>
    <h3>Liens utiles</h3>
    <a href="#">MDN Web Docs</a>
  </aside>
</main>
<footer>
  <p>&copy; 2026 Mon Blog</p>
</footer>
```
