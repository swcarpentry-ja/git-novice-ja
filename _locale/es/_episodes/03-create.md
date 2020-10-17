---
title: Creando un repositorio
teaching: 10
exercises: 0
questions:
- "¿Dónde almacena Git la información?"
objectives:
- "Crear un repositorio local de Git."
keypoints:
- "`git init` inicializa un repositorio."
---

Una vez que Git está configurado,
podemos comenzar a usarlo.

Vamos a crear un directorio para nuestro trabajo y nos movemos dentro de ese directorio:

~~~
$ mkdir planets
$ cd planets
~~~
{: .language-bash}

Después le indicamos a Git hacer de `planets` un [repository]({{ page.root }}/reference/#repository)— un lugar donde
Git puede almacenar las versiones de nuestros archivos:

~~~
$ git init
~~~
{: .language-bash}

Si usamos `ls` para mostrar el contenido del directorio,
parece que nada ha cambiado:

~~~
$ ls
~~~
{: .language-bash}

Pero si agregamos la flag `-a` para mostrar todo,
podemos ver que Git ha creado un directorio oculto dentro de `planets` llamado `.git`:

~~~
$ ls -a
~~~
{: .language-bash}

~~~
.\t..\t.git
~~~
{: .output}

Git utiliza este subdirectorio especial para almacenar toda la información del proyecto, incluyendo todos los archivos y subdirectorios. Si alguna vez borramos el directorio `.git`,
perderemos la historia del proyecto.

Podemos revisar que todo esté configurado correctamente
pidiendo a Git que nos informe el estado de nuestro proyecto:

~~~
$ git status
~~~
{: .language-bash}

Si estás utilizando una versión de git distinta a la que yo utilizo, el output puede ser ligeramente distinto. 

~~~
# On branch master
#
# Initial commit
#
nothing to commit (create/copy files and use "git add" to track)
~~~
{: .output}

> ## Lugares para crear un repositorio Git
> {: .solution}












































> {: .solution}
{: .challenge}

> ## Corrigiendo errores de `git init`
> ドラえもん le explica a のび太 cómo un repositorio anidado es redudante y puede causar problemas ms adelante.
> のび太 quiere eliminar el repositorio anidado.
> Cómo puede のび太 deshacer el último `git init` en el sub-directorio `moons`?
>
> > ## Solución - USAR CON CUIDADO!
> >
> > Para deshacerse de este pequeño error, のび太 puede simplemente eliminar el directorio `.git`
> > del subdirectorio `moons`. Para ello puede ejecutar el siguiente comando desde el interior del directorio `moons`:
> >
> > ~~~
> > $ rm -rf moons/.git
> > ~~~
> > {: .language-bash}
> >
> > ¡Pero ten cuidado! Ejecutar este comando en el directorio incorrecto eliminará
> > toda la historia git de un proyecto que podrías querer conservar. 
> > Por lo tanto, revisa siempre tu directorio actual usando el comando `pwd`.
> {: .solution}
{: .challenge}

