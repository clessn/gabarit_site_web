
# Créer votre site web avec GitHub Pages

Bienvenue ! Ce guide vous expliquera comment utiliser GitHub Pages pour créer votre propre site web personnel en utilisant un template HTML. Suivez attentivement chaque étape, même si vous n'êtes pas familier avec GitHub.

## Prérequis

- Avoir un compte GitHub. Si vous n'en avez pas encore, créez-en un sur [github.com](https://github.com).
- Avoir Git installé sur votre ordinateur. Vous pouvez télécharger Git [ici](https://git-scm.com/downloads) si ce n’est pas déjà fait.
- Un éditeur de texte comme Visual Studio Code ou Notepad++ pour modifier le code HTML.

---

## Étape 1: Créer un dépôt GitHub Pages

1. Connectez-vous à GitHub.
2. Allez à l'adresse suivante : [https://github.com/clessn/gabarit_site_web](https://github.com/clessn/gabarit_site_web).
3. Cliquez sur **"Use this template"** (bouton vert en haut à droite).
4. Dans la section **Repository name**, entrez votre nom d'utilisateur suivi de `.github.io`. Par exemple, si votre nom d'utilisateur est `johndoe`, nommez le dépôt `johndoe.github.io`. Cela est essentiel pour que GitHub reconnaisse votre site.
5. Assurez-vous que le dépôt est **Public** et cliquez sur **Create repository from template**.

---

## Étape 2: Cloner le dépôt sur votre ordinateur

Vous allez maintenant copier le dépôt sur votre machine pour pouvoir le modifier.

1. Sur la page de votre dépôt (par exemple, `https://github.com/johndoe/johndoe.github.io`), cliquez sur le bouton vert **Code**.
2. Copiez le lien du dépôt.
3. Ouvrez une fenêtre de terminal (ou Git Bash si vous êtes sur Windows) et tapez la commande suivante pour cloner le dépôt :
   
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

Maintenant que vous avez cloné le dépôt sur votre machine, vous pouvez modifier le fichier HTML pour y ajouter vos informations personnelles.

### Modifications à apporter

#### 1. Le titre du site

Dans le fichier `index.html`, trouvez cette ligne :

```html
<title>Ce qui va apparaître dans la tab de votre site</title>
```

Remplacez le texte entre les balises `<title>` par le titre que vous souhaitez pour votre site. Ce texte apparaîtra dans l'onglet de votre navigateur.

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
<a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a>
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

1. Allez sur la page de votre dépôt sur GitHub.
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
