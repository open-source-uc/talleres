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

---

# Taller de Git y GitHub

## **Sesión 1: Introducción a Git y GitHub**
<div class="pt-12">
  <a href="https://osuc.dev/" style="border-style: revert;"> <span class="px-2 py-1 rounded cursor-pointer bg-black bg-opacity-60" hover="bg-opacity-100">
    por Open Source UC <ph:link-simple-duotone class="inline"/>
  </span>
  </a>
</div>

---
layout: section
---

# Antes de empezar...

---

# Algunas cosas antes de que empecemos ✋

- 🎙 Asegúrense de **mantener apagado sus micrófonos** cuando no los estén usando
- 💬 **Aprovechen el chat** para hacer preguntas sobre la presentación
- 🖐 O bien esperen al final de la presentación, **levantando la mano**

## ¿Qué veremos hoy?

- Qué es un **sistema de control de versiones** (VCS)
- Qué es **git** y qué lo hace especial
- Los **fundamentos detrás de git**
- Un **flujo de uso** de git local 🏠 y remoto ☁, usando GitHub.

---

# ¿Cómo instalamos git? ⬇

Git puede ser instalado de muchas formas distintas; cuál usar depende del contexto y lo que te pidan!


Los links de descarga a la versión oficial de Git se pueden encontrar en [git-scm.com/downloads](https://git-scm.com/downloads).

- En **Windows**, se puede obtener con un installador disponible en la página, que provee una consola de Linux (Git Bash), y con interfaces gráficas como GitHub Desktop.
- En **macOS**, con Homebrew, usando `brew install git`.
- Y en **Linux**, puede encontrarse en la mayoria de los administradores de paquetes, como `apt`, `pacman`, `yum` o `brew`.

También pueden instalar Git junto con una interfaz gráfica, como [GitHub Desktop](https://desktop.github.com/).

---
layout: section
---

# Sistemas de Control de Versiones

---

# Sistemas de Control de Versiones (VCSs)


- 📂 Es un sistema que registra los cambios realizados en un archivo o grupo de archivos con tal de poder recuperar fácilmente versiones antiguas o identificar cambios específicos.

- Nos permite evitar esto:

<br>
<img style="display: block; margin: 0 auto;" src="/old-versiones.png" width="300" />

---

# Git

El sistema de control de versiones mas usado en el mundo!

Git es utilizado por prácticamente todas las compañías de tecnología a nivel mundial, haciendo funcionar todo desde Facebook hasta la NASA.

---

# Git

El sistema de control de versiones mas usado en el mundo!

Git es utilizado por prácticamente todas las compañías de tecnología a nivel mundial, haciendo funcionar todo desde Facebook hasta la NASA.

A grandes rasgos Git es:

- 👥 **Distribuido** - git siempre mantiene una copia completa y autónoma del código en cada computador. Es a prueba de incendios 🚒! 


---

TODO: Repo local/remoto

<img style="display: block; margin: 0 auto;" src="/distribuido.png" width="700" />

---

# Git

El sistema de control de versiones mas usado en el mundo!

Git es utilizado por prácticamente todas las compañías de tecnología a nivel mundial, haciendo funcionar todo desde Facebook hasta la NASA.

A grandes rasgos Git es:

- 👥 **Distribuido** - git siempre mantiene una copia completa y autónoma del código en cada computador. Es a prueba de incendios 🚒! 
- 🏠 **Local primero** - git solo manda información al servidor cuando tu se lo pides explícitamente (no es Drive!)


---

# Git

El sistema de control de versiones mas usado en el mundo!

Git es utilizado por prácticamente todas las compañías de tecnología a nivel mundial, haciendo funcionar todo desde Facebook hasta la NASA.

A grandes rasgos Git es:

- 👥 **Distribuido** - git siempre mantiene una copia completa y autónoma del código en cada computador. Es a prueba de incendios 🚒! 
- 🏠 **Local primero** - git solo manda información al servidor cuando tu se lo pides explícitamente (no es Drive!)
- ➕ **Mayoritariamente aditivo** - borrar cosas de git es muy díficil y requiere comandos especiales (una gran idea!)


---

TODO: SEPARAR, warning de que todavía no es remoto, cambiar diagrama por ejemplo concreto ayudante y tarea.

# Los tres estados de Git
Los archivos en Git pueden residir en tres estados distintos:

- 📝 **Modificado:** algo que cambiaste pero que todavía no está en el historial de cambios.
- ➕ **Stageado** (preparado): algo que marcaste para ser incluido en tu próximo conjunto de cambios.
- 📂 **Commiteado** (confirmado): Algo que ya fue guardado en el historial de cambios **local**.

⚠  Después de commitear los cambios, éstos no se suben solos a la nube, después veremos cómo hacerlo.

<!-- Agregar diagrama nuevo aquí -->
<!-- Así es como versiones de nuestros archivos pueden estar en tres lugares distintos: -->
<!-- <img src="/tres-lugares.png" style="display: block; margin: 0 auto;" width="340"/> -->

---
layout: section
---

# ¿Cómo usamos Git?

--- 

# Clientes o interfaces de Git
Hay muchas distintas formas de utilizar Git, desde la linea de comandos a toda clase de interfaces gráficas.  **Cada una tiene sus beneficios.**

- 👩‍💻 Tenemos la interfaz por linea de comandos (consola)

<br>
<img style="display: block; margin: 0 auto;" width="600" src="/cli.png"/>
<br>


--- 

# Clientes o interfaces de Git
Hay muchas distintas formas de utilizar Git, desde la linea de comandos a toda clase de interfaces gráficas.  **Cada una tiene sus beneficios.**

- 👩‍💻 Tenemos la interfaz por linea de comandos (consola)

- 📺 Y muchos, muchos clientes gráficos como [GitHub Desktop](https://desktop.github.com/), [GitKraken](https://www.gitkraken.com/) o incluso [VSCode](https://code.visualstudio.com/docs/editor/versioncontrol) o [PyCharm](https://www.jetbrains.com/help/pycharm/enabling-version-control.html).

<img style="display: block; margin: 0 auto;" width="750" src="https://1v5ymx3zt3y73fq5gy23rtnc-wpengine.netdna-ssl.com/wp-content/uploads/2021/03/og-git-client.png" />

---

TODO: Separar, ejemplo análogo de git, doble confirmación, separar el ejemplo.

# Flujo de git local
Para agregar cambios a nuestro historial **local** de Git:

0. **Editar los archivos**
1. **Stagearlos**, agregándolos al área de preparación con `git add <nombre_archivo_o_carpeta>`.
2. **Commitearlos**, agregando los cambios preparados al historial de cambios con `git commit`.
3. Revisar el estado de nuestro repositorio, utilizando `git status`.

Por ejemplo. Digamos que tenemos un archivo `main.py` en la carpeta `src/` cuyos cambios ahora quieres guardar.

```bash {1,2|3,4|5,6|all}
# Pasar los cambios de main.py a preparación (Staging)
git add src/main.py
# Guardar los cambios en el historial de Git.
git commit -m "exribe aqu´una descripción corta del cambio"
# Verificamos el estado de nuestro repositorio
git status
```

---

TODO: dividir
# GitHub
¿Y a dónde mandamos nuestros cambios?

- ☁ GitHub es un servicio que almacena repositorios de Git y permite colaborar fácilmente con otras personas.
- 📝 Desde la web de GitHub puedes fácilmente ver el historial de cambios y hacer operaciones simples.
- 👥 Desde GitHub también puedes explorar repos de otras personas, reportar bugs y leer su documentación.

## ¿Pero cómo?

Git nos permite conectar nuestro repositorio con un **origen**, un servidor remoto que nos permite sincronizar nuestros cambios y guardarlos de forma segura.

- ⬆ Cuando queremos subir nuestros cambios locales, usamos `git push`.
- ⬇ Cuando queremos obtener cambios remotos, usamos `git pull`.


---
layout: section
---

# Demostración 🛠


---

TODO: add con ., cheatsheet al final,
# El archivo `.gitignore`

Utilizar `git add .` con confianza

Es un archivo que le indica a Git que archivos o directorios ignorar. Cada línea corresponde a un path a ser ignorado, cuyos cambios ya no serán notados por git.


```gitignore
# Normalmente se ignorar archivos autogenerados por el sistema, como
.DS_Store

# O archivos que solo te sirven a ti, como entornos virtuales
.venv/
dist/

# O secretos o contraseñas que nadie debería ver
.env
archivo_ultra_secreto.txt
```

---

# Cómo conseguir ayuda sobre Git

### Si no recuerdas cómo usar un comando
🗒 Puedes abrir el manual que explica la funcionalidad de cualquier comando de git usando `git help <comando>`. Por ejemplo, `git help commit`.

### Si quieres repasar o explorar mas allá
📚 **La documentación de git** es notoriamente buena, y viene con un libro, *Pro Git*, de muy buena calidad. (Ambos tienen traducciones en español)

### Si tienes problemas o errores inesperados
🔎 **Googlea!** Git es extremadamente popular, y lo más probable es que no eres la primera persona en el mismo problema. Revisa sitios como [StackOverflow](https://stackoverflow.com/).

**Sin embargo**, es importante que siempre tengas un ojo a comentarios y te limites a buenas fuentes. No todos los recursos son de igual calidad, y **correr a ciegas un comando puede costarte meses de trabajo.**

---

# Open Source UC

- Contacto, etc