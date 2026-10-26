---
theme: ./
colorSchema: "auto"
layout: intro
highlighter: shiki
title: Formation HTML et CSS3 - Initiation 2026
#transition: slide-left
download: "https://html-css3.andromed.fr/slides.pdf"
themeConfig:
  logoHeader: "/avatar.png"
  eventLogo: "https://img2.storyblok.com/352x414/f/84560/2388x414/23d8eb4b8d/vue-amsterdam-with-name.png"
  eventUrl: "https://vuejs.amsterdam/"
---

# HTML et CSS3 - Initiation

🌐 Une formation présentée par Andromed.

💚 01 - 03 Avril 2026

<div class="pt-12">
  <span @click="next" class="px-2 p-3 rounded cursor-pointer hover:bg-white hover:bg-opacity-10 neon-border">
    Appuyez sur espace pour la page suivante <carbon:arrow-right class="inline"/>
  </span>
</div>


<div class="absolute flex gap-x-2 bottom-0 left-0 p-4 z-50">
      <SlideCurrentNo
        class="dark:!text-white !text-[8px] p-1 w-5 h-5 items-center justify-center flex rounded-full bg-white/10 backdrop-blur-sm border border-gray-600 opacity-80"
      />
      <span class="text-gray-400">/</span>
  <SlideTotal
        class="dark:!text-white !text-[8px] p-1 w-5 h-5 items-center justify-center flex rounded-full bg-white/10 backdrop-blur-sm border border-gray-600 opacity-80"
      />
</div>


<div class="absolute bottom-0 right-0 z-50 flex flex-col gap-y-2 p-2">
<div class="hover:bg-white hover:bg-opacity-10 neon-border border-2 rounded-xl w-[200px] p-2 flex flex-col gap-y-2">
  <span class="text-gray-400 text-xs">Programme : <b>2-024</b></span>
  <span class="text-gray-400 text-xs">Lot: <b>2</b></span>
</div>
</div>


---
layout: presenter
eventLogo: 'https://img2.storyblok.com/352x0/f/84560/2388x414/23d8eb4b8d/vue-amsterdam-with-name.png'
eventUrl: 'https://vuejs.amsterdam/'
twitter: '@jimmylansrq'

twitterUrl: 'https://twitter.com/jimmylansrq'
presenterImage: 'https://legacy.andromed.fr/images/fondator.jpg'
---

# Jimmylan Surquin

Fondateur <a  href="https://www.andromed.fr/"><logos-storyblok-icon  mr-1/>Andromed</a>

- Lille, France 🇫🇷
- Création de contenu sur <a href="https://www.youtube.com/channel/jimmylansrq"> <logos-youtube-icon mr-1 /> jimmylansrq </a>
- Blog & Portfolio <a href="https://jimmylan.fr"> jimmylan.fr </a>

---
layout: text-image
media: 'https://i.pinimg.com/originals/f5/5e/80/f55e8059ea945abfd6804b887dd4a0af.gif'
caption: 'HTML & CSS3 2026'
---

# DISCLAIMER 🌐

### Dans cette formation nous allons voir les bases du HTML et CSS3 pour créer des pages web modernes.

---
layout: two-cols
routeAlias: 'sommaire'
---

<a name="sommaire" id="sommaire"></a>

# SOMMAIRE HTML & CSS3 📜

### Jour 1 : Fondamentaux HTML

<div class="flex flex-col gap-2">
<Link to="introduction-web">🌍 1. Introduction au Web</Link>
<Link to="html-structure">🏗️ 2. Structure HTML</Link>
<Link to="html-texte-liens">📝 3. Texte, liens et images</Link>
<Link to="html-formulaires">📋 4. Formulaires HTML</Link>
</div>

### Jour 2 : CSS3

<div class="flex flex-col gap-2">
<Link to="css-introduction">🎨 5. Introduction au CSS</Link>
<Link to="css-box-model">📦 6. Box Model et positionnement</Link>
<Link to="css-flexbox">💪 7. Flexbox</Link>
</div>

::right::

### Jour 3 : CSS avancé et projet

