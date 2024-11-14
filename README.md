
# Créer votre site web avec GitHub Pages

Bienvenue ! Ce guide vous expliquera comment utiliser GitHub Pages pour créer votre propre site web personnel en utilisant un template HTML. Suivez attentivement chaque étape, même si vous n'êtes pas familier avec GitHub.
Faire un commit
## Prérequis

- Avoir un compte GitHub. Si vous n'en avez pas encore, créez-en un sur [github.com](https://github.com).
- Avoir Git installé sur votre ordinateur. Vous pouvez télécharger Git [ici](https://git-scm.com/downloads) si ce n’est pas déjà fait.
- Un éditeur de texte comme RStudio ou Visual Studio Code pour modifier le code HTML.

---

## Étape 1: Créer un répertoire GitHub Pages

1. Connectez-vous à GitHub.
2. Cliquez sur **"Use this template"** (bouton vert en haut à droite).
3. Sélectionnez **Create a new repository**
4. Dans la section **Repository name**, entrez votre nom d'utilisateur suivi de `.github.io`. Par exemple, si votre nom d'utilisateur est `johndoe`, nommez le répertoire `johndoe.github.io`. Cela est essentiel pour que GitHub reconnaisse votre site.
5. Assurez-vous que le répertoire est **Public** et cliquez sur **Create repository**.

---

## Étape 2: Cloner le répertoire sur votre ordinateur

Vous allez maintenant copier le répertoire sur votre machine pour pouvoir le modifier.

1. Sur la page de votre répertoire (par exemple, `https://github.com/johndoe/johndoe.github.io`), cliquez sur le bouton vert **Code**.
2. Copiez le lien du répertoire.
3. Ouvrez une fenêtre de terminal (ou Git Bash si vous êtes sur Windows) et tapez la commande suivante pour cloner le répertoire dans un dossier sur votre ordinateur :
   
   ```bash
   git clone https://github.com/username/username.github.io
   ```

   Remplacez `username` par votre propre nom d'utilisateur GitHub.

4. Accédez au répertoire cloné :

   ```bash
   cd username.github.io
   ```

---

## Étape 3: Modifier le fichier HTML

Maintenant que vous avez cloné le répertoire sur votre machine, vous pouvez modifier le fichier HTML pour y ajouter vos informations personnelles.
Vous pouvez utiliser RStudio pour éditer le code HTML, ou tout autre éditeur de texte.
Ouvrez le fichier index.html dans votre éditeur de texte.
Il est bon de savoir que le nom du fichier index.html est important, car c'est le fichier qui sera affiché par défaut lorsque quelqu'un visite votre site.
Les navigateurs web cherchent automatiquement un fichier index.html dans le répertoire racine d'un site web.

### Modifications à apporter

#### 1. Le titre du site

Dans le fichier `index.html`, trouvez cette ligne :

```html
<title>Ce qui va apparaître dans la tab de votre site</title>
```

Remplacez le texte entre les balises `<title>` par le titre que vous souhaitez pour votre site. 1Ce texte apparaîtra dans l'onglet de votre navigateur.

#### 2. Votre nom et description

Dans la section `header` du fichier HTML, modifiez les éléments suivants :

- **Nom** : Remplacez `VOTRE NOM` par votre propre nom.

```html
<h1 id="logo"><a href="#">VOTRE NOM</a></h1>
```

- **Description** : Écrivez une courte description de vous-même.

```html
<p>
  Une courte description de vous<br />
  Continuer la courte description
</p>
```

#### 3. Votre photo

Remplacez l'image de profil par une image de vous. Pour cela, vous devez remplacer le fichier `portrait.png` dans le dossier `images` par votre propre image et vous assurer que le nom du fichier est identique.

```html
<img src="images/portrait.png" alt="" />
```

Si vous nommez l'image différemment, modifiez également la ligne ci-dessus avec le nouveau nom de fichier.

#### 4. Sections de navigation

Vous pouvez modifier les sections suivantes dans la barre de navigation :

```html
<li><a href="#one" class="active">À propos</a></li>
<li><a href="#two">Mon travail</a></li>
<li><a href="#three">Mon CV</a></li>
<li><a href="#four">Contact</a></li>
```

Ces liens renvoient aux différentes sections de votre site. Vous pouvez modifier les noms des sections si vous le souhaitez.

#### 5. Vos réseaux sociaux

Modifiez les liens des réseaux sociaux dans la section `footer` :

```html
<a href="https://x.com/MLB/" class="icon brands fa-twitter"><span class="label">Twitter</span></a>
<a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a>
<a href="#" class="icon brands fa-linkedin"><span class="label">LinkedIn</span></a>
<a href="#" class="icon brands fa-github"><span class="label">Github</span></a>
```

Remplacez `href="#"` par le lien vers vos comptes de réseaux sociaux.

#### 6. Texte de la page d'accueil

Modifiez le texte dans la section suivante pour écrire quelque chose de personnel à propos de vous :

```html
<p>
  Faucibus sed lobortis aliquam lorem blandit. Lorem eu nunc metus
  col. Commodo id in arcu ante lorem ipsum sed accumsan erat
  praesent faucibus commodo ac mi lacus. 
</p>
```

#### 7. Section « Mes réalisations »

Ajoutez vos propres projets ou réalisations dans la section `two` :

```html
<h3>Mes réalisations</h3>
<p>Décrivez ici vos travaux ou projets.</p>
```

#### 8. Section « Me joindre »

Trouvez cette ligne et modifiez-la pour ajouter votre propre adresse e-mail :

```
<a href="mailto:your-email@example.com?subject=Sujet&body=Votre message ici." class="button primary">`
```

#### 9. Personnalisation supplémentaire

Vous pouvez personnaliser davantage le site en modifiant les couleurs, les polices, les images, etc. dans le fichier CSS `main.css`.

---

## Étape 4: Pousser les modifications sur GitHub

Une fois que vous avez fait toutes les modifications, vous devez les envoyer sur GitHub pour que votre site soit mis à jour.

1. Dans votre terminal, tapez les commandes suivantes :

```bash
git add .
git commit -m "Mise à jour du site avec mes informations"
git push origin main
```

Cela enverra vos modifications sur GitHub.

---

## Étape 5: Activer GitHub Pages

1. Allez sur la page de votre répertoire sur GitHub.
2. Cliquez sur **Settings**.
3. Dans la barre latérale gauche, cliquez sur **Pages**.
4. Sous **Source**, sélectionnez **main** et **root**.
5. Cliquez sur **Save**. 

Votre site sera maintenant accessible à l'adresse `https://username.github.io`, où `username` est votre nom d'utilisateur GitHub.

---

### Félicitations !

Vous avez maintenant un site web fonctionnel hébergé gratuitement sur GitHub Pages. Vous pouvez y ajouter plus de contenu et personnaliser votre site autant que vous le souhaitez.

---

N'hésitez pas à poser des questions si vous rencontrez des difficultés. Bonne chance !


## Étape 6: Bonus! Ajouter un nom de domaine personnalisé

Ce guide explique comment lier votre site GitHub Pages à votre nom de domaine personnalisé en utilisant Namecheap. Dans cet exemple, nous utiliserons le domaine `votrenom.com` comme domaine personnalisé.

### Prérequis

1. Un répertoire GitHub avec un site GitHub Pages configuré (par exemple, `username.github.io` ou `organisation.github.io`).
2. Un nom de domaine personnalisé enregistré chez un fournisseur de nom de domaine comme Namecheap (par exemple, `votrenom.com`).

### Étape 1 : Configurer les Enregistrements DNS sur Namecheap

Nous devons configurer les paramètres DNS sur Namecheap pour pointer votre domaine vers GitHub Pages.

1. **Connectez-vous à Namecheap :**
   - Allez sur [namecheap.com](https://www.namecheap.com) et connectez-vous à votre compte.

2. **Accéder à la Liste de Domaines :**
   - Depuis le tableau de bord, cliquez sur **Domain List** dans la barre latérale gauche.
   - Trouvez votre domaine (par exemple, `votrenom.com`) et cliquez sur **Manage**.

3. **Mettre à Jour les Paramètres DNS :**
   - Dans la section **DNS**, réglez **Nameservers** sur **Namecheap Basic DNS** si cela n'est pas déjà fait.

4. **Ajouter les Enregistrements DNS Suivants :**

   - Dans la page **Advanced DNS**, ajoutez cliquez sur `ADD NEW RECORD` et ajoutez les enregistrements suivants :

   | Type d'Enregistrement | Hôte           | Valeur                          | TTL  |
   |-----------------------|----------------|---------------------------------|------|
   | CNAME Record                 | www            | `username.github.io`            | Automatique |
   | A Record       | @              | `185.199.108.153`               | Automatique |
   | A Record       | @              | `185.199.109.153`               | Automatique |
   | A Record       | @              | `185.199.110.153`               | Automatique |
   | A Record       | @              | `185.199.111.153`               | Automatique |

   **Explication :**
   - L'enregistrement `CNAME` pointe `www.votrenom.com` vers votre site GitHub Pages.
   - Les enregistrements `A` garantissent que `votrenom.com` (sans `www`) pointe également vers le même site GitHub Pages.

5. **Enregistrer les Modifications** et attendez que les paramètres DNS se propagent. Cela peut prendre de quelques minutes à plusieurs heures.

### Étape 2 : Configurer GitHub Pages pour un Domaine Personnalisé

1. **Accéder à Votre répertoire :**
   - Allez dans le répertoire GitHub qui héberge votre site GitHub Pages.

2. **Ouvrir les Paramètres du répertoire :**
   - Cliquez sur l’onglet **Settings** dans votre répertoire.

3. **Aller dans Pages :**
   - Dans la section **Code and automation**, trouvez le lien **Pages**.

4. **Définir le Domaine Personnalisé :**
   - Dans le champ **Custom domain**, entrez votre nom de domaine (par exemple, `www.votrenom.com`).

5. **Créer un Fichier `CNAME` (Optionnel mais Recommandé) :**
   - Dans le répertoire racine de votre répertoire, créez un fichier nommé `CNAME`. Vous pouvez le faire directement sur GitHub.
   - À l’intérieur du fichier `CNAME`, ajoutez votre nom de domaine personnalisé, par exemple :
     ```
     www.votrenom.com
     ```



### Étape 3 : Vérifier la Configuration

1. **Visitez Votre Domaine :**
   - Ouvrez un navigateur et visitez `www.votrenom.com`. Il devrait afficher votre site GitHub Pages.
   - Essayez également de visiter `votrenom.com`, pour vous assurer que les deux domaines, avec et sans `www`, fonctionnent.

2. **Vérifier le HTTPS :**
   - Une fois que GitHub Pages configure le HTTPS (cela peut prendre quelques minutes), assurez-vous que votre site est accessible via HTTPS (`https://www.votrenom.com`).

### Dépannage

- **Temps de Propagation des DNS :** Les modifications des enregistrements DNS peuvent prendre du temps à se propager. Vous pouvez vérifier l'état DNS avec des outils en ligne comme [WhatsMyDNS](https://www.whatsmydns.net/).
- **Problèmes de HTTPS :** Si le HTTPS ne fonctionne pas, assurez-vous que l'option **Enforce HTTPS** est cochée dans les paramètres GitHub Pages et que les enregistrements DNS sont correctement configurés.

## Ressources

- [Documentation GitHub Pages Custom Domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Configuration DNS sur Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/9776/2237/how-to-set-up-dns-records-for-your-domain-in-namecheap)

Voilà ! Vous avez réussi à lier votre site GitHub Pages au domaine personnalisé `votrenom.com`.

# Critères d'évaluation

- Site Web sur GitHub (30%)
    - Le site web est hébergé sur GitHub, et le répertoire est accessible.
    - Les commits sont visibles et montrent un suivi régulier du travail effectué.
- Respect des étapes et des modifications demandées (60%)
    - L'étudiant.e a suivi les étapes du ReadMe.
    - Les sections essentielles ont été complétées et modifiées correctement.
    - Le contenu du site est pertinent par rapport aux objectifs du projet.
- Personnalisation avancée (10%)
    - L'étudiant.e ont personnalisé leur site (changement de couleurs, utilisation d’un autre template, ajustements spécifiques à leurs besoins).
    - Les modifications vont au-delà des consignes de base, démontrant une initiative supplémentaire.

# Consignes pour le travail de fin de session (2e itération)

Bravo pour la première itération de votre site web ! Dans cette deuxième itération, vous allez enrichir votre site avec un CV en format PDF, ajouter une nouvelle section pour héberger vos projets et y déposer déjà un premier projet. Suivez les étapes ci-dessous pour intégrer ces nouveaux éléments. 

## Étape 1 : Créer un CV et l'ajouter à votre site

1. **Choisissez un gabarit de CV en LaTeX** : [Overleaf]([https://www.overleaf.com/](https://fr.overleaf.com/gallery/tagged/cv)) présente de nombreux gabarits et est simple d'utilisation, mais vous pouvez fouiller ailleurs sans problème.

2. **Complétez votre CV** : Remplissez le gabarit avec vos informations. Assurez-vous que votre CV est complet et bien présenté.

3. **Enregistrez votre CV en PDF** : Une fois terminé, exportez votre CV en format PDF.

4. **Ajoutez le code source et le PDF de votre CV à votre répertoire GitHub** :
   - Créez un dossier nommé `cv` à la racine de votre répertoire GitHub.
   - Placez-y votre fichier LaTeX.
   - Placez également votre CV en PDF dans ce dossier.
   - Prenez une capture d’écran de la première page de votre CV et enregistrez-la dans le même dossier `cv`, sous le nom `cv.png`.
  
## Étape 2 : Intégrer un lien vers le CV en PDF et afficher un aperçu dans la section «Mon CV»

1. **Modifiez la section «Mon CV» dans le code HTML** :
   - Dans votre fichier `index.html`, localisez la section `three`, qui commence par :

     ```html
     <!-- Three -->
     <section id="three">
     ```

2. **Ajoutez le lien vers le CV et l’image d’aperçu** :
   - Remplacez le contenu de cette section avec les modifications ci-dessous pour intégrer le lien vers le CV PDF ainsi que l’aperçu de l’image.

   ```html
   <!-- Three -->
   <section id="three">
     <div class="container">
       <h3>Mon CV</h3>
       <p>
         Vous trouverez ci-dessous un aperçu de mon CV. Cliquez sur l’image ou le bouton pour consulter le document complet en format PDF.
       </p>
       <div class="features">
         <article>
           <!-- Aperçu du CV en image -->
           <a href="cv/cv.pdf" class="image" target="_blank">
             <img src="cv/cv.png" alt="Aperçu du CV" />
           </a>
           <div class="inner">
             <h4>Consultez mon CV</h4>
             <p>
               Cliquez sur l'image ci-dessus ou sur le lien ci-dessous pour ouvrir mon CV en PDF dans un nouvel onglet.
             </p>
             <!-- Lien direct vers le CV en PDF -->
             <p>
               <a href="cv/cv.pdf" target="_blank" class="button primary">
                 Voir le CV en PDF
               </a>
             </p>
           </div>
         </article>
       </div>
     </div>
   </section>
   ```

3. **Vérifiez l’affichage de votre site** :
   - Enregistrez les modifications et poussez-les sur GitHub.
   - Accédez à votre site et allez à la section «Mon CV» pour vérifier que l’image s’affiche correctement et que les liens vers le CV en PDF fonctionnent.

---

## Étape 3 : Ajouter une section «Mes Projets» et intégrer un projet de session

Après la section «Mon CV», nous allons ajouter une nouvelle section nommée «Mes Projets». Notez que dans le code initial, il y a seulement 4 sections : «À propos», «Mon travail», «Mon CV», et «Me joindre». Vous devrez donc insérer cette cinquième section **entre «Mon CV» et «Me joindre»**.

### 1. Créer la section «Mes Projets» dans le code HTML

1. **Ajoutez un onglet «Mes Projets»** dans le menu de navigation :
   - Dans votre fichier `index.html`, localisez la section de navigation :

     ```html
      <nav id="nav">
        <ul>
          <li><a href="#one" class="active">À propos</a></li>
          <li><a href="#two">Mon travail</a></li>
          <li><a href="#three">Mon CV</a></li>
          <li><a href="#four">Contact</a></li>
        </ul>
      </nav>
     ```
     
   - Ajoutez entre `three` et  `four` le lien vers cette nouvelle section en insérant le code suivant :

     ```html
     <li><a href="#projets">Mes Projets</a></li>
     ```

2. **Insérez la section «Mes Projets» dans le code HTML** :
   - Placez cette section après les sections entre `three` et  `four` de votre fichier `index.html`, de façon à ce qu’elle apparaisse avant «Me joindre».

   ```html
   <!-- Mes projets -->
   <section id="projets">
     <div class="container">
       <h3>Mes Projets</h3>
       <p>
         Voici une sélection de mes projets. Cliquez sur l'image pour découvrir le projet complet.
       </p>
       <div class="features">
         <article>
           <!-- Aperçu du projet en image -->
           <a href="projet_session/projet.html" class="image" target="_blank">
             <img src="projet_session/projet.png" alt="Aperçu du projet de session" />
           </a>
           <div class="inner">
             <h4>Cours d'outils numériques (POL-6078)</h4>
             <p>
               Cliquez sur l'image ou sur le lien ci-dessous pour explorer le contenu de ce projet.
             </p>
             <!-- Lien direct vers le projet -->
             <p>
               <a href="projet_session/projet.html" target="_blank" class="button primary">
                 Voir le projet complet
               </a>
             </p>
           </div>
         </article>
       </div>
     </div>
   </section>
   ```

### 2. Préparer le document R Markdown

1. **Créez un dossier nommé `projet_session`** dans votre répertoire GitHub :
   - Ce dossier contiendra le fichier R Markdown et les ressources associées à votre projet de session.

2. **Dans le dossier `projet_session`, enregistrer un fichier R Markdown nommé `projet.Rmd`**
   - Vous pouvez utiliser un gabarit R Markdown trouvé en ligne ou démarrer d'une page blanche via RStudio.
   - Pour créer une fichier R Markdown sur RStudio, cliquez sur «Files», «New File», puis «R Markdown...»
     
![Capture d’écran, le 2024-11-13 à 18 29 22](https://github.com/user-attachments/assets/138d6800-5182-4f73-ba88-f632b01a9e75)

3. **Exportez le fichier R Markdown en HTML** :
   - Vous pouvez vider le contenu par défaut de cette page, ou conserver l'en-tête, au choix.
   - L'important sera d'exporter le résultat (on dit « knit », en langage Markdown) en format html et de l'enregistrer dans votre dossier `projet_session`
   - Une fois le fichier `projet.md` complété, exportez-le en HTML et nommez ce fichier `projet.html`.
   - Prenez une capture d'écran de votre projet (ou une image trouvée sur le Web, au choix) et placez l’image d’aperçu du projet dans le même dossier `projet_session` et nommez-la `projet.png`.
  
![Capture d’écran, le 2024-11-13 à 18 32 54](https://github.com/user-attachments/assets/b4f6b682-ab1e-4536-8b31-5ac5e7abcde0)

4. **Vérifiez l’affichage de votre site** :
   - Enregistrez et poussez vos modifications sur GitHub.
   - Allez à la section « Mes Projets » pour vérifier que l’image d’aperçu est bien affichée et que le lien mène au contenu du projet en HTML.

### 3. Remplir le document R Markdown

Dans cette étape, vous allez réaliser un court projet de session dans votre page HTML de projet (écrite en R Markdown) qui démontrera votre capacité à utiliser différents outils de recherche tout au long du cycle de la recherche, tel que représenté dans l'image du cycle de recherche hypothético-déductif issue de la méthode scientifique.

En fonction des étapes indiquées dans l'image et vues en classe, suivez les consignes ci-dessous pour structurer votre projet de session.

![science_outils](https://github.com/user-attachments/assets/6f69f8f3-2450-4687-b23c-a574ed265f65)

#### Étapes du projet

1. **Question de recherche et hypothèse** :
   - Posez une question de recherche.
   - Effectuez une brève revue de la littérature scientifique pour dériver une hypothèse de recherche en lien avec votre question.
   - **Indiquez les outils utilisés** pour cette étape (ex. Google Scholar, Zotero, Elicit, etc.) et détaillez pourquoi et comment vous les avez utilisés (par exemple, pour trouver des articles, organiser des sources, etc.).

2. **Collecte de données** :
   - Choisissez un outil pour collecter des données en lien avec votre hypothèse (ex. Factiva, Eureka, un questionnaire en ligne, une base de données en libre accès, etc., des données extraites du Web, etc.).
   - **Présentez l'outil choisi** et expliquez en détail comment vous l'avez utilisé pour collecter vos données.

3. **Analyse et visualisation des données** :
   - Utilisez un outil pour analyser et/ou visualiser les données que vous avez collectées (ex. Excel, R, Python, Tableau, etc.).
   - **Détaillez l'outil utilisé** et expliquez comment vous vous en êtes servi pour produire des résultats ou des visualisations.

4. **Discussion** :
   - Ajoutez une section de discussion à la fin de votre projet.
   - Dans cette discussion, expliquez vos choix d'outils en fonction **des valeurs, de la philosophie ou des besoins** qui ont guidé vos décisions.
   -  Basez-vous, entre autres, sur les critères de sélection des outils vus en classe: l'accessibilité, l'existence d'une communauté d'utilisateurs, la popularité dans votre domaine, leur compatibilité avec d'autres outils, le besoin de transparence et la réplicabilité, et la capacité d'adaptabilité et de flexibilité des outils.

#### Important

Il n'y a pas de bonne ou mauvaise réponse pour ce travail. L'objectif est de démontrer votre capacité à utiliser des outils numériques de recherche tout au long d'un processus de recherche, de la réflexion sur une question jusqu'à la présentation des résultats. Ce travail doit refléter votre compréhension et votre maîtrise des outils ainsi que la manière dont vous les avez intégrés dans le cycle de la recherche.

### 4. Ajoutez tous les fichiers pertinents à votre répertoire GitHub

Votre dossier `projet_session` devrait contenir un dossier `code` à l'intérieur duquel se retrouvent les codes R (si vous utilisez cet outil, par exemple) créés pour l'analyse et la visualisation de données. Il pourrait y avoir également un dossier `data`, dans lequel se retrouvent les données collectées, et un dossier `images` dans lequel se trouvent vos graphiques et vos visualisations. Peu importe les outils choisis, assurez-vous que tout le contenu pertinent à l'évaluation de votre travail se retrouve dans le dossier `projet_session` de votre repo GitHub.

---

Une fois le projet complété, assurez-vous de bien respecter la structure décrite ci-dessus pour que chaque étape du cycle de recherche soit clairement identifiable dans votre document.

Bien joué!

---

### Critères d'évaluation de la 2e itération

**1. Site Web sur GitHub (20%)**
   - Le site web est hébergé correctement sur GitHub, et le répertoire est accessible.
   - Les commits sont visibles et montrent un suivi régulier du travail effectué.
   - Les fichiers (PDF, images, fichier markdown, HTML du projet) sont bien organisés dans les dossiers indiqués (`cv`, `projet_session`).

**2. Respect des consignes et des étapes (30%)**
   - L’étudiant.e a suivi toutes les étapes du ReadMe.
   - Les nouvelles sections «Mon CV» et «Mes Projets» sont présentes et complétées correctement.
   - Le lien vers le CV en PDF fonctionne, et l’aperçu du CV s'affiche bien dans la section «Mon CV».
   - La section «Mes Projets» contient une image cliquable qui mène au fichier HTML du projet de session.
   - La page HTML du projet de session respecte la structure demandée, avec chaque étape du cycle de recherche clairement identifiable.

**3. Qualité et clarté du contenu de recherche (40%)**
   - La question de recherche, l’hypothèse, la collecte de données, l'analyse et la discussion sont clairs et pertinents.
   - L’étudiant.e décrit de manière détaillée les outils utilisés à chaque étape et la manière dont ils ont été appliqués.
   - La visualisation de données est intéressante, pertinente et bien réalisée.
   - La discussion sur les choix d'outils montre une réflexion personnelle et justifie les choix par rapport aux valeurs ou à la philosophie de recherche.

**4. Créativité et personnalisation (10%)**
   - L’étudiant.e a pris des initiatives pour personnaliser son site au-delà des consignes de base, par exemple :
     - Amélioration du design ou des couleurs du site.
     - Choix d'un style ou d'une mise en page unique pour le projet de session.
     - Utilisation avancée de markdown ou d’éléments visuels pour enrichir la présentation du projet.

