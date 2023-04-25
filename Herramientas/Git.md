## Descripción:

Git es un sistema de control de versiones distribuido de código abierto utilizado para rastrear los cambios en el código fuente durante el proceso de desarrollo de software. Git permite a los desarrolladores trabajar en un proyecto de manera colaborativa y mantener un registro de los cambios realizados por cada miembro del equipo, lo que ayuda a mantener el código organizado y a solucionar problemas de forma eficiente. Además, Git es ampliamente utilizado en el desarrollo de software y es compatible con una gran cantidad de plataformas y herramientas de desarrollo.

## Comandos básicos:

1.  `git init`: Inicializa un nuevo repositorio de Git.
2.  `git clone`: Clona un repositorio existente de Git en una nueva carpeta.
3.  `git add`: Agrega archivos o cambios a la zona de preparación (staging area).
4.  `git commit`: Registra los cambios realizados en la zona de preparación en el repositorio.
5.  `git status`: Muestra el estado actual del repositorio, incluyendo archivos sin seguimiento, cambios pendientes de ser confirmados y otros detalles importantes.
6.  `git log`: Muestra el historial de cambios realizados en el repositorio.
7.  `git branch`: Muestra una lista de ramas (branch) disponibles en el repositorio.
8.  `git checkout`: Cambia entre ramas o versiones del código.
9.  `git merge`: Combina cambios realizados en diferentes ramas.
10.  `git push`: Envía los cambios locales al repositorio remoto.
11.  `git pull`: Descarga y fusiona los cambios remotos en el repositorio local.
12.  `git remote`: Muestra una lista de repositorios remotos configurados en el repositorio local.
13.  `git fetch`: Descarga los cambios remotos al repositorio local sin realizar una fusión.
14.  `git diff`: Muestra las diferencias entre diferentes versiones de un archivo o entre diferentes ramas del repositorio.

Estos son solo algunos de los comandos básicos de Git. Hay muchos más comandos y opciones disponibles en Git, y la documentación oficial de Git proporciona una excelente referencia para cualquier persona interesada en aprender más.

## Ejemplos de uso:

1. Crea un repositorio local:
2. Crea un archivo y agrega algunos cambios:
3. Confirma los cambios:
4. Agrega más cambios al archivo:
5. Confirma los cambios:

```bash
git commit -m "Modificado archivo.txt"
```

Esto confirma los cambios adicionales en el repositorio local con el mensaje "Modificado archivo.txt".

6. Muestra el estado actual del repositorio:

```bash
git status
```

Esto muestra el estado actual del repositorio, incluyendo los cambios pendientes de confirmación.

7. Muestra el historial de cambios:

```bash
git log
```

Esto muestra el historial de cambios en el repositorio.

8. Crea una nueva rama:

```bash
git branch nueva-rama
```

Esto crea una nueva rama llamada `nueva-rama`.

9. Cambia a la nueva rama:

```bash
git checkout nueva-rama
```

Esto cambia a la rama `nueva-rama`.

10. Agrega cambios a la nueva rama:

```bash
echo "Este es un nuevo archivo" > nuevo-archivo.txt
git add nuevo-archivo.txt
git commit -m "Agregado nuevo-archivo.txt"
```

Esto crea un nuevo archivo llamado `nuevo-archivo.txt` y lo agrega al área de preparación en la rama `nueva-rama`.

11. Cambia de vuelta a la rama principal:

```bash
git checkout main
```

Esto cambia de vuelta a la rama principal.

12. Fusiona la rama `nueva-rama` con la rama `main`:

```bash
git merge nueva-rama
```

Esto fusiona los cambios realizados en la rama `nueva-rama` con la rama `main`.

## Crear un repositorio + Alojarlo en Github:

1.  Crea un nuevo repositorio en GitHub:

```bash
curl -u <nombre de usuario> https://api.github.com/user/repos -d '{"name":"<nombre del repositorio>"}'
```

Reemplaza `<nombre de usuario>` con tu nombre de usuario de GitHub y `<nombre del repositorio>` con el nombre que deseas para tu repositorio.

2.  Crea un repositorio local:

```bash
mkdir <nombre del repositorio>
cd <nombre del repositorio>
git init
```

Reemplaza `<url del repositorio en GitHub>` con la URL de tu repositorio en GitHub. Puedes encontrar la URL en la página del repositorio de GitHub.

3.  Agrega y confirma los cambios:

```bash
echo "Hola, mundo" > archivo.txt
git add archivo.txt
git commit -m "Mi primer commit"
```

Esto crea un nuevo archivo llamado `archivo.txt`, lo agrega al área de preparación y luego lo confirma con el mensaje "Mi primer commit".

4.  Sube los cambios al repositorio remoto:

```bash
git push -u origin main
```

Esto sube los cambios del repositorio local al remoto en GitHub en la rama principal (`main`). La opción `-u` establece una conexión entre el repositorio local y el remoto para futuras operaciones de push/pull.