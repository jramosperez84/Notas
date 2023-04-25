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

```bash
mkdir mi-repositorio
cd mi-repositorio
git init
```

2. Crea un archivo y agrega algunos cambios:

```bash
echo "Hola, mundo" > archivo.txt
git add archivo.txt
```

Esto crea un nuevo archivo llamado `archivo.txt` y lo agrega al área de preparación.

3. Confirma los cambios:

```bash
git commit -m "Agregado archivo.txt"
```

Esto confirma los cambios en el repositorio local con el mensaje "Agregado archivo.txt".

4. Agrega más cambios al archivo:

```bash
echo "Este es un archivo de ejemplo" >> archivo.txt
git add archivo.txt
```

Esto agrega más cambios al archivo `archivo.txt` y lo vuelve a agregar al área de preparación.

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

## Conflictos en un repositorio local:

Supongamos que tienes un archivo llamado `archivo.txt` en tu repositorio local y dos colaboradores diferentes han realizado cambios en diferentes partes del archivo y han confirmado sus cambios. Cuando intentas fusionar los cambios en tu rama local, Git detecta un conflicto de merge. Para solucionarlo, sigue estos pasos:

1.  Actualiza tu repositorio local con los cambios remotos:

```bash
git fetch origin
```

Esto descarga los cambios remotos en tu repositorio local, pero no los fusiona con tus cambios locales.

2.  Cambia a la rama que quieres fusionar:

```bash
git checkout mi-rama
```

Esto cambia a la rama en la que estás trabajando y que quieres fusionar con los cambios remotos.

3.  Fusiona los cambios remotos en tu rama local:

```bash
git merge origin/mi-rama
```

Esto fusiona los cambios remotos en tu rama local. Si Git detecta un conflicto de merge, mostrará un mensaje indicándote que hay conflictos.

4.  Abre el archivo en conflicto:

```bash
git mergetool archivo.txt
```

Esto abre una herramienta de fusión de conflictos para que puedas ver y editar los cambios en conflicto. La herramienta de fusión dependerá de la configuración de tu sistema.

5. Resuelve los conflictos manualmente:
	Edite el archivo en conflicto y elimine los conflictos manualmente. Los conflictos se indicarán con marcadores especiales, como `<<<<<<<`, `=======` y `>>>>>>>`.
6. Agrega el archivo en conflicto al área de preparación:

```bash
git add archivo.txt
```

Esto agrega el archivo en conflicto resuelto al área de preparación.

7.  Confirma los cambios resueltos:

```bash
git commit -m "Solucionado conflicto en archivo.txt"
```

Esto confirma los cambios resueltos con un mensaje indicando que el conflicto se ha solucionado.

8.  Continúa con la fusión:

```bash
git merge origin/mi-rama
```

Esto continúa con la fusión y, si no hay más conflictos, Git fusionará los cambios remotos en tu rama local.

9.  Sube los cambios al repositorio remoto:

```bash
git push origin mi-rama
```

Esto sube los cambios de tu rama local al repositorio remoto.