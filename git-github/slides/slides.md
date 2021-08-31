---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
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

# ¿Qué veremos hoy?

- Qué es sistema de control de versiones
- Qué es git y qué los distingue de otros sistemas
- Los fundamentos detrás de git
- Comandos básicos y un workflow típico

---

# Algunos tips





---

# ¿Cómo instalamos git?

Git puede ser instalado de muchas formas distintas, cuál usar depende del contexto y lo que te pidan!


Los links de descarga a la versión oficial de Git se pueden encontrar en [git-scm.com/downloads](https://git-scm.com/downloads).

- En Windows, se puede obtener con un installador disponible en la página, que prevee una consola de Linux (Git Bash), y con interfaces gráficas como GitHub Desktop.
- En macOS, con `homebrew install git` y con un instalador binario disponible en la página.
- Y en Linux, puede encontrarse en la mayoria de los administradores de paquetes, como `apt`, `pacman`, `yum` o `linuxbrew`.

<!-- 
Instalar gh? https://github.com/cli/cli#installation

 -->


---
layout: section
---

# Git como sistema de control de versiones

---

# Control de Versiones


- 🛠 Es un sistema que registra los cambios realizados en un archivo o grupo de archivos con tal de poder recuperar fácilmente versiones antiguas o identificar cambios específicos.

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

# Demostración


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

# Tambien secreatos o contraseñas
.key
.env
```


---


# El archivo `.gitignore`

```bash
# Se pueden entregar patrones en vez de archivos o directorios
datos/generado-*.csv  # generado-1.csv, generado-2.csv, generado-nuevo.csv

# Además con ! se puede considerar elementos que fueron ignorados
# por una regla anterior (rechequear esto plz)
!datos/iniciales.csv

# Tambien secreatos o contraseñas
.key
.env
```


---
layout: section
---

# El rol de GitHub


---

# Sincronizar los camios


```bash
# Para obtener un repositorio, se utiliza:
git clone

# Si alguien sube realizaon cambios, se pueden obtener con:
git pull

# Para subir los cambios propios se utiliza:
git push # -u origin HEAD
```

> **Importante!**
>    Hay que evitar realizar commits a una rama (?)
>    en la que está trabajando otra persona.

---

# Cómo conseguir ayuda sobre Git

- 🔎 **Googlea!** Git es extremedamente popular, y lo más probable es que no eres la primera persona en tener ese problema.'

> Pero ten cuidado! 
> No todo el material es igual calidad, así que siempre debes estar atento a comentarios o advertencias.

- 📚 **La documentación de git** es notoriamente buena, y viene con un libro, *Pro Git*, de muy buena calidad. (Ambos tienen traducciones en español)


---