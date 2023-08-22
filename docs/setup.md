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
> para estudiantes de [GitHub Student Developer Pack][GSDP].

[GSDP]: https://education.github.com/discount_requests/application

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

#### HTTP

HTTP utiliza un sistema de tokens para autenticar a los usuarios.
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

#### GitHub cli

GitHub cli es una herramienta propia de GitHub que te permite
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

<!-- TODO -->

## Como comprobar que todo funciona

<!-- TODO -->
