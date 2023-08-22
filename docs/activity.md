# Actividad

## Crear un repositorio de GitHub

Primero deberás crear un repositorio en GitHub para que puedas subir
lo que realices en esta actividad. Puedes crear un nuevo repositorio
[en este link](https://github.com/new/) o en el botón <kbd>+</kbd>
de arriba a la derecha.

Asegúrate que el repositorio sea público. No añadas un `README.md` ni
un `.gitignore` por ahora.

## Clonar o abrir el repositorio

Si estás corriendo Git localmente:
1. Crea un repositorio localmente con `git init`.
2. Añade un archivo `README.md` con el contenido que quieras.
3. Commitéalo con `git add README.md` y `git commit -m "..."`.
4. Súbelo a GitHub con `git remote add origin <url>` y `git push -u origin master`. 

Si vas a usar GitHub Codespaces:
1. Puede salir arriba a la izquierda o arriba a la derecha en
   <kbd><> Code</kbd>, pestaña Codespaces. Esto podrá crear un archivo
   `README.md` por ti.
2. Modifica o crea el archivo `README.md` con el contenido que quieras.
3. Súbelo a GitHub con `git push`.

## Crear una rama, hacer cambios y commitearlos

1. Crea una branch y cámbiate a ella con `git switch -c <nombre>`.
2. Copia el archivo [HTML de este repositorio](../src/index.html).
4. Pega el archivo en tu repositorio, en la raíz del directorio.
5. Cambia “mundo” por tu nombre.
6. Commitéalo con `git add index.html` y `git commit -m "..."`.
7. Pushéalo con `git push -u origin <nombre>`.
8. Anda a la rama principal con `git switch main`.
9. Mergea los cambios con `git merge <nombre>`.
10. Pushéalo con `git push`.

> Nota: Se usa `git push -u origin <nombre>` solo la primera vez
> que se sube una rama. Después se puede usar `git push`.

## Opcional: ¡Deja tu página pública!

1. Ve a la página del repositorio, en la pestaña <kbd>Settings</kbd>.
2. Anda a la sección <kbd>Pages</kbd>.
3. Selecciona Source Deploy from a branch, selecciona la rama principal
   (`main`) y la carpeta raíz (`/ (root)`). Aprieta guardar.

Ahora tu repositorio debería estar disponible en

```text
https://<tu-usuario>.github.io/<tu-repositorio>
```

## Forkear un repositorio

1. Ve a la página de un repositorio de otra persona que está
   realizando esta misma actividad.
2. A la derecha del nombre del repositorio, aprieta el botón <kbd>Fork</kbd>.
3. Crea un fork. Puede ser que sea necesario cambiar el nombre del repositorio,
   no hay problema en eso.
4. Clona el repositorio en tu computador o ábrelo en GitHub Codespaces.
5. Crea una rama para hacer los cambios.

## Añade confeti al repositorio forkeado

1. Busca como añadir confeti a una página web. (Hint: Busca “confetti
   js github” en Google). **Es un desafío que puedas leer la
   documentación de una librería y usarla**. (Otro hint: busca 
   código que use `<script src="..." ></script>` y luego cree una
   instancia para confeti).
2. Añade los cambios a la rama y pushealos.
3. Ve a la página del repositorio forkeado, tab <kbd>Pull request</kbd>,
   y crea una PR que se dirija al repositorio original en su rama
   principal desde el repositorio forkeado en tu rama.

## Acepta la PR de otra persona

1. Ve a la página de tu repositorio, tab <kbd>Pull request</kbd>.
2. Abre la PR que te enviaron.
3. Ve los cambios y has click en <kbd>Merge pull request</kbd>.
