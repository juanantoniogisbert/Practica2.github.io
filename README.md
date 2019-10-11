### Paso 1

Orginalmente cuando creamos un repositorio en GitHub se crea automaticamente la rama master, ahora vamos a crear la rama `develop`.

```markdown
$ git branch develop
```
Para mostras las ramas hacemos el siguiente comando:

```markdown
$ git branch -a
```
Una vez tengamos la ramas creadas las vamos a subir en remoto a nuestro repositorio.

```markdown
$ git push origin develop
```

### Paso 2

En este paso vamos a crear las ramas `feature1, feature2` con los siguientes comandos

```markdown
$ git branch feature1
$ git branch feature2
```
Para mostras la ramas hacemos el siguiente comando:

```markdown
$ git branch -a
```
Una vez tengamos la ramas creadas las vamos a subir en remoto a nuestro repositorio.

```markdown
$ git push origin feature1
$ git push origin feature2
```




















```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/juanantoniogisbert/Practica2.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
