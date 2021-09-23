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
git checkout -b <nueva-rama>
or
git branch <nueva-rama>
```
<br/>
    
- 💱 **Cambio de rama**: La acción de mover de una rama de git a otra

```bash
# Navegar entre las ramas
git checkout <rama-existente>
or
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

