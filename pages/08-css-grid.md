---
layout: new-section
routeAlias: 'css-grid'
---

<a name="css-grid" id="css-grid"></a>

# 🔲 Module 8
## CSS Grid

### Le système de grille bidimensionnel

---

# Flexbox vs Grid 🤔

| Flexbox | Grid |
|---------|------|
| 1 dimension (ligne OU colonne) | 2 dimensions (lignes ET colonnes) |
| Idéal pour les composants | Idéal pour les layouts de page |
| Contenu qui détermine le layout | Layout qui détermine le contenu |

**En pratique :** on utilise les deux ensemble !

---

# Activer CSS Grid

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  /* 3 colonnes égales */
  gap: 20px;
}
```

**L'unité `fr`** = fraction de l'espace disponible.

---

# grid-template-columns et rows 📐

```css
.grid {
  display: grid;

  /* 3 colonnes : 200px, flexible, 200px */
  grid-template-columns: 200px 1fr 200px;

  /* Raccourci : 4 colonnes égales */
  grid-template-columns: repeat(4, 1fr);

  /* Colonnes auto-responsive */
  grid-template-columns:
    repeat(auto-fit, minmax(250px, 1fr));

  /* Lignes */
  grid-template-rows: auto 1fr auto;

  gap: 20px;
}
```

---

# grid-area : nommer les zones 🏷️

```css
.layout {
  display: grid;
  grid-template-areas:
    "header header header"
    "sidebar main aside"
    "footer footer footer";
  grid-template-columns: 200px 1fr 200px;
  grid-template-rows: auto 1fr auto;
  min-height: 100vh;
}

.header  { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main    { grid-area: main; }
.aside   { grid-area: aside; }
.footer  { grid-area: footer; }
```

---

# Placement des éléments 📍

```css
.item {
  /* Ligne de début / ligne de fin */
  grid-column: 1 / 3;  /* 2 colonnes */
  grid-row: 1 / 2;     /* 1 ligne */

  /* Raccourci : span */
  grid-column: span 2; /* S'étend sur 2 colonnes */
  grid-row: span 3;    /* S'étend sur 3 lignes */
}
```

---

# Alignement dans Grid 🎯

```css
.container {
  /* Aligner tous les items */
  justify-items: center;  /* Horizontal */
  align-items: center;    /* Vertical */

  /* Aligner la grille dans le conteneur */
  justify-content: center;
  align-content: center;
}

.item {
  /* Alignement individuel */
  justify-self: end;
  align-self: start;
}
```

---

# Grille auto-responsive magique ✨

```css
/* Le pattern le plus utile ! */
.cards-grid {
  display: grid;
  grid-template-columns:
    repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  padding: 20px;
}
```

**Ce que ça fait :**
- Colonnes de minimum 280px
- S'adapte automatiquement au nombre de colonnes
- Pas besoin de media queries !

---

# En résumé 📝

- **CSS Grid** : layout 2D (lignes + colonnes)
- `display: grid` + `grid-template-columns`
- **fr** : unité fractionnaire
- **grid-template-areas** : nommer les zones
- **repeat(auto-fit, minmax())** : grille auto-responsive
- **Flexbox + Grid** = combo parfait
