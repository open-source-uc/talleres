# Taller de Git y GitHub
## Sesión 1
### Introducción

- **Control de versiones**: ¿Para qué usar uno?

- **Git como control de versiones distribuido (DVCSs)**:  
![DVCSs](https://git-scm.com/book/en/v2/images/distributed.png)

- **Fundamentos de Git**: Local, distribuido y el principio de solo añadir datos.

- **Los tres estados**: Directorio de trabajo, staging y el repositorio.

![los tres estados](https://git-scm.com/book/en/v2/images/areas.png)

- **Workflow básico de git**: Modificar, agregar a staging, confirmar los cambios (commitear).

- **Interfaces a Git:** La línea de comandos, interfaces gráficas (GitHub Desktop, GitKraken, VSCode).

- **¿Cómo instalar git?**: macOS (Homebrew), Windows (GitHub Desktop? Git bash?), Linux (apt/pacman). ¿GitHub CLI?

- **Configuración Inicial**: Nombre, mail, editor, nombre de branch (main).

```shell
$ git config --global user.name "Ignacio Sánchez"
$ git config --global user.email rectoria@uc.cl
$ git config --global init.defaultBranch main
$ git config --global core.editor code
```

- **¿Cómo conseguir ayuda?**: Documentación de git, `git help` StackOverflow es tu amigo (con cuidado!)

### Empezando a trabajar

- **Crear y obtener un repositorio**: ¿Cómo crear un repositorio (`git init` o GitHub)? ¿Cómo clonar un repositorio (`git clone` o `gh repo clone`)? Autenticación.

- **Grabar cambios**: Archivos rastreados y no rastreados, staging, `git status` y tu primer commit. `git rm` para quitar archivos de staging.

- **Ver la historia**: `git log`

- **Deshacer y arreglar cosas**: `git commit --ammend` (pre-pull) y con ayuda de `git status`: `git reset HEAD`, `git restore`.

- **Sincronizando cambios**: `git push` y `git pull`, revisar historial de cambios.

- **Resumen**: Cheatsheet de comandos básicos, workflow completo.

## Sesión 2 (Git avanzado)
### Funcionamiento de Git
- **Historial como un árbol**: Como git almacena los cambios.

- **Branches**: ¿Para qué sirven? ¿Cómo funcionan (árbol)? 

![Branches](https://git-scm.com/book/en/v2/images/advance-testing.png)

- **Trabajando con branches**: Branch y merge, divergencia de historiales, conflictos de merge.

![Divergencia](https://git-scm.com/book/en/v2/images/basic-merging-1.png)

- **Workflows con branches**: Branches de producción, feature branches, pull requests.

- **¿Rebasing como alternativa a merge?**: Rebases simples, opciones de merge en PRs.

- **Resumen de branches**

### Reescribir la historia

- **Beneficios y riesgos de reescribir la historia**

- **Repaso de Ammend**

- **Rebase**: Uso de rebase interactivo para limpieza de historiales, extracción de cambios y squashing.

### Herramientas avanzadas

- **Stashing**: ¿Cómo guardamos cambios temporales? `git stash`

- **Búsqueda**: `git grep`.

