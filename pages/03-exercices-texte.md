---

# Exercices Module 3 : Texte, liens et images 🎯

---

# Exercice : Page de CV en HTML (20 min)

**Consigne :** Créez une page HTML `cv.html` contenant :
1. Un titre h1 avec votre nom
2. Une photo (ou image placeholder)
3. Une section "À propos" avec un paragraphe
4. Une liste à puces de vos compétences
5. Une liste ordonnée de vos expériences
6. Un tableau avec vos formations
7. Un lien vers votre email

---

# Exercice : Solution ✅

```html
<h1>Marie Dupont</h1>
<img src="https://picsum.photos/150/150"
     alt="Photo de Marie Dupont">

<section>
  <h2>À propos</h2>
  <p>Développeuse web passionnée
     avec <strong>3 ans</strong> d'expérience.</p>
</section>
```

---

# Exercice : Solution (suite)

```html
<section>
  <h2>Compétences</h2>
  <ul>
    <li>HTML5 &amp; CSS3</li>
    <li>JavaScript</li>
    <li>React</li>
  </ul>
</section>

<section>
  <h2>Expériences</h2>
  <ol>
    <li>Développeuse chez TechCorp (2024-2026)</li>
    <li>Stage chez WebAgency (2023)</li>
  </ol>
</section>
```

---

# Exercice : Solution (fin)

```html
<section>
  <h2>Formations</h2>
  <table>
    <thead>
      <tr>
        <th>Année</th>
        <th>Diplôme</th>
        <th>École</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>2023</td>
        <td>Licence Info</td>
        <td>Université Paris</td>
      </tr>
    </tbody>
  </table>
</section>

<footer>
  <a href="mailto:marie@example.com">
    Contactez-moi
  </a>
</footer>
```