<div class="flex flex-col gap-2">
<Link to="css-grid">🔲 8. CSS Grid</Link>
<Link to="css-responsive">📱 9. Responsive Design</Link>
<Link to="css-animations">✨ 10. Animations et transitions</Link>
<Link to="projet-final">🎯 11. Projet final</Link>
<Link to="qcm-final">✅ QCM de validation finale</Link>
</div>

<br>

**Note :** Chaque module contient :
- 📖 Cours théorique
- ✅ QCM de validation
- 🎯 Exercices pratiques

---
layout: two-cols
---

### PROGRAMME JOUR 1 : HTML 📅

<small>

**Module 1 - Introduction au Web**
- Comment fonctionne Internet ?
- Client / Serveur
- Navigateurs et standards
- Outils de développement (VSCode)

**Module 2 - Structure HTML**
- Anatomie d'un document HTML
- Balises et attributs
- HTML5 sémantique
- Validation W3C

</small>

::right::

<small>

**Module 3 - Texte, liens et images**
- Titres, paragraphes, listes
- Liens hypertextes
- Images et multimedia
- Tableaux

**Module 4 - Formulaires HTML**
- Inputs et labels
- Types d'inputs HTML5
- Validation native
- Accessibilité des formulaires

</small>

---
layout: two-cols
---

### PROGRAMME JOUR 2 : CSS3 📅

<small>

**Module 5 - Introduction au CSS**
- Syntaxe CSS
- Sélecteurs (élément, classe, id)
- Couleurs et unités
- Typographie web

**Module 6 - Box Model**
- Margin, border, padding
- Width et height
- Display (block, inline, inline-block)
- Positionnement (relative, absolute, fixed)

</small>

::right::

<small>

**Module 7 - Flexbox**
- Axes principal et transversal
- justify-content, align-items
- flex-wrap, flex-grow
- Cas d'usage pratiques

</small>

---
layout: two-cols
---

### PROGRAMME JOUR 3 : CSS avancé 📅

<small>

**Module 8 - CSS Grid**
- grid-template-columns/rows
- grid-gap
- grid-area
- Layout complet avec Grid

**Module 9 - Responsive Design**
- Media queries
- Mobile First
- Images responsive
- Unités relatives (rem, em, vw, vh)

</small>

::right::

<small>

**Module 10 - Animations**
- Transitions CSS
- Keyframes
- Transform (translate, rotate, scale)
- Bonnes pratiques performance

**Module 11 - Projet final**
- Création d'un portfolio complet
- HTML sémantique + CSS moderne
- Responsive + animations

**QCM Final** ✅

</small>

---
src: './pages/01-introduction-web.md'
---

---
src: './pages/01-qcm-introduction.md'
---

---
src: './pages/02-html-structure.md'
---

---
src: './pages/02-qcm-structure.md'
---

---
src: './pages/02-exercices-structure.md'
---

---
src: './pages/03-html-texte-liens.md'
---

---
src: './pages/03-qcm-texte.md'
---

---
src: './pages/03-exercices-texte.md'
---

---
src: './pages/04-html-formulaires.md'
---

---
src: './pages/04-qcm-formulaires.md'
---

---
src: './pages/04-exercices-formulaires.md'
---

---
src: './pages/05-css-introduction.md'
---

---
src: './pages/05-qcm-css-intro.md'
---

---
src: './pages/05-exercices-css-intro.md'
---

---
src: './pages/06-css-box-model.md'
---

---
src: './pages/06-qcm-box-model.md'
---

---
src: './pages/06-exercices-box-model.md'
---

---
src: './pages/07-css-flexbox.md'
---

---
src: './pages/07-qcm-flexbox.md'
---

---
src: './pages/07-exercices-flexbox.md'
---

---
src: './pages/08-css-grid.md'
---

---
src: './pages/08-qcm-grid.md'
---

---
src: './pages/08-exercices-grid.md'
---

---
src: './pages/09-css-responsive.md'
---

---
src: './pages/09-qcm-responsive.md'
---

---
src: './pages/09-exercices-responsive.md'
---

---
src: './pages/10-css-animations.md'
---

---
src: './pages/10-qcm-animations.md'
---

---
src: './pages/10-exercices-animations.md'
---

---
src: './pages/11-projet-final.md'
---

---
src: './pages/12-qcm-final.md'
---
