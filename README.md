
# Créer votre site web avec GitHub Pages

Bienvenue ! Ce guide vous expliquera comment utiliser GitHub Pages pour créer votre propre site web personnel en utilisant un template HTML. Suivez attentivement chaque étape, même si vous n'êtes pas familier avec GitHub.

## Prérequis

- Avoir un compte GitHub. Si vous n'en avez pas encore, créez-en un sur [github.com](https://github.com).
- Avoir Git installé sur votre ordinateur. Vous pouvez télécharger Git [ici](https://git-scm.com/downloads) si ce n’est pas déjà fait.
- Un éditeur de texte comme Visual Studio Code ou Notepad++ pour modifier le code HTML.

---

## Étape 1: Créer un répertoire GitHub Pages

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
Vous pouvez utiliser R pour éditer le code HTML, ou tout autre éditeur de texte.
Ouvrez le fichier index.html dans votre éditeur de texte.
Il est bon de savoir que le nom du fichier index.html est important, car c'est le fichier qui sera affiché par défaut lorsque quelqu'un visite votre site.
Les navigateurs web cherchent automatiquement un fichier index.html dans le répertoire racine d'un site web.

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

#### 8. Section « Me joindre »


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


## Étape 6: Bonus! Ajouter un nom de domaine personnalisé

Ce guide explique comment lier votre site GitHub Pages à votre nom de domaine personnalisé en utilisant Namecheap. Dans cet exemple, nous utiliserons le domaine `votrenom.com` comme domaine personnalisé.

### Prérequis

1. Un dépôt GitHub avec un site GitHub Pages configuré (par exemple, `username.github.io` ou `organisation.github.io`).
2. Un nom de domaine personnalisé enregistré chez Namecheap (par exemple, `votrenom.com`).

### Étape 1 : Configurer GitHub Pages pour un Domaine Personnalisé

1. **Accédez à Votre Dépôt :**
   - Allez dans le dépôt GitHub qui héberge votre site GitHub Pages.

2. **Ouvrir les Paramètres du Dépôt :**
   - Cliquez sur l’onglet **Settings** dans votre dépôt.

3. **Faites Défiler jusqu’à GitHub Pages :**
   - Dans la section **Code and automation**, trouvez le lien **Pages**.

4. **Définir le Domaine Personnalisé :**
   - Dans le champ **Custom domain**, entrez votre nom de domaine (par exemple, `www.votrenom.com`).
   - Assurez-vous que la case **Enforce HTTPS** est cochée. Cela garantira des connexions sécurisées.

5. **Créer un Fichier `CNAME` (Optionnel mais Recommandé) :**
   - Dans le répertoire racine de votre dépôt, créez un fichier nommé `CNAME`.
   - À l’intérieur du fichier `CNAME`, ajoutez votre nom de domaine personnalisé, par exemple :
     ```
     www.votrenom.com
     ```

### Étape 2 : Configurer les Enregistrements DNS sur Namecheap

Maintenant, nous devons configurer les paramètres DNS sur Namecheap pour pointer votre domaine vers GitHub Pages.

1. **Connectez-vous à Namecheap :**
   - Allez sur [namecheap.com](https://www.namecheap.com) et connectez-vous à votre compte.

2. **Accéder à la Liste de Domaines :**
   - Depuis le tableau de bord, cliquez sur **Domain List** dans la barre latérale gauche.
   - Trouvez votre domaine (par exemple, `votrenom.com`) et cliquez sur **Manage**.

3. **Mettre à Jour les Paramètres DNS :**
   - Dans la section **DNS**, réglez **Nameservers** sur **Namecheap Basic DNS** si cela n'est pas déjà fait.

4. **Ajouter les Enregistrements DNS Suivants :**

   - Sous l'onglet **Advanced DNS**, ajoutez les enregistrements suivants :

   | Type d'Enregistrement | Hôte           | Valeur                          | TTL  |
   |-----------------------|----------------|---------------------------------|------|
   | CNAME                 | www            | `username.github.io`            | Automatique |
   | Enregistrement A       | @              | `185.199.108.153`               | Automatique |
   | Enregistrement A       | @              | `185.199.109.153`               | Automatique |
   | Enregistrement A       | @              | `185.199.110.153`               | Automatique |
   | Enregistrement A       | @              | `185.199.111.153`               | Automatique |

   **Explication :**
   - L'enregistrement `CNAME` pointe `www.votrenom.com` vers votre site GitHub Pages.
   - Les enregistrements `A` garantissent que `votrenom.com` (sans `www`) pointe également vers le même site GitHub Pages.

5. **Enregistrer les Modifications** et attendez que les paramètres DNS se propagent. Cela peut prendre de quelques minutes à plusieurs heures.

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
