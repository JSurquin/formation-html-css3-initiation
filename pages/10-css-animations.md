---
layout: new-section
routeAlias: 'css-animations'
---

<a name="css-animations" id="css-animations"></a>

# ✨ Module 10
## Animations et Transitions CSS

### Donner vie à vos pages web

---

# Les transitions CSS 🔄

**Transition** = changement fluide d'une propriété CSS.

```css
.button {
  background: #2563eb;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.button:hover {
  background: #1d4ed8;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
}
```

---

# Syntaxe des transitions

```css
/* Propriété | Durée | Timing | Délai */
transition: background 0.3s ease 0s;

/* Toutes les propriétés */
transition: all 0.3s ease;

/* Plusieurs propriétés */
transition:
  background 0.3s ease,
  transform 0.2s ease,
  box-shadow 0.3s ease;
```

**Timing functions :**
- `ease` : début lent, milieu rapide, fin lente
- `linear` : vitesse constante
- `ease-in` : début lent
- `ease-out` : fin lente
- `ease-in-out` : début et fin lents

---

# Transform : déplacer, tourner, agrandir 🔄

```css
/* Déplacer */
transform: translateX(20px);
transform: translateY(-10px);
transform: translate(20px, -10px);

/* Tourner */
transform: rotate(45deg);

/* Agrandir / Réduire */
transform: scale(1.1);  /* +10% */
transform: scale(0.8);  /* -20% */

/* Incliner */
transform: skew(10deg);

/* Combiner */
transform: translateY(-5px) rotate(2deg) scale(1.05);
```

---

# Les animations CSS (@keyframes) 🎬

```css
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.element {
  animation: fadeIn 0.6s ease forwards;
}
```

---

# Keyframes avec étapes multiples

```css
@keyframes pulse {
  0%   { transform: scale(1); }
  50%  { transform: scale(1.05); }
  100% { transform: scale(1); }
}

.card {
  animation: pulse 2s ease infinite;
}
```

---

# Propriétés d'animation

```css
.element {
  animation-name: fadeIn;
  animation-duration: 0.6s;
  animation-timing-function: ease;
  animation-delay: 0.2s;
  animation-iteration-count: 1; /* ou infinite */
  animation-fill-mode: forwards;
  animation-direction: normal;

  /* Raccourci */
  animation: fadeIn 0.6s ease 0.2s 1 forwards;
}
```

---

# Animations utiles au quotidien ✨

```css
/* Spinner de chargement */
@keyframes spin {
  to { transform: rotate(360deg); }
}
.spinner {
  width: 40px; height: 40px;
  border: 4px solid #e0e0e0;
  border-top-color: #2563eb;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}
```

---

# Bonnes pratiques animations ⚡

**Performance :**
- Animer uniquement `transform` et `opacity` (GPU)
- Éviter d'animer `width`, `height`, `margin`, `top/left`
- Utiliser `will-change` avec parcimonie

**UX :**
- Durée : 200-500ms pour les interactions
- Pas d'animation excessive (mal de mer)
- Respecter `prefers-reduced-motion`

```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

# Dark Mode avec CSS 🌙

```css
/* Thème clair par défaut */
:root {
  --bg: #ffffff;
  --text: #1a1a2e;
  --card-bg: #f8fafc;
}

/* Thème sombre automatique */
@media (prefers-color-scheme: dark) {
  :root {
    --bg: #0f172a;
    --text: #e2e8f0;
    --card-bg: #1e293b;
  }
}

body {
  background: var(--bg);
  color: var(--text);
  transition: background 0.3s ease, color 0.3s ease;
}
```

---

# Dégradés CSS modernes 🌈

```css
/* Dégradé linéaire */
.hero {
  background: linear-gradient(
    135deg, #667eea 0%, #764ba2 100%
  );
}

/* Dégradé radial */
.spotlight {
  background: radial-gradient(
    circle at center, #2563eb, transparent
  );
}

/* Texte en dégradé */
.gradient-text {
  background: linear-gradient(90deg, #667eea, #764ba2);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* Bordure en dégradé */
.gradient-border {
  border: 2px solid transparent;
  background-clip: padding-box;
  border-image: linear-gradient(135deg, #667eea, #764ba2) 1;
}
```

---

# Glassmorphism (tendance 2025) 🪟

```css
.glass-card {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 16px;
  padding: 24px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}
```

Un effet de verre dépoli très tendance pour les cartes et modales.

---

# En résumé 📝

- **Transitions** : changement fluide au hover/focus
- **Transform** : translate, rotate, scale, skew
- **@keyframes** : animations personnalisées
- Animer `transform` et `opacity` pour la performance
- Respecter `prefers-reduced-motion` pour l'accessibilité
- **Dark mode** : `prefers-color-scheme` + variables CSS
- **Dégradés** : linear-gradient, radial-gradient
- **Glassmorphism** : backdrop-filter blur
