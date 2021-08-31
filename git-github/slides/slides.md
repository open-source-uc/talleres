---
theme: default
background: https://source.unsplash.com/842ofHC6MaI
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Taller de Git y GitHub
  Hecho por Open Source UC

  Más información en [GitHub](https://github.com/open-source-uc/talleres)
---

# Taller de Git y GitHub

Sesión 1: Introducción a Git y GitHub
<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    ¿Qué es git? <carbon:arrow-right class="inline"/>
  </span>
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
<!-- 
Instalar gh? https://github.com/cli/cli#installation

 -->


---
layout: section
---

# Sistemas de Control de Versiones

---

# Sistemas de Control de Versiones (VCSs)


- 📂 Es un sistema que registra los cambios realizados en un archivo o grupo de archivos con tal de poder recuperar fácilmente versiones antiguas o identificar cambios específicos.

- Nos permite evitar esto:

<img src="/old-versiones.png" width="300" />


<!-- Si eres programador y quieres conservar cada versión de una imagen o diseño (que sin duda es lo que quieres), utilizar un sistema de control de versiones es una decisión muy acertada. El sistema te permite volver a versiones anteriores de archivos, regresar a versiones anteriores de todo el proyecto, comparar cambios a lo largo del tiempo, ver quién modificó por última vez el contenido que pudo haber causado el problema, ver quién introdujo el problema y cuándo, y mucho más. El uso de este sistema de control de versiones también suele significar que si se equivoca o pierde archivos, se pueden restaurar fácilmente. -->

---

# Git

El sistema de control de versiones mas usado en el mundo!

Git es utilizado por prácticamente todas las compañías de tecnología a nivel mundial, haciendo funcionar todo desde Facebook hasta la NASA.

A grandes rasgos Git es:

- 👥 **Distribuido** - git siempre mantiene una copia completa y autónoma del código en cada computador. Es a prueba de incendios 🚒! 
- 🏠 **Local primero** - git solo manda información al servidor cuando tu se lo pides explícitamente (no es Drive!)
- ➕ **Mayoritariamente aditivo** - borrar cosas de git es muy díficil y requiere comandos especiales (una gran idea!)



---

<center><img src="/distribuido.png" width="700" /></center>

---

# Los tres estados de Git
Los archivos en Git pueden residir en tres estados distintos:

- 📝 **Modificado:** algo que cambiaste pero que todavía no está en el historial de cambios.
- ➕ **Stageado** (preparado o rastreado): algo que marcaste para ser incluido en tu próximo conjunto de cambios.
- 📂 **Commiteado** (confirmado): Algo que ya fue guardado en el historial de cambios.

Así es como versiones de nuestros archivos pueden estar en tres lugares distintos:


<img src="/tres-lugares.png" style="display: block; margin: 0 auto;" width="340"/>

---
layout: section
---

# ¿Cómo usamos Git?


---

# Flujo de git local

Luego de editar los archivos del repositorio:

```bash {1,2|3,4|5,6}
# Pasar los cambios de main.py a preparación
git add src/main.py
# Confirmar los cambios y enviar a BBDD
git commit -m "remover except Exception"
```

---

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


# El archivo `.gitignore`

Utilizar `git add .` con confianza

Es un archivo que le indica a Git que archivos o directorios ignorar. Cada línea corresponde a un path a ser ignorado, cuyos cambios ya no serán notados por git.


```bash
# Normalmente se ignorar archivos autogenerados por el sistema, como
.DS_Store

# Además de archivos que son generados por programas
.venv/
dist/

# O secretos o contraseñas que nadie debería ver
.key
.env
```

---

# Cómo conseguir ayuda sobre Git

- 🔎 **Googlea!** Git es extremedamente popular, y lo más probable es que no eres la primera persona en tener ese problema.'

> Pero ten cuidado! 
> No todo el material es igual calidad, así que siempre debes estar atento a comentarios o advertencias.

- 📚 **La documentación de git** es notoriamente buena, y viene con un libro, *Pro Git*, de muy buena calidad. (Ambos tienen traducciones en español)

