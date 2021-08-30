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


<style>
h1 {
  background-color: white;
  background-image: initial;
}
p {
  color: white;
}
</style>

---

# Control de Versiones

## ¿Qué es un sistema de control de versiones?

- 🛠 Es un sistema que registra los cambios realizados en un archivo o grupo de archivos con tal de poder recuperar fácilmente versiones antiguas o identificar cambios específicos.

- Nos permite evitar esto:

<img src="old-versiones.png" width="300" />


<!-- Si eres programador y quieres conservar cada versión de una imagen o diseño (que sin duda es lo que quieres), utilizar un sistema de control de versiones es una decisión muy acertada. El sistema te permite volver a versiones anteriores de archivos, regresar a versiones anteriores de todo el proyecto, comparar cambios a lo largo del tiempo, ver quién modificó por última vez el contenido que pudo haber causado el problema, ver quién introdujo el problema y cuándo, y mucho más. El uso de este sistema de control de versiones también suele significar que si se equivoca o pierde archivos, se pueden restaurar fácilmente. -->

---

# Git es

El sistema de control de versiones mas usado en el mundo! 

Y además es:

- 👥 **Distribuido** - git siempre mantiene una copia completa y autónoma del código en cada computador. Es a prueba de incendios 🚒! 

- 🏠 **Local primero** - git solo manda información al servidor cuando tu se lo pides explícitamente (no es Drive!)
- ➕ **Mayoritariamente aditivo** - borrar cosas de git es muy díficil y requiere comandos especiales (una gran idea!)



---

## ¿Cómo instalar git?

[Acá](https://git-scm.com/downloads)


---


<center><img src="distribuido.png" width="700" /></center>


---

## Los tres estados de Git
- 📁 Directorio de trabajo: Tu carpeta del PC
- 🔴 Staging: Área de preparación 
- <img src="https://raw.githubusercontent.com/github/explore/78df643247d429f6cc873026c0622819ad797942/topics/github/github.png" width="21" height="21" style="filter:invert(100%);display:inline;margin-right:8px"/>Repositorio de git




---

## Métodología básica de Git

- ✍ **Modificar archivos**
- ➡ **Agregar cambios al área de preparación** (*stagear* - staging area)
- ✅ **Confirmar cambios** (*commitear*), agregándolos a la BBDD de git.
- ☁ **Subir los cambios a Gitub** (*pushear*)

---

## Flujo de git


```bash {1,2|3,4|5,6}
# Pasar los cambios de main.py a preparación
git add .src/main.py
# Confirmar los cambios y enviar a BBDD
git commit -m "fix: remove a bug"
# Enviar repo al servidor
git push -u origin HEAD
```


---




<div v-click-hide>Hola?</div>

<v-clicks>

- add files
- commit -m "mensaje"
- push

</v-clicks>

<!-- https://sli.dev/guide/animations.html#v-after :( -->
<div v-click-hide>xd</div>

<v-click>

hola

</v-click>
