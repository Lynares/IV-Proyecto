### Creación de par de claves y subida de clave a GitHub

Lo primero que tendremos que hacer será crear un par de claves SSH, para que el proceso de subida de archivos sea menos laborioso.
Lo primero será generar una nueva clave SSH, para ello vamos a usar ha hacer lo siguiente:

`ssh-keygen -t rsa -b 4096 -C "alvarlinares@gmail.com"`

Ahora mediante xclip copiaremos la clave pública, para añadirla a GitHub:

`xclip -sel clip < ~/.ssh/id_rsa.pub`

En GitHub nos iremos a Settings -> SSH and GPG keys -> New SSH key, le pondremos un título a la nueva clave y la copiaremos, para terminar click en Add SSH key y nos pedirá nuestra contraseña de usuario.

Todo este proceso se puede ver en:

[Creación de clave SSH](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

[Añadir clave SSH a GitHub](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)


### Configuración de nombre y correo electrónico para que aparezca en los commits

En este caso lo que tendremos que hacer será únicamente usar dos comandos:

Para el nombre: `git config --global user.name "Álvaro Linares"`

Para el correo: `git config --global user.email "alvarlinares@gmail.com"`

### Edición del perfil para que aparezca nombre completo y ciudad, así como universidad

En este caso lo que tendremos que hacer será acceder en GitHub a la parte de "Settings" y allí directamente pondremos nuestro nombre, el email público, la ciudad y para el caso de la universidad en Company pondremos "Universidad de Granada", para finalizar "Update profile" y ya tendremos todo hecho.

### Creación de la rama hito0

En este caso, para no usar la interfaz de GitHub, lo que haremos será crear la rama mediante terminal y después empezar a editar en ella.

Con `git checkout -b hito0` crearemos la rama hito0 y saltaremos a ella, es un atajo a:
~~~
git brach hito0

git checkout hito0
~~~
En esta rama lo que habrá será un archivo llamado hito0.md donde estará localizada toda esta documentación.

### Creación de issues y su cierre correspondiente

Para crear un issue tendremos que hacerlo en GitHub mediante la pestaña issues de nuestro proyecto.

Para hacerle un commit a un issue será:

`git commit -m "Commit a \#1"`

Para cerrar un issue haremos:

`git commit -m "comentario close \#1 "`
