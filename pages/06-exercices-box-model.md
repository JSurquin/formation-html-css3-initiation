---

# Exercices Module 6 : Box Model 🎯

---

# Exercice : Créer des cartes produit (20 min)

**Consigne :** Créez 3 cartes produit côte à côte avec :
- Largeur fixe de 300px
- Padding de 20px
- Bordure arrondie (border-radius: 12px)
- Ombre portée (box-shadow)
- Effet hover (ombre plus forte + léger décalage)
- Image, titre, description et prix

---

# Exercice : Solution HTML

```html
<div class="cards">
  <div class="card">
    <img src="https://picsum.photos/300/200"
         alt="Produit 1">
    <h3>Produit 1</h3>
    <p>Description du produit 1</p>
    <span class="price">29.99€</span>
  </div>
  <div class="card">
    <img src="https://picsum.photos/300/201"
         alt="Produit 2">
    <h3>Produit 2</h3>
    <p>Description du produit 2</p>
    <span class="price">49.99€</span>
  </div>
</div>
```

---

# Exercice : Solution CSS (structure)

```css
* { box-sizing: border-box; }

.cards {
  display: flex;
  gap: 20px;
  padding: 20px;
}

.card {
  width: 300px;
  padding: 20px;
  border-radius: 12px;
  background: white;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
}
```

---

# Exercice : Solution CSS (hover & details)

```css
.card:hover {
  box-shadow: 0 8px 24px rgba(0,0,0,0.15);
  transform: translateY(-4px);
}

.card img {
  width: 100%;
  border-radius: 8px;
}

.price {
  color: #2563eb;
  font-weight: bold;
  font-size: 1.2rem;
}
```
