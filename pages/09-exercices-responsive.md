---

# Exercices Module 9 : Responsive Design 🎯

---

# Exercice : Rendre votre layout responsive (20 min)

**Consigne :** Reprenez le layout Grid du module 8 et rendez-le responsive :
- **Mobile** : tout empilé sur 1 colonne
- **Tablette** : sidebar + main (pas d'aside)
- **Desktop** : layout 3 colonnes complet

---

# Exercice : Solution ✅

```css
.page {
  display: grid;
  min-height: 100vh;
  /* Mobile : 1 colonne */
  grid-template-areas:
    "header"
    "main"
    "footer";
  grid-template-columns: 1fr;
  grid-template-rows: 60px 1fr 50px;
}

.sidebar, .aside { display: none; }
```

---

# Exercice : Solution (suite)

```css
@media (min-width: 768px) {
  .page {
    grid-template-areas:
      "header  header"
      "sidebar main"
      "footer  footer";
    grid-template-columns: 250px 1fr;
  }
  .sidebar { display: block; }
}

@media (min-width: 1024px) {
  .page {
    grid-template-areas:
      "header  header  header"
      "sidebar main    aside"
      "footer  footer  footer";
    grid-template-columns: 250px 1fr 200px;
  }
  .aside { display: block; }
}
```
