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

# Taller de Git Avanzado <mdi-git class="inline"/>

## **Sesión 2: Git Avanzado**
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

<!--
TODO: legibilidad texto titulo
-->

---

# Algunas cosas antes de que empecemos ✋

- 🎙 Asegúrense de **mantener apagado sus micrófonos** cuando no los estén usando
- 💬 **Aprovechen el chat** para hacer preguntas sobre la presentación
- 🖐 O bien esperen al final de la presentación, **levantando la mano**

## ¿Qué veremos hoy?

- Uso de ramas
- Trabajo colaborativo con Git
- Buenas practicas
- Comandos avanzados de utilidad

<!-- Mensaje pseudomotivacional: es muy dificil, y puede que no lo entiendan todo a la primera, siempre tienen la presentación! -->

---
layout: section
---
# Ramas y espacios de trabajo
---

<!-- parte teorica -->

## Dividir para conquistar

- En proyectos más complejos, usualmente se desarrollan varias
  caracteristicas a las vez o se trabaja con multiples personas en
  el mismo repositorio. ⚙️

- En esos casos, es de mucha utilidad designar un "espacio" para
  trabajar especificamente en los cambios que uno busca realizar,
  aislando esos cambios del resto, lo que permite un mayor control
  sobre estos. 🍱

- Separar un proyecto en varias rama permite añadir cambios en una
  sin afectar a otras, guardando el  historial de manera independiente.
  Luego de que los cambios esten listos para ser unidos a una rama
  principal del proyecto, pueden ser revisadas claramente con sus
  diferencias e historial antes de ser unidas. 📝

---

## ¿Ramas en Git? 🤔

- Git guarda una imagen del trabajo a partir de los commits,
  que son identificables a partir de un string único llamado hash.
  Ejemplo de hash: `0ee13be`

- Las ramas son simplemente etiquetas que apuntan a los commits,
  que se mueven a medida que uno crea commits sobre ellas. 🏷️

- Uno indica que uno esta en una rama utilizando el apuntador especial
  `HEAD`. 

<!-- parte más practica -->

<!-- https://git-scm.com/book/es/v2/Ramificaciones-en-Git-%C2%BFQu%C3%A9-es-una-rama%3F -->

<!-- > La rama por defecto de Git es la rama master.
https://git-scm.com/book/es/v2/Ramificaciones-en-Git-%C2%BFQu%C3%A9-es-una-rama%3F
-->
---
layout: cover

---
# Ramas



<img src="/branch.png" width="750" style="margin:0 auto"/>

---
---
## Conceptos clave

<br/>

- 🔨 **Crear una rama:** Desde tu posición actual crea una nueva rama, es decir, una version de trabajo paralela a la original y luego te mueve a ella.

```bash
# Crea una rama llamada <nueva-rama> a partir de mi rama actual
git branch <nueva-rama>
```

<br/>
    
- 💱 **Cambio de rama**: La acción de mover de una rama de git a otra

```bash
# Navegar entre las ramas
git switch <rama-existente>
# Crear y cambiar de rama
git switch -c <nueva-rama>
```
<br/>

- 🤝 **Fusión de ramas**(merge): La acción de traer los cambios de una rama a otra.

```bash
# Te ubicas en la receptor antes (cambio de rama)
# Y la fusionas o unes con la rama que nombres a continuación
git merge <rama-a-traer>
```

> `git switch [-c]` es equivalente a git `checkout [-b]`

---

## Flujo común de trabajo local

<br>


```bash{1-3|5-6|8-9|11-12|14-15|all}
# Partiendo en la rama main
# Se crea una rama y se navega a ella
git switch -c add-workflow

# Se agregan los cambios a la zona de empaquetado
git add .

# Se realizan cambios con
git commit -m "<mensaje del commit>"

# Una vez listos los cambios, uno va a main
git switch main

# Y une los cambios de la rama nueva
git merge add-workflow
```

---
layout: section
---

# Pull (Merge) Request

---

<!-- - ¿Que es una Pull request?
- ¿Porque hacerlas?
- ¿Que se hace al revisar una PR? -->
## Pull (Merge) Request

<br/>

- Una Pull Request (PR) o Merge Request es una **solicitud a unir cambios de una rama a otra**.
- Cuando uno hace `git merge` localmente, el único registro que queda de la unión son los commits nuevos. Hacer una PR es crear un registro en el repositorio, con opcionalmente una descripción de los cambios y una discusión.
- Hacer PRs es una parte esencial en el trabajo colaborativo con ramas. Se utiliza en flujos de trabajo como GitHub-Flow y Git-Flow.

<br/>
<img src="/gh-flow.svg" width="800" style="margin:0 auto"/>

---

## PRs en GitHub

Una vez subida una rama con cambios a GitHub, se podrá hacer una PR en https://github.com/{usuario}/{repo}/pull/new/{nombre-rama} o en el interfaz, con el siguiente botón:

<img src="/new-pr.png" width="150" style="margin:0 auto"/>

Para luego añadir un título a la PR y opcionalmente añadiendo una descripción:

<img src="/pr-form.png" width="600" style="margin:0 auto"/>

<!-- <div style="color:white;background:#2ea043;padding: 5px 16px;display:box">New pull request</div> -->


---

## Discusión

- La PR estará disponible para todos los que puedan ver el repositorio.

- Todos ellos podrán **añadir comentarios** en el código. Esto se suele hacer al realizar **revisiones de pares**, donde otra persona que no participo en los cambios revisa los cambios, y ve si estos deben (o no) ser unidos.

- Estas reseñas se hacer en la sección de cambios realizados (_Files changed_), en la opción de Review Changes. Opcionalmente uno puede seleccionar trozos de código en los numeros junto a las lineas a comentar para indicar las lineas a comentar.


---
layout: section
---

# Demostración


---
layout: section
---

# Comandos de ayuda extra



---
layout: default
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
layout: default
---
# Manejar cambios
El c

- 📦 **Remover**(stash): Remueve los cambios hechos antes de tu última confirmación (commit) y los guarda en una "caja" (stack).

```bash
git stash # git checkout .
```

<br/>

- ♻️ **Recuperar**(stash pop): Los cambios removidos por stash, pueden ser recuperados más tarde. La caja es una especie de papelera de reciclaje.


```bash
git stash pop
```
---

## Comandos avanzados de utilidad

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


# Preguntas

<img style="display: block; margin: 0 auto;" src="/xkcd.png" width="290"/>

---

# <ion-git-branch class="inline"/> Open Source UC

- Una comunidad de estudiantes apasionados por el software abierto y los proyectos colaborativos.
- Puedes sumarte! Entra a nuestro <mdi-discord class="inline" /> [Discord](https://discord.com/invite/VMXCNAvjPW) o <mdi-telegram class="inline" /> [Telegram](https://t.me/joinchat/gF0vFkKWZZxiZTIx). También puedes suscribirte a anuncios en [**t.me/open_source_uc**](https://t.me/open_source_uc).

<br>
<img style="display: block; margin: 0 auto;" src="/osuc.png" width="1200"/>
