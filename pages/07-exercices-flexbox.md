---

# Exercices Module 7 : Flexbox 🎯

---

# Exercice : Layout complet avec Flexbox (25 min)

**Consigne :** Créez une page avec :
1. Une navbar (logo à gauche, liens à droite)
2. Une hero section centrée (titre + sous-titre + bouton)
3. 3 cartes de features côte à côte
4. Un footer avec 3 colonnes

---

# Exercice : Solution CSS (navbar)

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  background: #1a1a2e;
  color: white;
}

.navbar .links {
  display: flex;
  gap: 20px;
}
```

---

# Exercice : Solution CSS (hero)

```css
.hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 60vh;
  text-align: center;
  background: linear-gradient(135deg,
    #667eea 0%, #764ba2 100%);
  color: white;
}

.hero h1 { font-size: 3rem; }
.hero p { font-size: 1.2rem; opacity: 0.9; }
```

---

# Exercice : Solution CSS (features + footer)

```css
.features {
  display: flex;
  gap: 20px;
  padding: 40px;
  justify-content: center;
  flex-wrap: wrap;
}

.feature-card {
  flex: 1;
  min-width: 250px;
  max-width: 350px;
  padding: 30px;
  text-align: center;
  border-radius: 12px;
  background: white;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.footer {
  display: flex;
  justify-content: space-around;
  padding: 40px;
  background: #1a1a2e;
  color: #ccc;
}
```
