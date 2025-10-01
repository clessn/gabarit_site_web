# Créer votre site web avec GitHub Pages

Bienvenue ! Ce guide vous expliquera comment utiliser GitHub Pages pour créer votre propre site web personnel en utilisant n'importe quel template HTML. 
Suivez attentivement chaque étape, même si vous n'êtes pas familier avec GitHub.

## Prérequis

- Avoir un compte GitHub. Si vous n'en avez pas encore, créez-en un sur [github.com](https://github.com).
- Avoir Git installé sur votre ordinateur. Vous pouvez télécharger Git [ici](https://git-scm.com/downloads) si ce n'est pas déjà fait.
- Un éditeur de texte comme RStudio ou Visual Studio Code pour modifier le code HTML.

## Étape 1: Créer un répertoire GitHub Pages

1. Connectez-vous à GitHub.
2. Cliquez sur **"Use this template"** (bouton vert en haut à droite).
3. Sélectionnez **Create a new repository**
4. Dans la section **Repository name**, entrez votre nom d'utilisateur suivi de `.github.io`. Par exemple, si votre nom d'utilisateur est `joebloe`, nommez le répertoire `joebloe.github.io`. Cela est essentiel pour que GitHub reconnaisse votre site.
5. Assurez-vous que le répertoire est **Public** et cliquez sur **Create repository**.

## Étape 2: Cloner le répertoire sur votre ordinateur

Vous allez maintenant copier le répertoire sur votre machine pour pouvoir le modifier.

1. Sur la page de votre répertoire (par exemple, `https://github.com/joebloe/joebloe.github.io`), cliquez sur le bouton vert **Code**.
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

## Étape 3: Personnaliser votre site

Maintenant que vous avez cloné le répertoire sur votre machine, vous pouvez modifier les fichiers pour y ajouter vos informations personnelles. 
Vous pouvez utiliser RStudio, Visual Studio Code, ou tout autre éditeur de texte pour éditer les fichiers.

Le fichier principal à modifier est généralement `index.html`, car c'est le fichier qui sera affiché par défaut lorsque quelqu'un visite votre site.
Les navigateurs web cherchent automatiquement un fichier `index.html` dans le répertoire racine d'un site web.

À noter: si vous ne souhaitez pas utiliser le modèle déjà présent dans index.html, il existe une multitude de modèles gratuits sur le Web! Visitez par exemple:

- https://html5up.net/ (le modèle proposé vient de ce site);
- https://huggingface.co/spaces/enzostvs/deepsite (pour générer votre site Web par IA).

### Éléments à personnaliser

Voici les éléments que vous devriez généralement personnaliser dans votre template, quel qu'il soit :

#### 1. Le titre du site

Recherchez la balise `<title>` dans le fichier HTML principal. Cette balise détermine ce qui apparaîtra dans l'onglet de votre navigateur.

```html
<title>Votre titre ici</title>
```

#### 2. Votre nom et informations personnelles

Recherchez les sections qui contiennent des informations personnelles comme votre nom, votre métier ou votre description personnelle. Dans la plupart des templates, ces informations se trouvent dans les sections d'en-tête (`header`) ou d'introduction.

#### 3. Vos photos ou images

La plupart des templates incluent des emplacements pour des photos de profil ou des images d'arrière-plan. Remplacez ces images par les vôtres :

1. Préparez vos propres images dans des formats web courants (JPG, PNG)
2. Placez-les dans le dossier approprié (généralement `images/` ou `img/`)
3. Mettez à jour les chemins dans le code HTML si nécessaire

#### 4. Navigation et sections

Personnalisez les sections de votre site selon vos besoins. Vous pouvez généralement :
- Renommer les sections existantes
- Ajouter ou supprimer des sections
- Réorganiser l'ordre des sections

#### 5. Liens vers vos réseaux sociaux

Mettez à jour les liens vers vos profils de réseaux sociaux. Recherchez dans le code HTML les balises `<a>` avec des classes comme `fa-twitter`, `fa-linkedin`, etc.

```html
<a href="https://www.linkedin.com/in/votre-profil">LinkedIn</a>
```

#### 6. Contenu principal

Personnalisez le contenu principal de votre site :
- Votre biographie ou présentation
- Vos compétences
- Vos projets ou réalisations
- Votre parcours académique et professionnel

#### 7. Informations de contact

Assurez-vous de mettre à jour vos informations de contact, notamment votre adresse e-mail :

```html
<a href="mailto:votre-email@example.com">Me contacter</a>
```

#### 8. Stylisation et design

Si vous souhaitez personnaliser davantage l'apparence de votre site, vous pouvez modifier les fichiers CSS (généralement dans un dossier `css/` ou `styles/`). Cela vous permettra de changer les couleurs, les polices, les espacements, etc.

#### 9. Exploration du template

Prenez le temps d'explorer et de comprendre la structure de votre template :
- Identifiez les différents fichiers et leur rôle
- Examinez comment les sections sont organisées
- Notez les classes CSS importantes qui contrôlent le style
- Recherchez les éventuels fichiers JavaScript qui contrôlent les fonctionnalités interactives

## Étape 4: Pousser les modifications sur GitHub

Une fois que vous avez fait toutes les modifications, vous devez les envoyer sur GitHub pour que votre site soit mis à jour.

1. Dans votre terminal, tapez les commandes suivantes :

```bash
git add .
git commit -m "Mise à jour du site avec mes informations"
git push origin main
```

Cela enverra vos modifications sur GitHub.

## Étape 5: Activer GitHub Pages

1. Allez sur la page de votre répertoire sur GitHub.
2. Cliquez sur **Settings**.
3. Dans la barre latérale gauche, cliquez sur **Pages**.
4. Sous **Source**, sélectionnez **main** et **root**.
5. Cliquez sur **Save**. 

Votre site sera maintenant accessible à l'adresse `https://username.github.io`, où `username` est votre nom d'utilisateur GitHub.

### Félicitations !

Vous avez maintenant un site web fonctionnel hébergé gratuitement sur GitHub Pages. Vous pouvez y ajouter plus de contenu et personnaliser votre site autant que vous le souhaitez.

N'hésitez pas à poser des questions si vous rencontrez des difficultés. Bonne chance !


# Bonus : Ajouter un nom de domaine personnalisé

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
   - Cliquez sur l'onglet **Settings** dans votre répertoire.

3. **Aller dans Pages :**
   - Dans la section **Code and automation**, trouvez le lien **Pages**.

4. **Définir le Domaine Personnalisé :**
   - Dans le champ **Custom domain**, entrez votre nom de domaine (par exemple, `www.votrenom.com`).

5. **Créer un Fichier `CNAME` (Optionnel mais Recommandé) :**
   - Dans le répertoire racine de votre répertoire, créez un fichier nommé `CNAME`. Vous pouvez le faire directement sur GitHub.
   - À l'intérieur du fichier `CNAME`, ajoutez votre nom de domaine personnalisé, par exemple :
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


# Bonus : Créer un CV et l'ajouter à votre site

## Étape 1 : Créer votre CV en PDF

1. **Utilisez Quarto pour créer votre CV** : [Quarto CV](https://github.com/schochastics/quarto-cv) offre de nombreux templates modernes et professionnels pour créer facilement un CV. Vous pouvez choisir parmi plusieurs styles comme `awesome-cv`, `markdowncv`, `classic`, `moderncv`, et d'autres.

2. **Installez Quarto et un template** : 

   - Installez [Quarto](https://quarto.org/docs/download/) si ce n'est pas déjà fait
   - Clonez ou téléchargez un template de votre choix depuis https://github.com/schochastics/quarto-cv
   - Suivez les instructions du README pour utiliser le template

3. **Complétez votre CV** : Remplissez le template avec vos informations en format YAML et Markdown. Quarto rend l'édition simple et intuitive.

4. **Rendez votre CV en PDF** : Utilisez la commande `quarto render cv.qmd` pour générer un PDF de votre CV.

5. **Ajoutez le PDF de votre CV à votre répertoire GitHub** :
   - Créez un dossier nommé `cv` à la racine de votre répertoire GitHub.
   - Placez votre CV en PDF dans ce dossier.
   - Prenez une capture d'écran de la première page de votre CV et enregistrez-la dans le même dossier `cv`, sous le nom `cv.png` (cette image servira de solution de secours pour les navigateurs qui ne peuvent pas afficher le PDF intégré).
  
## Étape 2 : Intégrer votre CV en PDF à votre site

Il existe plusieurs façons d'intégrer un PDF à votre site web, quelle que soit la template que vous utilisez. Voici une méthode universelle qui fonctionne avec n'importe quelle structure HTML :

1. **Identifiez l'emplacement où vous souhaitez intégrer votre CV** :
   - Dans votre fichier HTML, choisissez la section où vous voulez que votre CV apparaisse.
   - Cela peut être une section dédiée au CV, ou vous pouvez créer une nouvelle section.

2. **Intégrez le PDF à l'aide de la balise `<object>` ou `<iframe>` ** :

   ```html
   <!-- Méthode 1 : Utilisation de la balise object -->
   <div style="width: 100%; height: 600px; overflow: auto; margin-bottom: 20px;">
     <object data="cv/cv.pdf" type="application/pdf" width="100%" height="100%">
       <p>Il semble que votre navigateur ne puisse pas afficher le PDF intégré. Vous pouvez <a href="cv/cv.pdf">télécharger le PDF</a> ou utiliser l'image d'aperçu ci-dessous.</p>
       <img src="cv/cv.png" alt="Aperçu du CV" style="width: 100%;" />
     </object>
   </div>
   
   <!-- OU -->
   
   <!-- Méthode 2 : Utilisation de la balise iframe -->
   <div style="width: 100%; height: 600px; margin-bottom: 20px;">
     <iframe src="cv/cv.pdf" width="100%" height="100%" style="border: none;">
       Votre navigateur ne supporte pas les iframes. Vous pouvez <a href="cv/cv.pdf">télécharger le PDF</a> directement.
     </iframe>
   </div>
   ```

3. **Ajoutez un lien de téléchargement direct** :

   ```html
   <p>
     <a href="cv/cv.pdf" download>Télécharger mon CV</a>
   </p>
   ```

4. **Adaptez le style à votre template** :
   - Ajustez les styles CSS (largeur, hauteur, marges, etc.) pour que l'intégration s'harmonise avec votre design.
   - Vous pouvez utiliser les classes CSS de votre template pour les boutons et autres éléments.

5. **Vérifiez l'affichage sur différents navigateurs** :
   - Les balises `<object>` et `<iframe>` se comportent différemment selon les navigateurs.
   - L'approche avec la balise `<object>` permet d'afficher une solution de secours (l'image PNG) si le navigateur ne peut pas afficher le PDF.
   - Testez votre site sur différents navigateurs pour vous assurer que le CV s'affiche correctement ou que l'alternative est visible.

# Critères d'évaluation (cours d'outils numériques POL-6078)

- Site Web sur GitHub (30%)
    - Le site web est hébergé sur GitHub, et le répertoire est accessible.
    - Les commits sont visibles et montrent un suivi régulier du travail effectué.
- Respect des étapes et des modifications demandées (50%)
    - L'étudiant.e a suivi les étapes du ReadMe.
    - Les sections essentielles ont été complétées et modifiées correctement.
    - Le contenu du site est pertinent par rapport aux objectifs du cours.
- Personnalisation avancée (20%)
    - L'étudiant.e a personnalisé son site (changement de couleurs, utilisation d’un autre template, ajustements spécifiques à ses besoins).
    - Les modifications vont au-delà des consignes de base, démontrant une initiative supplémentaire.
