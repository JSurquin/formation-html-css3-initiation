---

# Exercices Module 5 : Introduction CSS 🎯

---

# Exercice : Styliser le CV HTML (20 min)

**Consigne :** Reprenez votre CV HTML et créez un fichier `style.css` :
1. Police Inter via Google Fonts
2. Couleur de fond : `#f5f5f5`
3. Titre h1 en bleu (`#2563eb`), centré
4. Paragraphes en gris foncé (`#333`), line-height 1.6
5. Liens en bleu qui deviennent rouge au survol
6. Tableau avec bordures et alternance de couleur

---

# Exercice : Solution ✅

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', sans-serif;
  background-color: #f5f5f5;
  color: #333;
  line-height: 1.6;
  padding: 20px;
}

h1 {
  color: #2563eb;
  text-align: center;
  margin-bottom: 20px;
}
```

---

# Exercice : Solution (suite)

```css
a {
  color: #2563eb;
  text-decoration: none;
}

a:hover {
  color: red;
  text-decoration: underline;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
}

th, td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

tr:nth-child(even) {
  background-color: #e8e8e8;
}
```
