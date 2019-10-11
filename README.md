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

En este paso vamos a crear las ramas `feature1, feature2` desde la rama `develop` con los siguientes comandos

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

Ahora accederos a `feature1` y crearemos un fichero y lo modicaremos.

```markdown
$ git checkout feature1
$ touch fichero.txt
```

Una vez modificado este fichero lo subimos al repositorio remoto:

```markdown
$ git commit -m "modificacion en feature1"
$ git push -u origin feature1
```

Ahora realizaremos lo mismo pero en la `feature2`. Una vez realizo los comandos experimentaremos con un error entre features.

### Paso 3

En este paso lo que vamos a hacer es solucionar el conficto, utilizamos los siguientes comandos:

```markdown
$ git checkout develop
$ git merge feature1
$ git merge feature2
```

Una vez solucionado el conficto pasamos al siguiente paso.

### Paso 4

Vamos a subir los cambios con una etiqueta anotada:

```markdown
$ git add fichero.txt
$ git commit -m "Conflictos solucionados"
$ git push origin develop
$ git tag -a TagAnotada -m "Modificacion de las features"
$ git push origin develop --tags
```

Ahora vamos a pasarlo todo la rama master y subirlo a nuestro repositorio remoto

```markdown
$ git checkout master
$ git merge develop
$ git push origin master
```
Nos encotraremos con un error en la rama master para ello utilizaremos un hotfix para solucionarlo.

```markdown
$ git checkout -b hotfix1
$ git commit -m "Error en rama master"
```
Para tener nuestra aplicacion actualizada hacemos los siguientes comandos:

```markdown
$ git checkout develop
$ git merge hotfix1 
$ git push origin develop
$ git checkout master
$ git merge hotfix1
$ git push origin master
```
