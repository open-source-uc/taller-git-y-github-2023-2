# Setup necesario

Para el taller es necesario que puedas interactuar en GitHub
utilizando Git. Para esto es necesario que tengas 2 cosas:

- Una cuenta en GitHub
- Una manera de correr Git

A continuación te explicamos como hacerlo, y más abajo podrás
ver como probar que todo funciona.

> ❗ Importante: Aquí se asume que conoces que es un terminal y como
> correr los comandos que se muestran.

## Crear una cuenta en GitHub

GitHub es una plataforma para trabajar y compartir código.
Puedes crearte una cuenta en [github.com](https://github.com/signup).

> 💡 ProTip: Luego de crear tu cuenta, puedes solicitar beneficios
> para estudiantes del [GitHub Student Developer Pack][GSDP].

[GSDP]: https://education.github.com/benefits?utm_source=2023-08-24-Git&GitHubWorkshopUC

## Utilizar Git

Git es un programa para controlar las versiones de código y otros
archivos de texto plano. En el taller se explicará su funcionamiento.

Para poder probarlo durante el taller, tienes 2 opciones:

- Configurar Git en tu computador
- Utilizar GitHub Codespaces para correr Git en la nube

### Configurar Git en tu computador


#### Instalar Git

> Puedes leer la sección 1.5 y 1.6 del libro [Pro Git][progit] que
> entra en más detalles sobre la instalación de Git.

01. [Instala Git](https://git-scm.com/downloads)
02. Configura tu nombre, correo, editor y rama por defecto:
    ```bash
    # TU nombre y mail
    git config --global user.name "Tu nombre"
    git config --global user.email tu-mail@example.com

    # El editor que se abrirá en ciertas situaciones
    git config --global core.editor code  # por ejemplo vscode
  
    # La rama por defecto
    git config --global init.defaultBranch main
    ```

[progit]: https://git-scm.com/book/en/v2

### Vincular la cuenta de GitHub con Git

Uno puede vincularse a GitHub de 3 maneras: HTTPS, SSH y GitHub cli.

#### HTTPS

HTTPS utiliza un sistema de tokens para autenticar a los usuarios.
Para clonar este repositorio por HTTPS, se usa:

```bash
git clone https://github.com/open-source-uc/taller-git-y-github-2023-2.git
```

Uno puede clonar un repositorio público utilizando HTTPS sin ingresar
ninguna credencial, pero al momento de querer subir cambios o clonar
un repositorio privado, deberás usar credenciales para autenticarte.

> ❗ Importante: GitHub no pedirá tu contraseña, sino que te pedirá
> que ingreses un token.

Puedes crear e ingresar un token cada vez que lo necesites, pero es más
conveniente instalar [Git Credential Manager][gcm] para que maneje la 
autentificación por ti. Viene instalado por defecto en Windows, en macOS
y Linux puedes instalarlo siguiendo [estas instrucciones][gcm-install].

[gcm]: https://github.com/git-ecosystem/git-credential-manager
[gcm-install]: https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md


#### SSH

SSH utiliza un sistema de llaves para autenticar a los usuarios.
Para clonar este repositorio por SSH, se usa:

```bash
git clone git@github.com:open-source-uc/taller-git-y-github-2023-2.git
```

No vamos a entrar en detalle sobre SSH aquí, pero puedes aprender
sobre como se usa leyendo la sección 4.3 y 6.1 de [Pro Git][progit],
la documentación de GitHub sobre [SSH][ssh-github] y la guía de
BenjaVicente [sobre SSH][ssh-benja].

[ssh-github]: https://docs.github.com/es/authentication/connecting-to-github-with-ssh
[ssh-benja]: https://gist.github.com/benjavicente/7614dd15ee6046355909d5e21a23dde6

#### GitHub CLI

GitHub CLI es una herramienta propia de GitHub que te permite
interactuar con GitHub desde la terminal. Puedes instalarla en su
[página principal][gh-cli] y configurarlo siguiendo las instrucciones
de [su manual][gh-cli-manual], que se resumen en correr:

```bash
gh auth login
```

Luego podrás clonar este repositorio con:

```bash
gh repo clone open-source-uc/taller-git-y-github-2023-2
```

[gh-cli]: https://cli.github.com/
[gh-cli-manual]: https://cli.github.com/manual/

### Utilizar GitHub Codespaces
GitHub Codespaces es un entorno de desarrollo instantáneo que corre en la nube para que puedas hacer, básicamente, todo lo que haces en tu IDE, pero en tu buscador ✨ Esto signfica que puedes llevar tu experiencia de VSCode a tu buscador, para así programar en máquinas en la nube más potentes y contenidas.

Para empezar a utilizar GitHub Codespaces -tal como lo indica esta [guía oficial]- puedes hacerlo al crear un nuevo repositorio y se te dará la opción. Igualmente, si quieres utilizar un Codespace en un repositorio ya existente, puedes hacerlo haciendo click en el botón "Code" para clonar un repositorio, ahí podrás ver la opción para utilizar tu Codespace.

![image](https://github.com/open-source-uc/taller-git-y-github-2023-2/assets/81819758/b3d1d80d-989d-42ff-a885-07e15c92e249)

Si deseas aprender más en profunidad en cómo utilizar GitHub Codespaces, puedes hacerlo [acá].

> Pro Tip: ¡Prueba jugar creando un Codespace! 🎏

[guía oficial]: https://docs.github.com/es/codespaces/getting-started/quickstart#introduction
[acá]: https://docs.github.com/es/codespaces/getting-started/deep-dive


## Como comprobar que todo funciona

1. Crea un repositorio en GitHub.
2. Clona el repositorio (`git clone <url>`).
3. Abre el repositorio localmente o en GitHub Codespaces.
4. Edita un archivo.
5. Añade los cambios (`git add . && git commit -m "setup"`)
6. Sube los cambios (`git push`)
7. Ve que los cambios aparecen en GitHub.
