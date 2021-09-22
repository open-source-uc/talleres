---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# Welcome to Slidev

Presentation slides for developers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---

# Que es una terminal

---

# Que es un emulador de consola

---

# Instalar PowerShell

- Descagar powershell: https://github.com/PowerShell/PowerShell/releases/tag/v7.1.4
  - `PowerShell-7.1.4-win-x64.msi`

---

# Que es un manejador de paquetes 

---

# Instalar scoop (Manejador de paquetes)
- Inciar consola como admin: `Set-ExecutionPolicy RemoteSigned -scope CurrentUser`
- Inciar consola sin admin: `Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')`

---

# Agregar nuevo repositorio

- scoop install git
- scoop install aria2
- scoop bucket add extras
- scoop update
- scoop install wt
- scoop bucket add nerd-fonts
- scoop install sudo
- sudo scoop install firamono-nf

---

# Configurar emulador de terminal

- Settings -> open json file

```json
"schemes":[
  {
      "background": "#2E3440",
      "black": "#333333",
      "blue": "#5E81AC",
      "brightBlack": "#808080",
      "brightBlue": "#81A1C1",
      "brightCyan": "#88C0D0",
      "brightGreen": "#C3E4A8",
      "brightPurple": "#DAACD1",
      "brightRed": "#E5747F",
      "brightWhite": "#FFFFFF",
      "brightYellow": "#FFE396",
      "cursorColor": "#FFFFFF",
      "cyan": "#8FBCBB",
      "foreground": "#C0C0C0",
      "green": "#A3BE8C",
      "name": "NordTheme",
      "purple": "#B48EAD",
      "red": "#BF616A",
      "selectionBackground": "#FFFFFF",
      "white": "#C0C0C0",
      "yellow": "#EBCB8B"
  },
]
```
- defaults

```json
"defaults": 
        {
            "acrylicOpacity": 0.59999999999999998, // transparencia ventana
            "antialiasingMode": "grayscale",
            "backgroundImage": "/path/to/img",
            "backgroundImageOpacity": 0.080000000000000002, // transparencia img
            "backgroundImageStretchMode": "fill",
            "colorScheme": "NordTheme",
            "font": 
            {
                "face": "FiraMono NF",
                "size": 10,
                "weight": "bold"
            },
            "historySize": 9001,
            "useAcrylic": true
        },
```

---

# Modificar el terminal

- scoop install neofetch
- scoop install starship
- code $PROFILE
- `Invoke-Expression (&starship init powershell)`

---

# Herramientas de linea de Comandos

- pip install pipx
- pipx install thefuck
- pipx ensurepath