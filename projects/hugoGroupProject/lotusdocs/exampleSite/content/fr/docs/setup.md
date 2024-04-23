---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Pedro Simoes"
title: "Configuration"
icon: "rocket_launch"
toc: true
description: "Un guide de démarrage rapide pour créer un nouveau contenu dans Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Débutants"]
---

## Exigences

- **git**
- **Go ≥ v1.19**
- **Hugo ≥ v0.100.0** (Version étendue)

## Installer Hugo

Installez la [CLI de Hugo](https://github.com/gohugoio/hugo/releases/latest) en suivant les instructions spécifiques à votre système d'exploitation ci-dessous :

{{< tabs tabTotal="4">}}
{{% tab tabName="Linux" %}}

Le gestionnaire de paquets de votre distribution Linux peut inclure Hugo. Si c'est le cas, installez-le directement à l'aide du gestionnaire de paquets de votre distribution - par exemple, sous Ubuntu, exécutez la commande suivante. Cela installera la version étendue de Hugo :

```shell
sudo apt install hugo
```

{{% /tab %}}
{{% tab tabName="Homebrew (macOS)" %}}

Si vous utilisez le gestionnaire de paquets [Homebrew](https://brew.sh/), exécutez la commande `brew install` dans votre terminal pour installer Hugo :

```shell
brew install hugo
```

{{% /tab %}}
{{% tab tabName="Windows (Chocolatey)" %}}

Si vous utilisez le gestionnaire de paquets [Chocolatey](https://chocolatey.org/), exécutez la commande `choco install` dans votre terminal pour installer Hugo :

```shell
choco install hugo --confirm
```

{{% /tab %}}
{{% tab tabName="Windows (Scoop)" %}}

Si vous utilisez le gestionnaire de paquets [Scoop](https://scoop.sh/), exécutez la commande `scoop install` dans votre terminal pour installer Hugo :

```shell
scoop install hugo
```

{{% /tab %}}
{{< /tabs >}}

### Installation manuelle

Le référentiel GitHub de Hugo contient des versions pré-construites de l'outil en ligne de commande Hugo pour différents systèmes d'exploitation, qui peuvent être trouvées sur la [page des versions](https://github.com/gohugoio/hugo/releases/latest)

Pour plus d'instructions sur l'installation de ces versions, reportez-vous à la [documentation de Hugo](https://gohugo.io/getting-started/installing/)

## Créer un nouveau site Lotus Docs

Avec Hugo installé, créez un nouveau projet Hugo en utilisant la commande `hugo new` :

```shell
hugo new site my-docs-site && cd my-docs-site
```

Initialisez maintenant votre projet en tant que module Hugo en utilisant la commande `hugo mod init` :

```
hugo mod init my-docs-site
```

{{% alert context="info" text="**Remarque**: Si votre site a déjà un dépôt git, vous pouvez initialiser votre site en utilisant le chemin vers le dépôt git de votre site, par exemple`hugo mod init github.com/<utilisateur>/<my-docs-site>/`." /%}}

Vous pouvez maintenant choisir votre méthode préférée pour ajouter le thème Lotus Docs à votre nouveau site parmi les options ci-dessous:

{{< tabs tabTotal="3">}}
{{% tab tabName="Ajouter en tant que module Hugo" %}}

Modifiez le fichier de configuration `hugo.toml` pour inclure le [thème Lotus Docs](https://github.com/colinwilson/lotusdocs) et le [module Hugo Bootstrap](https://github.com/gohugoio/hugo-mod-bootstrap-scss)  (ligne `5 à 11` ci-dessous):

```toml {linenos=table,hl_lines=["5-11"]}
baseURL = 'http://example.org/'
languageCode = 'fr-fr'
title = 'Mon nouveau site Hugo'

[module]
    [[module.imports]]
        path = "github.com/colinwilson/lotusdocs"
        disable = false
    [[module.imports]]
        path = "github.com/gohugoio/hugo-mod-bootstrap-scss/v5"
        disable = false
```
{{% alert context="info" text="**Remarque**: Hugo ≥ v0.110.0 a changé le nom du fichier de configuration de base par défaut en `hugo.toml`. Si vous utilisez une version antérieure de Hugo, envisagez de renommer votre fichier `config.toml` en `hugo.toml`." /%}}

{{% /tab %}}
{{% tab tabName="Ajouter en tant que sous-module Git" %}}

Initialisez Git et clonez le référentiel du thème Lotus Docs en tant que sous-module :

```shell
git init
git submodule add https://github.com/colinwilson/lotusdocs themes/lotusdocs
```

Mettez à jour votre fichier de configuration `hugo.toml` existant avec la configuration ci-dessous :

```toml {linenos=table,hl_lines=["5-11"]}
baseURL = 'http://example.org/'
languageCode = 'fr-fr'
title = 'Mon nouveau site Hugo'

[module]
    [[module.imports]]
        path = "lotusdocs"
        disable = false
    [[module.imports]]
        path = "github.com/gohugoio/hugo-mod-bootstrap-scss/v5"
        disable = false
```

{{% alert context="info" text="**Remarque**: Hugo ≥ v0.110.0 a changé le nom du fichier de configuration de base par défaut en `hugo.toml`. Si vous utilisez une version antérieure de Hugo, envisagez de renommer votre fichier `config.toml` en `hugo.toml`." /%}}

{{% /tab %}}
{{% tab tabName="Cloner les fichiers du thème" %}}

Dans les cas où vous préférez personnaliser et maintenir vous-même le thème Lotus Docs, vous pouvez cloner le thème dans le sous-répertoire `themes` de votre projet.

Exécutez la commande suivante depuis le répertoire racine de votre projet pour cloner le thème Lotus Docs dans votre sous-répertoire `themes`:

```shell
git clone https://github.com/colinwilson/lotusdocs themes/lotusdocs
```

Modifiez le fichier de configuration `hugo.toml` pour inclure le thème Lotus Docs et le module Hugo Bootstrap (lignes `5 à 11` ci-dessous) :

```toml {linenos=table,hl_lines=["5-11"]}
baseURL = 'http://example.org/'
languageCode = 'fr-fr'
title = 'Mon nouveau site Hugo'

[module]
    [[module.imports]]
        path = "lotusdocs"
        disable = false
    [[module.imports]]
        path = "github.com/gohugoio/hugo-mod-bootstrap-scss/v5"
        disable = false
```
{{< alert context="info" text="**Remarque**: Hugo ≥ v0.110.0 a changé le nom du fichier de configuration de base par défaut en `hugo.toml`. Si vous utilisez une version antérieure de Hugo, envisagez de renommer votre fichier `config.toml` en `hugo.toml`." />}}

{{% /tab %}}
{{< /tabs >}}

## Créer un nouveau contenu

Accédez à la racine de votre projet Hugo et utilisez la commande `hugo new` pour créer un fichier dans le répertoire `content/docs`:

```shell
hugo new docs/example-page.md
```

Cela créera un fichier markdown nommé `page-exemple.md` avec la frontière par défaut suivante :

```toml
+++
title = "Page Exemple"
description = ""
icon = "article"
date = "2023-05-22T00:27:57+01:00"
lastmod = "2023-05-22T00:27:57+01:00"
draft = false
toc = true
weight = 999
+++
```

Modifiez les options selon vos besoins.

Le code ci-dessous montre le code de la frontière utilisé pour créer cette page, ainsi qu'une partie du markdown du corps :

{{< prism lang="md" >}}
+++
weight = 100
date = "2023-05-03T22:37:22+01:00"
draft = true
author = "Colin Wilson"
title = "Démarrage rapide"
icon = "rocket_launch"
toc = true
description = "Un guide de démarrage rapide pour créer un nouveau contenu dans Lotus Docs"
publishdate = "2023-05-03T22:37:22+01:00"
tags = ["Débutants"]
+++

## Créer un nouveau contenu

Accédez à la racine de votre projet Hugo et utilisez la commande `hugo new` pour créer un fichier dans le répertoire `content/docs`:

```shell
hugo new docs/examplepage.md
```
...
{{< /prism >}}

## Prévisualisez votre site

Maintenant que vous avez créé un contenu d'exemple, vous pouvez prévisualiser votre nouveau site Lotus Docs en utilisant la commande `hugo server`:

```shell
hugo server -D
```

Accédez à `localhost:1313/docs` et vous devriez voir un lien de carte vers la **Page Exemple** créée précédemment :

![New Lotus Docs Site - Example Content](https://res.cloudinary.com/lotuslabs/image/upload/v1690992310/Lotus%20Docs/images/lotus_docs_new_site_and_content_module_setup_oiuyex.png)

## Ordre du contenu

Lotus Docs utilise une méthode de pondération simple pour ordonner le contenu et créer des menus.

La variable `weight` de la frontière est utilisée pour ordonner tout le contenu et générer automatiquement la structure du menu (y compris le menu latéral et les boutons de navigation de page). Les valeurs de poids inférieures ont une priorité plus élevée. Ainsi, le contenu avec des poids inférieurs vient en premier et est ainsi ordonné dans le menu.

## Menu auto-généré

Comme mentionné précédemment, Lotus Docs génère automatiquement des menus et des liens de navigation en utilisant la variable de poids [front matter](https://gohugo.io/content-management/front-matter/#predefined). Par exemple, accédez au répertoire `content/docs` et créez deux fichiers de contenu, `doc-one.md` et `doc-two.md`, puis modifiez les valeurs de poids respectivement à `100` et `200`:

{{< alert text="Il est recommandé d'augmenter le poids de vos articles d'un facteur de <code>100</code>. Cela garantit suffisamment d'espace pour insérer de nouveaux articles entre les éléments existants si nécessaire." />}}

Votre structure de répertoire devrait maintenant ressembler à ceci:

```treeview
content/
└── docs/
    ├── doc-one.md
    └── doc-two.md
```

Les liens vers les deux articles sont désormais visibles dans le menu latéral où `doc-one.md` viendra avant et sera placé au-dessus de `doc-two.md`:

![sidebar menu items example](https://res.cloudinary.com/lotuslabs/image/upload/v1684719173/Lotus%20Docs/images/sidebar_menu_example_01-modified_qkb2si.png)

{{< alert context="info" text="L'option de configurer manuellement une structure de menu prédéfinie dans <code>hugo.toml</code> au lieu d'une auto-générée fait partie de la feuille de route de Lotus Docs." />}}

## Éléments de menu de deuxième niveau

Les éléments de menu de deuxième niveau peuvent être générés en créant d'abord un **répertoire parent** contenant un fichier `_index.md`, par exemple:

```shell
hugo new docs/parent-directory/_index.md
```

La commande ci-dessus crée un fichier `_index.md` à l'intérieur d'un répertoire nommé `repertoire-parent` sous `content/docs`:

```treeview
content/
└── docs/
    ├── parent-directory/
    │   └── _index.md
    ├── doc-one.md
    ├── doc-two.md
    └── _index.md
```

Vous pouvez maintenant créer des éléments de deuxième niveau à l'intérieur du `repertoire-parent` comme d'habitude. Exécutez à nouveau la commande `hugo new` pour créer un article à l'intérieur du `repertoire-parent` nouvellement créé :

```shell
hugo new docs/parent-directory/doc-three.md
```

Votre structure de répertoire/fichier devrait maintenant ressembler à ceci :

```treeview
content/
└── docs/
    ├── parent-directory/
    │   ├── _index.md
    │   └── doc-three.md
    ├── doc-one.md
    ├── doc-two.md
    └── _index.md
```

Cela se reflète dans le menu latéral avec `repertoire-parent` fonctionnant comme un menu déroulant contenant un lien vers l'article **Doc Trois**:

![sidebar parent menu example](https://res.cloudinary.com/lotuslabs/image/upload/v1684802032/Lotus%20Docs/images/sidebar_menu_example_02_jsecye.png)