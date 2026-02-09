---
layout: new-section
routeAlias: 'html-texte-liens'
---

<a name="html-texte-liens" id="html-texte-liens"></a>

# 📝 Module 3
## Texte, liens et images

### Les éléments de contenu HTML

---

# Les titres (headings) 📰

HTML propose 6 niveaux de titres :

```html
<h1>Titre principal (1 seul par page)</h1>
<h2>Sous-titre</h2>
<h3>Sous-sous-titre</h3>
<h4>Titre niveau 4</h4>
<h5>Titre niveau 5</h5>
<h6>Titre niveau 6</h6>
```

**Règle importante :** Ne pas sauter de niveaux !
- ✅ h1 → h2 → h3
- ❌ h1 → h3 (pas de h2)

---

# Paragraphes et mise en forme 📄

```html
<p>Ceci est un paragraphe normal.</p>

<p>Texte avec du <strong>gras important</strong>
   et de l'<em>italique pour l'emphase</em>.</p>

<p>Un saut de ligne<br>au milieu du texte.</p>

<hr> <!-- Ligne horizontale de séparation -->

<blockquote>
  "Le Web est plus une invention sociale
   que technologique." - Tim Berners-Lee
</blockquote>
```

---

# Les listes 📋

**Liste non ordonnée (puces) :**

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

**Liste ordonnée (numérotée) :**

```html
<ol>
  <li>Apprendre HTML</li>
  <li>Apprendre CSS</li>
  <li>Créer un site</li>
</ol>
```

---

# Les liens hypertextes 🔗

```html
<!-- Lien externe -->
<a href="https://google.com">Google</a>

<!-- Lien dans un nouvel onglet -->
<a href="https://google.com" target="_blank">
  Google (nouvel onglet)
</a>

<!-- Lien interne -->
<a href="contact.html">Page contact</a>

<!-- Lien vers une section (ancre) -->
<a href="#section2">Aller à la section 2</a>

<!-- Lien email -->
<a href="mailto:contact@example.com">
  Envoyer un email
</a>
```

---

# Les images 🖼️

```html
<!-- Image simple -->
<img src="photo.jpg"
     alt="Description de la photo"
     width="600" height="400">

<!-- Image depuis une URL -->
<img src="https://picsum.photos/400/300"
     alt="Image aléatoire">

<!-- Image avec lien -->
<a href="https://example.com">
  <img src="logo.png" alt="Logo">
</a>
```

**L'attribut `alt` est obligatoire** pour l'accessibilité !

---

# L'élément figure 📸

```html
<figure>
  <img src="graphique.png"
       alt="Graphique des ventes 2026">
  <figcaption>
    Figure 1 : Évolution des ventes en 2026
  </figcaption>
</figure>
```

`<figure>` + `<figcaption>` = sémantique pour les images avec légende.

---

# Les tableaux 📊

```html
<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Âge</th>
      <th>Ville</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>25</td>
      <td>Paris</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>30</td>
      <td>Lyon</td>
    </tr>
  </tbody>
</table>
```

---

# En résumé 📝

- **h1 à h6** : titres hiérarchiques (1 seul h1 par page)
- **p** : paragraphe, **strong** : gras, **em** : italique
- **ul/ol + li** : listes non ordonnées / ordonnées
- **a href** : liens hypertextes
- **img src alt** : images (alt obligatoire !)
- **table** : tableaux avec thead/tbody/tr/th/td
