---

# Exercices Module 10 : Animations 🎯

---

# Exercice : Boutons animés (15 min)

**Consigne :** Créez 3 boutons avec des effets hover différents :
1. Bouton qui change de couleur + léger zoom
2. Bouton qui a une bordure animée
3. Bouton avec effet "glow" (ombre colorée)

---

# Exercice : Solution ✅

```css
/* Bouton 1 : couleur + zoom */
.btn-zoom {
  background: #2563eb;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
}
.btn-zoom:hover {
  background: #1d4ed8;
  transform: scale(1.05);
}
```

---

# Exercice : Solution (suite)

```css
/* Bouton 2 : bordure */
.btn-border {
  background: transparent;
  color: #2563eb;
  padding: 12px 24px;
  border: 2px solid #2563eb;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
}
.btn-border:hover {
  background: #2563eb;
  color: white;
}

/* Bouton 3 : glow */
.btn-glow {
  background: #8b5cf6;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
}
.btn-glow:hover {
  box-shadow: 0 0 20px rgba(139, 92, 246, 0.6);
  transform: translateY(-2px);
}
```
