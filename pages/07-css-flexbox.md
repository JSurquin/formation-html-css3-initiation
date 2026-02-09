---
layout: new-section
routeAlias: 'css-flexbox'
---

<a name="css-flexbox" id="css-flexbox"></a>

# 💪 Module 7
## Flexbox

### Le système de mise en page flexible

---

# Qu'est-ce que Flexbox ? 🤸

**Flexbox** = un mode de layout CSS pour organiser les éléments en ligne ou en colonne.

**Activer Flexbox :**

```css
.container {
  display: flex;
}
```

Tous les enfants directs deviennent des **flex items**.

---

# Les axes de Flexbox 📐

**Axe principal (main axis) :** horizontal par défaut
**Axe transversal (cross axis) :** vertical par défaut

```css
/* Direction des éléments */
flex-direction: row;            /* → (défaut) */
flex-direction: row-reverse;    /* ← */
flex-direction: column;         /* ↓ */
flex-direction: column-reverse; /* ↑ */
```

---

# justify-content : axe principal ↔️

```css
.container {
  display: flex;
  justify-content: flex-start;    /* Début */
  justify-content: flex-end;      /* Fin */
  justify-content: center;        /* Centre */
  justify-content: space-between; /* Espacé */
  justify-content: space-around;  /* Espacement égal */
  justify-content: space-evenly;  /* Espacement uniforme */
}
```

---

# align-items : axe transversal ↕️

```css
.container {
  display: flex;
  align-items: stretch;    /* Étiré (défaut) */
  align-items: flex-start; /* En haut */
  align-items: flex-end;   /* En bas */
  align-items: center;     /* Centré */
  align-items: baseline;   /* Ligne de base du texte */
}
```

---

# Centrer parfaitement un élément 🎯

```css
/* Le Saint Graal du centrage CSS */
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```

C'est tout ! Fini les hacks de centrage vertical.

---

# flex-wrap : passer à la ligne 🔄

```css
.container {
  display: flex;
  flex-wrap: nowrap; /* Sur 1 ligne (défaut) */
  flex-wrap: wrap;   /* Passe à la ligne */
}
```

---

# gap : espacement entre les éléments

```css
.container {
  display: flex;
  gap: 20px;       /* Espacement uniforme */
  row-gap: 10px;   /* Espacement vertical */
  column-gap: 20px; /* Espacement horizontal */
}
```

`gap` remplace les marges compliquées !

---

# Propriétés des flex items 📦

```css
.item {
  /* Croître pour remplir l'espace */
  flex-grow: 1;

  /* Rétrécir si nécessaire */
  flex-shrink: 0;

  /* Taille de base */
  flex-basis: 200px;

  /* Raccourci : grow shrink basis */
  flex: 1 0 200px;

  /* Réordonner sans changer le HTML */
  order: 2;

  /* Alignement individuel */
  align-self: center;
}
```

---

# Exemple : Navigation responsive

```css
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  background: #1a1a2e;
}

nav .logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: white;
}

nav .links {
  display: flex;
  gap: 20px;
}

nav a {
  color: #e0e0e0;
  text-decoration: none;
}

nav a:hover {
  color: white;
}
```

---

# En résumé 📝

- `display: flex` sur le conteneur
- **justify-content** : axe principal (horizontal)
- **align-items** : axe transversal (vertical)
- **flex-wrap: wrap** : passer à la ligne
- **gap** : espacement entre éléments
- **flex: 1** : les items se partagent l'espace
- Centrer = `justify-content: center` + `align-items: center`
