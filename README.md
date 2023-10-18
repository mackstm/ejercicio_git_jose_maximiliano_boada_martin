<div align="justify">

# Examen Práctico Git

## Enlace a repositorio

https://github.com/mackstm/ejercicio_git_jose_maximiliano_boada_martin

## Índice

- [Inicio](#index01)
- [Rama develop](#index02)
- [Merge de ramas](#index03)
- [Mostrar cambios realizados](#index04)
- [Crear tags](#index05)
- [Crear la rama feature-2](#index06)
- [Merge final](#index07)
- [Crear el tag v.2](#index08)
- [Mostrar cambios y commits](#index09)

## Inicio <a name="index01"></a>

- Clonar repositorio.
- Añadir fichero README.md.
- Hacer commit.

<details> <summary>Pulse para ver los pasos</summary>

- __git clone git@github.com:mackstm/ejercicio_git_jose_maximiliano_boada_martin.git__
- __cd ejercicio_git_jose_maximiliano_boada_martin__
- __touch README.md__
- __git add .__
- __git commit -m "añadido README.md"__

<details> <summary>Salida:</summary>

```console
[master (commit-raíz) c6792c8] añadido README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
```

</details>

</details>

## Rama develop <a name="index02"></a>

- Crear una rama con nombre develop.
- Lista las ramas actuales.

<details> <summary>Pulse para ver los pasos</summary>

- __git branch develop__
- __git branch__

Salida:

```console
  develop
* master
```

</details>

## Merge de ramas <a name="index03"></a>

- Moverse a la rama y crear el fichero: _hola.html_. Añadir el siguiente contenido:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
<title>Hola </title>
</head>
<body>
<h1 align="center" >Hola soy un título </h1>
<hr>
<p> Hola soy el alumno Maxi </p>
</body>
</html>
```

- Moverse a la rama principal y crear el fichero _adios.html_. Añadir el siguiente contenido:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
<title>Adios </title>
</head>
<body>
<h1 align="center" >Adios soy un título </h1>
<hr>
<p> Adios soy el alumno Maxi </p>
</body>
</html>
```

- Crea el commit con un mensaje descriptivo.
- Sube los cambios a la rama actual.
- Lista las ramas actuales.

<details> <summary>Pulse para ver los pasos</summary>

- __git checkout develop__
- __vi hola.html__
- Pegar contenido
- Guardar y salir de vi con __:wq__
- __git checkout master__
- __vi adios.html__
- Pegar contenido
- Guardar y salir de vi con __:wq__
- __git add .__
- __git commit -m "Añadidos hola.html en develop y adios.html en master"__

<details> <summary>Salida:</summary>

```console
[master 32bb231] Añadidos hola.html en develop y adios.html en master
 2 files changed, 22 insertions(+)
 create mode 100644 adios.html
 create mode 100644 hola.html
```

</details>

- __git push origin master__

<details> <summary>Salida:</summary>

```console
Enumerando objetos: 7, listo.
Contando objetos: 100% (7/7), listo.
Compresión delta usando hasta 12 hilos
Comprimiendo objetos: 100% (5/5), listo.
Escribiendo objetos: 100% (7/7), 749 bytes | 749.00 KiB/s, listo.
Total 7 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:mackstm/ejercicio_git_jose_maximiliano_boada_martin.git
 * [new branch]      master -> master
```

</details>

- __git branch__

Salida:

```console
  develop
* master
```

</details>

## Mostrar cambios realizados <a name="index04"></a>

- Muestra todos los cambios realizados.
- Lista ahora los últimos cambios que se han producido en el repositorio, es decir, los últimos commits que han realizado en el repositorio.

<details> <summary>Pulse para ver los pasos</summary>

- __git log__

<details> <summary>Salida:</summary>

```console
commit 32bb231c92973e6077af5211e43ca678cddff74c (HEAD -> master, origin/master)
Author: mackstm <thelewyntm@gmail.com>
Date:   Wed Oct 18 15:13:44 2023 +0100

    Añadidos hola.html en develop y adios.html en master

commit c6792c804cbd6f3dfc6ed7811a49b0e7bcb24529 (develop)
Author: mackstm <thelewyntm@gmail.com>
Date:   Wed Oct 18 14:52:52 2023 +0100

    añadido README.md
```

</details>

- __git log -n 1__

<details> <summary>Salida:</summary>

```console
commit 32bb231c92973e6077af5211e43ca678cddff74c (HEAD -> master, origin/master)
Author: mackstm <thelewyntm@gmail.com>
Date:   Wed Oct 18 15:13:44 2023 +0100

    Añadidos hola.html en develop y adios.html en master
```

</details>

</details>

## Crear tags <a name="index05"></a>

- Lista todos los tags(etiquetas que existan).
- Crea una nueva etiqueta (tag) de nombre v.1 y sube los cambios.

<details> <summary>Pulse para ver los pasos</summary>

- __git tag__
- No tendrá salida puesto que aún no hemos creado ningún tag.
- __git tag v.1__
- __git tag__

Salida:

```console
v.1
```

</details>

## Crear la rama feature-2 <a name="index06"></a>

- Crea la rama feature-2 y muévete a esta.

<details> <summary>Pulse para ver los pasos</summary>

- __git checkout -b feature-2__

</details>

## Merge final <a name="index07"></a>

- Crea el archivo _Estamos_a_punto_de_terminar.html_, con el siguiente contenido:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
<title>Terminando </title>
</head>
<body>
<h1 align="center" >Apunto de terminar </h1>
<hr>
<p> Esto se esta acabando Maxi </p>
</body>
</html>
```

- Realiza el commit y sube los cambios.
- Muevete a la rama develop, y realiza la mezcla con la rama feature-2.
- Sube los cambios de la rama develop a Github.
- Cambia a la rama principal, realiza la mezcla con la rama develop.

<details> <summary>Pulse para ver los pasos</summary>

- __vi Estamos_a_punto_de_terminar.html__
- Guardar y salir de vi con __:wq__
- __git add .__
- __git commit -m "añadido Estamos_a_punto_de_terminar.html"__

<details> <summary>Salida:</summary>

```console
[feature-2 fcda78d] añadido Estamos_a_punto_de_terminar.html
 1 file changed, 11 insertions(+)
 create mode 100644 Estamos_a_punto_de_terminar.html
```

</details>

- __git checkout develop__
- __git merge feature-2__

<details> <summary>Salida:</summary>

```console
Actualizando c6792c8..fcda78d
Fast-forward
 Estamos_a_punto_de_terminar.html | 11 +++++++++++
 adios.html                       | 11 +++++++++++
 hola.html                        | 11 +++++++++++
 3 files changed, 33 insertions(+)
 create mode 100644 Estamos_a_punto_de_terminar.html
 create mode 100644 adios.html
 create mode 100644 hola.html
```

</details>

- __git push origin develop__

<details> <summary>Salida:</summary>

```console
Enumerando objetos: 4, listo.
Contando objetos: 100% (4/4), listo.
Compresión delta usando hasta 12 hilos
Comprimiendo objetos: 100% (3/3), listo.
Escribiendo objetos: 100% (3/3), 570 bytes | 570.00 KiB/s, listo.
Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
remote: 
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/mackstm/ejercicio_git_jose_maximiliano_boada_martin/pull/new/develop
remote: 
To github.com:mackstm/ejercicio_git_jose_maximiliano_boada_martin.git
 * [new branch]      develop -> develop
```

</details>

- __git checkout master__
- __git merge develop__

<details> <summary>Salida:</summary>

```console
Actualizando 32bb231..fcda78d
Fast-forward
 Estamos_a_punto_de_terminar.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 Estamos_a_punto_de_terminar.html
```

</details>

</details>

## Crear el tag v.2 <a name="index08"></a>

- Realiza el tag con el nombre v.2.

<details> <summary>Pulse para ver los pasos</summary>

- __git tag v.2__

</details>

## Mostrar cambios y commits <a name="index09"></a>

- Muestra todos los cambios realizados en el repositorio.
- Muestra todos los commits realizados.

<details> <summary>Pulse para ver los pasos</summary>

- __git status__

Salida:

```console
En la rama master
Tu rama está actualizada con 'origin/master'.

nada para hacer commit, el árbol de trabajo está limpio
```

- __git log__

<details> <summary>Salida:</summary>

```console
commit fcda78d7da3b5e45de1560fc84be7558298781b4 (HEAD -> master, tag: v.2, origin/master, origin/develop, feature-2, develop)
Author: mackstm <thelewyntm@gmail.com>
Date:   Wed Oct 18 15:43:16 2023 +0100

    añadido Estamos_a_punto_de_terminar.html

commit 32bb231c92973e6077af5211e43ca678cddff74c (tag: v.1)
Author: mackstm <thelewyntm@gmail.com>
Date:   Wed Oct 18 15:13:44 2023 +0100

    Añadidos hola.html en develop y adios.html en master

commit c6792c804cbd6f3dfc6ed7811a49b0e7bcb24529
Author: mackstm <thelewyntm@gmail.com>
Date:   Wed Oct 18 14:52:52 2023 +0100

    añadido README.md
```

</details>

</details>

</div>