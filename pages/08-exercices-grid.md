---

# Exercices Module 8 : CSS Grid 🎯

---

# Exercice : Layout de page complète (20 min)

**Consigne :** Créez un layout de page avec Grid :
- Header sur toute la largeur
- Sidebar à gauche (250px)
- Contenu principal au centre
- Aside à droite (200px)
- Footer sur toute la largeur
- Utilisez `grid-template-areas`

---

# Exercice : Solution ✅

```css
.page {
  display: grid;
  grid-template-areas:
    "header  header  header"
    "sidebar main    aside"
    "footer  footer  footer";
  grid-template-columns: 250px 1fr 200px;
  grid-template-rows: 60px 1fr 50px;
  min-height: 100vh;
  gap: 0;
}

.header  { grid-area: header;
            background: #1a1a2e; color: white; }
.sidebar { grid-area: sidebar;
            background: #f0f0f0; padding: 20px; }
.main    { grid-area: main;
            padding: 20px; }
.aside   { grid-area: aside;
            background: #f8f8f8; padding: 20px; }
.footer  { grid-area: footer;
            background: #1a1a2e; color: white; }
```
