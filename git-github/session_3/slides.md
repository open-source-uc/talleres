---
theme: default
background: https://source.unsplash.com/842ofHC6MaI
# apply any windi css classes to the current slide
class: 'text-center'
# show line numbers in code blocks
lineNumbers: true
# some information about the slides, markdown enabled
info: |
  ## Taller de Git y GitHub
  Hecho por Open Source UC

  Más información en [GitHub](https://github.com/open-source-uc/talleres)

fonts:
  # basically the text
  sans: 'Robot'
  # use with `font-serif` css class from windicss
  serif: 'Robot Slab'
  # for code blocks, inline code, etc.
  mono: 'Fira Code'

colorSchema: 'dark'
---

# Taller de Git y GitHub <mdi-git class="inline"/>

## **Sesión 1: Introducción a Git**
<div class="pt-12">
  <a href="https://osuc.dev/" style="border-style: revert;"> <span class="px-2 py-1 rounded cursor-pointer bg-black bg-opacity-60" hover="bg-opacity-100">
    por Open Source UC <ph:link-simple-duotone class="inline"/>
  </span>
  </a>
</div>

---
layout: section
---

# ¿Qué veremos hoy?

<!--
TODO: legibilidad texto titulo
-->

---

# ¿Qué veremos hoy?

- ¿Qué 🐍❌💀 es git? (Sistema de Control de Versiones)

- Comandos básicos de consola

- Un **flujo de uso** de git local 🏠 y remoto ☁, usando GitHub

- Crear cuenta de github

- Demostración

- Ramificación y espacios de trabajo

- Pull/Merge requests

- Demostración

- Comandos ayuda extra


---
layout: section
---

# ¿Qué 🐍❌💀 es git?

---

# Sistema de Control de Versiones


- 📂 Es un sistema que registra los cambios realizados en un archivo o grupo de archivos con tal de poder recuperar fácilmente versiones antiguas o identificar cambios específicos.

- Nos permite evitar esto:

<br>
<img style="display: block; margin: 0 auto;" src="/old-versiones.png" width="300" />

---

# <mdi-git class="inline"/> git

El sistema de control de versiones mas usado en el mundo!

Git es utilizado por prácticamente todas las compañías de tecnología a nivel mundial, haciendo funcionar todo desde Facebook hasta la NASA.

---

# <mdi-git class="inline"/> git

El sistema de control de versiones mas usado en el mundo!


<img style="display: block; margin: 0 auto;" src="/distribuido_2.png" width="300" />

---

# <mdi-git class="inline"/> git

El sistema de control de versiones mas usado en el mundo!


<img style="display: block; margin: 0 auto;" src="/distribuido.png" width="700" />

---
layout: section

---

# ¿Cómo usamos <mdi-git class="inline" style="color: #a1e3fa"/> git?

---

# ¿Cómo instalamos <mdi-git class="inline"/> git?

Git puede ser instalado de muchas formas distintas; cuál usar depende del contexto y lo que te pidan!


Los links de descarga a la versión oficial de Git se pueden encontrar en [git-scm.com/downloads](https://git-scm.com/downloads).

- <uiw-windows class="inline"/>  En **Windows**, se puede obtener con un installador disponible en la página, que provee una consola de Linux (Git Bash), y con interfaces gráficas como GitHub Desktop.
- <uiw-apple class="inline"/>  En **macOS**, con Homebrew, usando `brew install git`.
- <uiw-linux class="inline"/>  Y en **Linux**, puede encontrarse en la mayoria de los administradores de paquetes, como `apt`, `pacman`, `yum` o `brew`.

También pueden instalar Git junto con una interfaz gráfica, como [GitHub Desktop](https://desktop.github.com/).

---

# ¿Cómo usamos <mdi-git class="inline"/> git?
Hay muchas distintas formas de usar <mdi-git class="inline"/> git, desde la consola del PC a interfaces gráficas.  **Cada una tiene sus beneficios.**

- 👩‍💻 Consola (o interfaz por linea de comandos)

<br>
<img style="display: block; margin: 0 auto;" width="500" src="/git_bash.png"/>
<br>

<!--
Git Bash, PowerShell, cmd, terminal, etc
-->

---

# ¿Cómo usamos <mdi-git class="inline"/> git?
Hay muchas distintas formas de usar <mdi-git class="inline"/> git, desde la consola del PC a interfaces gráficas.  **Cada una tiene sus beneficios.**


- 📺 Y muchos, muchos clientes gráficos como [GitHub Desktop](https://desktop.github.com/), [GitKraken](https://www.gitkraken.com/) o incluso [VSCode](https://code.visualstudio.com/docs/editor/versioncontrol) o [PyCharm](https://www.jetbrains.com/help/pycharm/enabling-version-control.html).

<img style="display: block; margin: 0 auto;" width="750" src="/github.png"/>

---
layout: section

---

# Comandos básicos

---

# Comandos básicos de consola
Comandos para sobrevivir si no tienes experiencia previa.

- `ls`: Muestra los archivos en la carpeta actual.

- `cd <directorio>`: Cambia la carpeta actual a `<directorio>`.

El `<directorio>` puede ser descrito como una ruta **absoluta o relativa**

- **Relativo**: `Tarea/T0`
- **Absoluto:** `/Users/jacas/Progra/Syllabus/Tarea/T0`

Para una consola `..` significa el directorio de atrás y `.` es el actual.

---
layout: section

---

# Flujo de uso de <mdi-git class="inline" style="color: #a1e3fa"/> git

---

# Los tres estados de <mdi-git class="inline"/> git
Los archivos en git pueden residir en tres estados distintos, y usamos sub-comandos de git para moverlos entre ellos.

- 📝 **Modificado:** algo que cambiaste pero que todavía no está en el historial de cambios.


---

# Los tres estados de <mdi-git class="inline"/> git
Los archivos en git pueden residir en tres estados distintos, y usamos sub-comandos de git para moverlos entre ellos.

- 📝 **Modificado:** algo que cambiaste pero que todavía no está en el historial de cambios.

- ➕ **Stageado** (preparado): algo que marcaste para ser incluido en tu próximo conjunto de cambios.
```bash
# Mover los cambios que hiciste en de main.py a preparación (Staging)
git add Tareas/T0/main.py
```

---

# Los tres estados de <mdi-git class="inline"/> git
Los archivos en git pueden residir en tres estados distintos, y usamos sub-comandos de git para moverlos entre ellos.

- 📝 **Modificado:** algo que cambiaste pero que todavía no está en el historial de cambios.

- ➕ **Stageado** (preparado): algo que marcaste para ser incluido en tu próximo conjunto de cambios.

```bash {0}
# Mover los cambios que hiciste en de main.py a preparación (Staging)
git add Tareas/T0/main.py
```

- 📂 **Commiteado** (confirmado): Algo que ya fue guardado en el historial de cambios **local**.

```bash
# Empacar los cambios en preparación en un commit
# Y agregarlos al historial de cambios
git commit -m "escribe aquí una descripción corta del cambio"
```

⚠ &nbsp;**IMPORTANTE:** Después de commitear los cambios, éstos no se suben solos a la nube.

---

# Comandos auxiliares básicos de <mdi-git class="inline"/> git

<br/>

- 👀 **Visualizar estado:** Nos describe el estado en el que se encuentran los cambios. Tambien sugiere comandos para realizar acciones.

```bash
git status
```

Ante la duda, siempre revisa `git status` para saber qué hacer!


---

# Comandos auxiliares básicos de <mdi-git class="inline"/> git

<br/>

- 👀 **Visualizar estado:** Nos describe el estado en el que se encuentran los cambios. Tambien sugiere comandos para realizar acciones.

```bash
git status
```

Ante la duda, siempre revisa `git status` para saber qué hacer!

<br/>

- 🐸 **Revisar historial de commits:** Nos muestra el autor, fecha y mensaje de cada commit.

```bash
git log
```

---

# Ejemplo de uso de <mdi-git class="inline"/> git
<div class="row">
  <img style="margin: 5% 0; padding: 0 5px; float: left; width: 50%;" src="/git_use_1.png"/>
  <img style="margin: 5% 0; padding: 0 5px; float: left; width: 50%;" src="/git_use_2.png"/>
</div>

---

# Viendo el historial de cambios local
Podemos usar el comando `git log` para visualizar el historial de commits.

<!-- eliminar comentario despues (benjavicente): 
  siento que se ve mal comparado a una imagen más pequeña porque el
  resto de las imagenes que van fuera del margen son servicios, los
  terminales se han mostrado siempre completamente
  (medio nitpick xd, esta bien)
 -->

<img style="display: block; margin: 0 auto;" src="/git_log.png" width="600"/>
<br />
<img style="display: block; margin: 0 auto;" src="/commits.png" width="600"/>

---

# <tabler-brand-github class="inline" /> GitHub
¿Y a dónde mandamos nuestros cambios?

- ☁ GitHub es un servicio que almacena repositorios de Git y permite colaborar fácilmente con otras personas.
- 📝 Desde la web de GitHub puedes fácilmente ver el historial de cambios y hacer operaciones simples.
- 👥 Desde GitHub también puedes explorar repos de otras personas, reportar bugs y leer su documentación.

<br>

<img style="display: block; margin: 0 auto;" src="/github_2.png" width="800"/>


---

# ¿Pero cómo sincronizamos cambios?

Git nos permite conectar nuestro repositorio con un **origen**, un servidor remoto que nos permite sincronizar nuestros cambios y guardarlos de forma segura.

- ⬆ Cuando queremos subir nuestros cambios locales, usamos `git push`.
- ⬇ Cuando queremos obtener cambios remotos, usamos `git pull`.

<br>

<img style="display: block; margin: 0 auto;" src="/cli2.png" width="700"/>

---

# ¿Pero cómo sincronizamos cambios?

<img style="display: block; margin: 0 auto;" src="/git_github_0.png" width="700"/>

---

# ¿Pero cómo sincronizamos cambios?

<img style="display: block; margin: 0 auto;" src="/git_github_1.png" width="700"/>

---

# ¿Pero cómo sincronizamos cambios?

<img style="display: block; margin: 0 auto;" src="/git_github_2.png" width="700"/>

---

# ¿Pero cómo sincronizamos cambios?

<img style="display: block; margin: 0 auto;" src="/git_github_3.png" width="700"/>

---

# ¿Pero cómo sincronizamos cambios?

<img style="display: block; margin: 0 auto;" src="/git_github_4.png" width="700"/>

---
layout: section

---

# <codicon-terminal-bash class="inline"/> [Demostración](https://github.com/Baelfire18/template-taller-git)

---
layout: section

---

# Ramificación y espacios de trabajo

---

# Dividir para conquistar

- En proyectos más complejos, usualmente se desarrollan varias
  caracteristicas a las vez o se trabaja con multiples personas en
  el mismo repositorio. ⚙️

- En esos casos, es de mucha utilidad designar un "espacio" para
  trabajar especificamente en los cambios que uno busca realizar,
  aislando esos cambios del resto, lo que permite un mayor control
  sobre estos. Permite añadir cambios en una sin afectar a otras,
  guardando el  historial de manera independiente.🍱

<img style="display: block; margin: 0 auto;" src="/dividir.jpg" width="300"/>

---
layout: section

---

# Ramas en <mdi-git class="inline" style="color: #a1e3fa"/> git

---
---

## ¿Ramas en <mdi-git class="inline"/> git? 🤔

- Git guarda una imagen del trabajo a partir de los commits. 📸

<br />
<img style="display: block; margin: 0 auto;" src="/commits.png" width="600"/>

- Las ramas son simplemente "hilos" de commits. Que por detrás
  están marcadas con etiquetas. 🏷️

---

## ¿Ramas en <mdi-git class="inline"/> git? 🤔

- Git guarda una imagen del trabajo a partir de los commits. 📸

<br />
<img style="display: block; margin: 0 auto;" src="/commits.png" width="600"/>

- Las ramas son simplemente "hilos" de commits. Que por detrás
  están marcadas con etiquetas. 🏷️

<img src="/branch.png" width="750" style="margin:0 auto"/>

---

## Conceptos clave

<br/>

- 🔨 **Crear una rama:** Desde tu posición actual crea una nueva rama, es decir, una version de trabajo paralela a la original y luego te mueve a ella.

```bash
# Crea una rama llamada <nueva-rama> a partir de mi rama actual y te mueve a la nueva rama
git checkout -b <nueva-rama>
git switch -c <nueva-rama>
```

---


## Conceptos clave

<br/>

- 🔨 **Crear una rama:** Desde tu posición actual crea una nueva rama, es decir, una version de trabajo paralela a la original y luego te mueve a ella.

```bash{0}
# Crea una rama llamada <nueva-rama> a partir de mi rama actual y te mueve a la nueva rama
git checkout -b <nueva-rama>
git switch -c <nueva-rama>
```

<br/>
    
- 💱 **Cambio de rama**: La acción de mover de una rama de git a otra

```bash
# Navegar a la rama <rama-existente>
git checkout <rama-existente>
git switch <rama-existente>
```

---

## Conceptos clave

<br/>

- 🔨 **Crear una rama:** Desde tu posición actual crea una nueva rama, es decir, una version de trabajo paralela a la original y luego te mueve a ella.

```bash{0}
# Crea una rama llamada <nueva-rama> a partir de mi rama actual y te mueve a la nueva rama
git checkout -b <nueva-rama>
git switch -c <nueva-rama>
```

<br/>
    
- 💱 **Cambio de rama**: La acción de mover de una rama de git a otra

```bash{0}
# Navegar a la rama <rama-existente>
git checkout <rama-existente>
git switch <rama-existente>
```
<br/>

- 🤝 **Fusión de ramas**(merge): La acción de traer los cambios de una rama a otra.

```bash
# Te ubicas en la receptor antes (cambio de rama)
# Y la fusionas o unes con la rama que nombres a continuación
git merge <rama-a-traer>
```

---

## Flujo común de trabajo local

<br>


```bash{1-3|5-6|8-9|11-12|14-15|all}
# Partiendo en la rama main
# Se crea una rama y se navega a ella
git branch -b add-workflow

# Se agregan los cambios a la zona de empaquetado
git add .

# Se realizan cambios con
git commit -m "<mensaje del commit>"

# Una vez listos los cambios, uno va a main
git checkout main

# Y une los cambios de la rama nueva
git merge add-workflow
```

---
layout: section
---

# Pull Request / Merge Request

---

<!-- - ¿Que es una Pull request?
- ¿Porque hacerlas?
- ¿Que se hace al revisar una PR? -->
## Pull Request / Merge Request

<br/>

- Una Pull Request (PR) o Merge Request es una **solicitud a unir cambios de una rama a otra**. Se utliza en nubes de trabajo colaborativo como GitHub, GitLab, Bitbucket, etc.
- Cuando uno hace `git merge` localmente, el único registro que queda de la unión son los commits nuevos. Hacer una PR es crear un registro en el repositorio, con opcionalmente una descripción de los cambios y una discusión.
- Hacer PRs es una parte esencial en el trabajo colaborativo con ramas. Se utiliza en flujos de trabajo como GitHub-Flow y Git-Flow.

<br/>
<img src="/gh-flow.svg" width="800" style="margin:0 auto"/>

---

## PRs en GitHub

Una vez subida una rama con cambios a GitHub, se podrá hacer una PR en https://github.com/{usuario}/{repo}/pull/new/{id_pr} o en el interfaz, con el siguiente botón:

<img src="/new-pr.png" width="150" style="margin:0 auto"/>

Para luego añadir un título a la PR y opcionalmente añadiendo una descripción:

<img src="/pr-form.png" width="600" style="margin:0 auto"/>

<!-- <div style="color:white;background:#2ea043;padding: 5px 16px;display:box">New pull request</div> -->


---

## Discusión 🧵

- La PR estará disponible para todos los que puedan ver el repositorio.

- Todos ellos podrán **añadir comentarios** en el código. Esto se suele hacer al realizar **revisiones de pares**, donde alguien más revisa los cambios para estar seguros de unirlos al resto del trabajo.

<img src="/discussion.png" width="600" style="margin:0 auto"/>


---
layout: section
---

# Demostración

---
layout: section
---

# Comandos de ayuda extra

---
# 👀 Visualizar ramas locales

La acción de traer los cambios de una rama a otra.


```bash
git branch
```

<br/>

```r
* main
develop
docs
<feature-name>
```

---

# Manejar cambios

- 📦 **Remover**(stash): Remueve los cambios hechos antes de tu última confirmación (commit) y los guarda en una "caja" (stack).

```bash
git stash
```

<br/>

- ♻️ **Recuperar**(stash pop): Los cambios removidos por stash, pueden ser recuperados más tarde. La caja es una especie de papelera de reciclaje.


```bash
git stash pop
```
---

# Comandos avanzados de utilidad

- Mostrar el "arbol" del proyecto 
  ```bash
  git log --all --oneline --graph
  ```

<img style="display: block; margin: 0 auto;" src="/git-log-2.png" width="400"/>

- Editar interactivamente los N commits pasados de una rama
  ```bash
  git rebase --interactive HEAD~N
  ```

---

# Cómo conseguir ayuda sobre <mdi-git class="inline"/> git

### Si no recuerdas cómo usar un comando
🗒 Puedes abrir el manual que explica la funcionalidad de cualquier comando de git usando `git help <comando>`. Por ejemplo, `git help commit`.

### Si quieres repasar o explorar mas allá
📚 **[La documentación de git](https://git-scm.com/doc)** es notoriamente buena, y viene con un libro, **[Pro Git](https://git-scm.com/book/es/v2)**, de muy buena calidad (ambos tienen traducciones en español).

### Si tienes problemas o errores inesperados
🔎 **Googlea!** Git es extremadamente popular, y lo más probable es que no eres la primera persona en el mismo problema. Revisa sitios como [StackOverflow](https://stackoverflow.com/).

**Sin embargo**, es importante que siempre tengas un ojo a comentarios y te limites a buenas fuentes. No todos los recursos son de igual calidad, y **correr a ciegas un comando puede costarte meses de trabajo.**

<!--
sub-comando
-->

---

# Preguntas

<img style="display: block; margin: 0 auto;" src="/xkcd.png" width="290"/>


<!--
En la próxima sesión hablaremos de como sacarle todo el potencial a GitHub y utilizar Git de forma colaborativa, trabajando en proyectos grandes con otras personas.
-->
