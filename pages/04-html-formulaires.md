---
layout: new-section
routeAlias: 'html-formulaires'
---

<a name="html-formulaires" id="html-formulaires"></a>

# 📋 Module 4
## Formulaires HTML

### Créer des formulaires interactifs

---

# Structure de base d'un formulaire 📝

```html
<form action="/inscription" method="POST">
  <label for="nom">Nom :</label>
  <input type="text" id="nom" name="nom"
         placeholder="Votre nom" required>

  <label for="email">Email :</label>
  <input type="email" id="email" name="email"
         placeholder="votre@email.com" required>

  <button type="submit">Envoyer</button>
</form>
```

---

# Les attributs du formulaire

- `action` : URL où envoyer les données
- `method` : GET (dans l'URL) ou POST (dans le corps)
- `for` + `id` : lie le label à l'input (accessibilité !)
- `name` : nom du champ envoyé au serveur
- `placeholder` : texte d'aide grisé
- `required` : champ obligatoire

---

# Les types d'input HTML5 🎨

```html
<input type="text">       <!-- Texte libre -->
<input type="email">      <!-- Email (validation) -->
<input type="password">   <!-- Mot de passe (masqué) -->
<input type="number">     <!-- Nombre -->
<input type="tel">        <!-- Téléphone -->
<input type="url">        <!-- URL -->
<input type="date">       <!-- Sélecteur de date -->
<input type="time">       <!-- Heure -->
<input type="color">      <!-- Sélecteur de couleur -->
<input type="range">      <!-- Curseur -->
<input type="file">       <!-- Upload de fichier -->
<input type="search">     <!-- Champ de recherche -->
```

---

# Autres éléments de formulaire 📦

```html
<!-- Zone de texte multi-lignes -->
<textarea name="message" rows="5" cols="40">
</textarea>

<!-- Liste déroulante -->
<select name="pays">
  <option value="">Choisir un pays</option>
  <option value="fr">France</option>
  <option value="be">Belgique</option>
  <option value="ch">Suisse</option>
</select>
```

---

# Cases à cocher et boutons radio 🔘

```html
<!-- Cases à cocher (choix multiples) -->
<input type="checkbox" id="html" name="skills"
       value="html">
<label for="html">HTML</label>

<input type="checkbox" id="css" name="skills"
       value="css">
<label for="css">CSS</label>

<!-- Boutons radio (choix unique) -->
<input type="radio" id="oui" name="newsletter"
       value="oui">
<label for="oui">Oui</label>

<input type="radio" id="non" name="newsletter"
       value="non">
<label for="non">Non</label>
```

---

# Validation native HTML5 ✅

```html
<!-- Champ obligatoire -->
<input type="text" required>

<!-- Longueur min/max -->
<input type="text" minlength="2" maxlength="50">

<!-- Pattern (expression régulière) -->
<input type="text"
       pattern="[A-Za-z]{2,}"
       title="Au moins 2 lettres">

<!-- Nombre min/max -->
<input type="number" min="18" max="120">
```

---

# Grouper les champs avec fieldset 📦

```html
<form>
  <fieldset>
    <legend>Informations personnelles</legend>
    <label for="nom">Nom :</label>
    <input type="text" id="nom" name="nom">
    <label for="prenom">Prénom :</label>
    <input type="text" id="prenom" name="prenom">
  </fieldset>

  <fieldset>
    <legend>Coordonnées</legend>
    <label for="email">Email :</label>
    <input type="email" id="email" name="email">
  </fieldset>
</form>
```

---

# Accessibilité des formulaires ♿

**Bonnes pratiques :**
- Toujours utiliser `<label>` avec `for`/`id`
- Ajouter `aria-label` si pas de label visible
- Utiliser `fieldset` + `legend` pour grouper
- Indiquer les champs obligatoires visuellement
- Messages d'erreur clairs et proches du champ

---

# En résumé 📝

- `<form>` avec `action` et `method`
- `<label>` + `<input>` liés par `for`/`id`
- HTML5 offre de nombreux **types d'input** (email, date, etc.)
- **Validation native** : required, minlength, pattern
- `<select>`, `<textarea>`, checkbox, radio
- **fieldset** + **legend** pour grouper
- **Accessibilité** : labels, aria, messages d'erreur
