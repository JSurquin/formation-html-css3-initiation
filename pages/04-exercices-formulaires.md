---

# Exercices Module 4 : Formulaires 🎯

---

# Exercice : Formulaire d'inscription (20 min)

**Consigne :** Créez un formulaire d'inscription avec :
1. Nom et prénom (texte, requis, min 2 caractères)
2. Email (type email, requis)
3. Mot de passe (min 8 caractères)
4. Date de naissance (type date)
5. Genre (boutons radio)
6. Compétences (cases à cocher)
7. Pays (liste déroulante)
8. Message (textarea)
9. Bouton d'envoi

---

# Exercice : Solution ✅

```html
<form action="/inscription" method="POST">
  <fieldset>
    <legend>Identité</legend>
    <label for="nom">Nom :</label>
    <input type="text" id="nom" name="nom"
           required minlength="2">
    <label for="prenom">Prénom :</label>
    <input type="text" id="prenom" name="prenom"
           required minlength="2">
    <label for="email">Email :</label>
    <input type="email" id="email" name="email"
           required>
    <label for="mdp">Mot de passe :</label>
    <input type="password" id="mdp" name="mdp"
           required minlength="8">
    <label for="ddn">Date de naissance :</label>
    <input type="date" id="ddn" name="ddn">
  </fieldset>
```

---

# Exercice : Solution (suite)

```html
  <fieldset>
    <legend>Genre</legend>
    <input type="radio" id="h" name="genre"
           value="homme">
    <label for="h">Homme</label>
    <input type="radio" id="f" name="genre"
           value="femme">
    <label for="f">Femme</label>
    <input type="radio" id="a" name="genre"
           value="autre">
    <label for="a">Autre</label>
  </fieldset>

  <fieldset>
    <legend>Compétences</legend>
    <input type="checkbox" id="html" name="skills"
           value="html">
    <label for="html">HTML</label>
    <input type="checkbox" id="css" name="skills"
           value="css">
    <label for="css">CSS</label>
  </fieldset>
```

---

# Exercice : Solution (fin)

```html
  <label for="pays">Pays :</label>
  <select id="pays" name="pays">
    <option value="">-- Choisir --</option>
    <option value="fr">France</option>
    <option value="be">Belgique</option>
    <option value="ch">Suisse</option>
  </select>

  <label for="msg">Message :</label>
  <textarea id="msg" name="message"
            rows="4" cols="40"></textarea>

  <button type="submit">S'inscrire</button>
</form>
```
