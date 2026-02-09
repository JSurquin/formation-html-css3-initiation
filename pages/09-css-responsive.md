---
layout: new-section
routeAlias: 'css-responsive'
---

<a name="css-responsive" id="css-responsive"></a>

# 📱 Module 9
## Responsive Design

### Adapter votre site à tous les écrans

---

# Pourquoi le responsive ? 📱

**En 2026 :**
- 60% du trafic web est mobile
- Google privilégie les sites mobile-friendly (SEO)
- Des milliers de tailles d'écran différentes

**Responsive Design =** un seul site qui s'adapte à tous les écrans.

---

# Le viewport meta tag 📐

```html
<!-- INDISPENSABLE dans le <head> -->
<meta name="viewport"
      content="width=device-width, initial-scale=1.0">
```

Sans ce tag, le mobile affiche la page en version desktop réduite.

---

# Mobile First 📱→🖥️

**Approche recommandée : coder d'abord pour mobile, puis agrandir.**

```css
/* Style de base = mobile */
.container {
  padding: 10px;
}

/* Tablette (768px et +) */
@media (min-width: 768px) {
  .container {
    padding: 20px;
  }
}

/* Desktop (1024px et +) */
@media (min-width: 1024px) {
  .container {
    padding: 40px;
    max-width: 1200px;
    margin: 0 auto;
  }
}
```

---

# Media Queries : les breakpoints 📏

```css
/* Mobile : 0 - 767px (styles par défaut) */

/* Tablette */
@media (min-width: 768px) { ... }

/* Desktop */
@media (min-width: 1024px) { ... }

/* Grand écran */
@media (min-width: 1440px) { ... }

/* Orientation */
@media (orientation: landscape) { ... }

/* Impression */
@media print { ... }
```

---

# Exemple pratique : grille responsive

```css
.grid {
  display: grid;
  gap: 20px;
  padding: 20px;

  /* Mobile : 1 colonne */
  grid-template-columns: 1fr;
}

@media (min-width: 768px) {
  .grid {
    /* Tablette : 2 colonnes */
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .grid {
    /* Desktop : 3 colonnes */
    grid-template-columns: repeat(3, 1fr);
  }
}
```

---

# Images responsive 🖼️

```css
/* Image fluide (toujours) */
img {
  max-width: 100%;
  height: auto;
}
```

```html
<!-- Image responsive HTML -->
<picture>
  <source media="(min-width: 1024px)"
          srcset="hero-large.jpg">
  <source media="(min-width: 768px)"
          srcset="hero-medium.jpg">
  <img src="hero-small.jpg" alt="Hero image">
</picture>
```

---

# Unités relatives pour le responsive 📏

```css
/* rem : relatif à la taille de base (16px) */
font-size: 1.5rem;   /* = 24px */

/* vw/vh : relatif au viewport */
width: 100vw;         /* Largeur de l'écran */
height: 50vh;         /* 50% de la hauteur */

/* clamp() : valeur responsive avec min/max */
font-size: clamp(1rem, 2.5vw, 2rem);
/* min: 1rem, idéal: 2.5vw, max: 2rem */

padding: clamp(10px, 3vw, 40px);
```

---

# Navbar responsive complète 📱→🖥️

```css
/* Mobile : menu hamburger (masqué par défaut) */
.nav-links {
  display: none;
  flex-direction: column;
  background: var(--dark);
  position: absolute;
  top: 60px;
  left: 0;
  right: 0;
}

.nav-links.active {
  display: flex;
}

/* Desktop : menu horizontal */
@media (min-width: 768px) {
  .nav-links {
    display: flex;
    flex-direction: row;
    position: static;
    background: transparent;
  }
  .hamburger { display: none; }
}
```

---

# Container queries (CSS moderne 2025+) 📐

```css
/* Au lieu de se baser sur la taille de l'écran,
   on se base sur la taille du CONTENEUR */

.card-container {
  container-type: inline-size;
  container-name: card;
}

@container card (min-width: 400px) {
  .card {
    display: flex;
    flex-direction: row;
  }
}

@container card (max-width: 399px) {
  .card {
    display: flex;
    flex-direction: column;
  }
}
```

**L'avenir du responsive !** Supporté par tous les navigateurs modernes.

---

# En résumé 📝

- **Viewport meta tag** : indispensable
- **Mobile First** : styles mobile par défaut, media queries pour agrandir
- **Breakpoints** : 768px (tablette), 1024px (desktop)
- **Images fluides** : `max-width: 100%`
- **clamp()** : tailles responsive sans media queries
- **`repeat(auto-fit, minmax())`** : grille auto-responsive
- **Container queries** : responsive basé sur le conteneur
