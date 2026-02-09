---
layout: new-section
routeAlias: 'css-box-model'
---

<a name="css-box-model" id="css-box-model"></a>

# 📦 Module 6
## Box Model et Positionnement

### Comprendre comment les éléments prennent de la place

---

# Le Box Model CSS 📦

Chaque élément HTML est une **boîte** composée de :

1. **Content** : le contenu (texte, image)
2. **Padding** : espace intérieur (entre contenu et bordure)
3. **Border** : la bordure
4. **Margin** : espace extérieur (entre l'élément et ses voisins)

---

# Box Model en code

```css
.box {
  /* Contenu */
  width: 300px;
  height: 200px;

  /* Padding (intérieur) */
  padding: 20px;

  /* Bordure */
  border: 2px solid #333;

  /* Margin (extérieur) */
  margin: 10px;
}
```

---

# box-sizing: border-box ⭐

**Problème par défaut :** padding et border s'ajoutent à width/height.

```css
/* TOUJOURS utiliser border-box ! */
* {
  box-sizing: border-box;
}
```

**Avec `border-box` :**
- `width: 300px` = 300px TOTAL (contenu + padding + border)
- Beaucoup plus intuitif !

---

# Raccourcis padding et margin ✂️

```css
/* 4 valeurs : haut droite bas gauche */
padding: 10px 20px 10px 20px;

/* 2 valeurs : vertical horizontal */
padding: 10px 20px;

/* 1 valeur : partout */
padding: 10px;

/* Individuel */
margin-top: 10px;
margin-right: 20px;
margin-bottom: 10px;
margin-left: 20px;

/* Centrer horizontalement un bloc */
margin: 0 auto;
```

---

# Display : block, inline, inline-block 📐

```css
/* Block : prend toute la largeur */
/* div, p, h1-h6, section, article */
display: block;

/* Inline : reste sur la même ligne */
/* span, a, strong, em, img */
display: inline;

/* Inline-block : inline + width/height */
display: inline-block;

/* Caché */
display: none;
```

---

# Positionnement CSS 📍

```css
/* Static : par défaut, flux normal */
position: static;

/* Relative : décalé par rapport à sa position */
position: relative;
top: 10px;
left: 20px;

/* Absolute : par rapport au parent positionné */
position: absolute;
top: 0;
right: 0;

/* Fixed : fixé par rapport à l'écran */
position: fixed;
bottom: 0;
right: 0;

/* Sticky : collé en scrollant */
position: sticky;
top: 0;
```

---

# Exemple pratique : carte 🃏

```css
.card {
  width: 300px;
  padding: 20px;
  margin: 10px;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.card:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transform: translateY(-2px);
  transition: all 0.3s ease;
}
```

---

# En résumé 📝

- **Box Model** : content + padding + border + margin
- **box-sizing: border-box** : à utiliser TOUJOURS
- **display** : block, inline, inline-block, none
- **position** : static, relative, absolute, fixed, sticky
- `margin: 0 auto` pour centrer un bloc
