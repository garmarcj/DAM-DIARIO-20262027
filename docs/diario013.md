# 🚀 Diario de clase: lunes, 28 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulos:** Programación (PR) + Entornos de desarrollo (ED)  
**Fecha:** Lunes, 28 de septiembre de 2026  
**Duración:** 4 horas lectivas (200 min)  

## 🧭 Sesión 1. PR - Constantes inmutables y literales tipados

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Arranca la Semana 3, la recta final del Sprint 1. Pau Ferrer revisa el código de cálculos matemáticos de la semana anterior. *«He visto que en el código fuente hemos escrito el número 60 a mano en varios sitios para convertir los minutos a horas, y también hemos fijado un límite de aforo con un 100 metido a la fuerza en el algoritmo»*.
* Alba Torres interviene de inmediato: *«A eso lo llamamos **'números mágicos'**. Es una mala práctica de ingeniería porque si mañana el IES El Caminàs cambia su aforo máximo, tendríamos que buscar y cambiar ese 100 línea por línea. Hoy aprenderemos a utilizar **constantes inmutables** y a definir los literales tipados para blindar los valores de negocio desde el inicio de la clase»*.

### 2. Fundamento teórico: constantes inmutables y literales tipados (10 min)

* **Constantes inmutables en Java:** Uso del modificador `final`. Una vez se le asigna un valor en memoria, la JVM bloquea la celda e impide cualquier modificación posterior. Convención de nomenclatura corporativa en AzaharTech: escritura en mayúsculas sostenidas separadas por guiones bajos (`SNAKE_CASE`).
  ```java
  final int AFORO_MAXIMO = 100;
  final double TEMPERATURA_UMBRAL = 37.5;
  ```
* **Literales tipados:** Cómo el compilador de Java infiere los valores directos escritos en el código y la necesidad de sufijos para forzar tipos, como la `f` en `float` o la `L` en `long`.

### 3. Refactorización a ControlAccesoQR v0.7 (35 min)

Actualización conjunta a `ControlAccesoQR v0.7`. Los estudiantes abren el archivo maestro y proceden a extraer los *números mágicos* transformándolos en constantes en la cabecera del programa:

* **Paso A. Refactorización en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v0.7`)**:
  * Se declaran las constantes al inicio del diagrama/código y se sustituyen los valores estáticos en las fórmulas matemáticas.

* **Paso B. Refactorización en Java (`pr/src/ControlAccesoQR.java - v0.7`)**:
  * Incorporación del bloque de constantes con el modificador `final` al inicio del `main`.
  * Refactorización de las expresiones aritméticas para que utilicen los nombres de las constantes, ganando semántica y legibilidad.

## ⚙️ Sesión 2 (50 min). PR - Aplicación al proyecto propio

**Balance de tiempo:** Docente: 10 min | Estudiante: 40 min

### 1. Trabajo del estudiante: refactorización de su proyecto propio (40 min)

* Cada estudiante abre los archivos `.psc` y `.java` correspondientes a la versión `v0.6` de su proyecto elegido de la bolsa de proyectos y la refactoriza a `v0.7`.
* Debe identificar valores estáticos en su lógica y extraerlos a **constantes inmutables (`final`)** según su dominio:
  * En **Aventura conversacional**: fijar la vida máxima o el multiplicador de daño crítico (`final int VIDA_MAXIMA = 100;`).
  * En **Motor de recomendación**: establecer el máximo de estrellas permitidas en una reseña (`final int ESTRELLAS_MAX = 5;`).
  * En **Simulador de físicas 2D**: definir la gravedad constante o la masa por defecto (`final double GRAVEDAD_TIERRA = 9.81;`).
  * En **Bóveda de contraseñas**: declarar la longitud mínima exigida o los días legales de caducidad (`final int CADUCIDAD_DIAS = 90;`).
* El docente audita el código en los distintos monitores verificando que el nombrado de las constantes cumple con el estándar estricto de mayúsculas (SNAKE_CASE).

### 2. Cierre de la sesión de programación (10 min)

* Comprobación en consola (`Ctrl + Shift + F10`) verificando que la lógica matemática produce el mismo resultado que la semana anterior, asegurando que la refactorización a constantes ha sido un éxito.

## 🧭 Sesión 3. ED - El cierre del Sprint y la calidad del repositorio

**Balance de tiempo:** Docente: 25 min | Estudiante: 25 min

### 1. Caso guía en AzaharTech. La recta final del Sprint 1 (5 min)

* Laia Claramunt inicia la sesión de Entornos de Desarrollo: *«Esta semana se agota el tiempo de nuestro primer Sprint. El cliente espera el incremento de software funcional del sistema de acceso. En metodologías ágiles, el fin de ciclo no es solo entregar código; requiere auditar la higiene del repositorio y celebrar dos ceremonias fundamentales para la mejora continua del equipo»*.

### 2. Las ceremonias de cierre del Sprint: Review frente a Retrospective (10 min)

* **A. La Revisión del Sprint (Sprint Review):** Sesión orientada al *producto*. Se reúne al equipo con el Product Owner y los *stakeholders* (cliente) para realizar una demostración del software construido y recoger *feedback* directo.
* **B. La Retrospectiva del Sprint (Sprint Retrospective):** Sesión técnica y humana orientada al *equipo*. Se analiza qué procesos han funcionado bien, qué herramientas han fallado y qué acciones de mejora se implementarán en el Sprint 2 para trabajar de forma más eficiente y sana.

### 3. Principios de higiene técnica. El control estricto de .gitignore (10 min)

* ¿Por qué jamás deben subirse archivos binarios o temporales al repositorio? Impacto en el rendimiento de clonado, colisiones (*merge conflicts*) en archivos compilados y exposición accidental de secretos o configuraciones de la máquina local.
* **El archivo .gitignore: el guardián de la limpieza:** Recordatorio del archivo que creamos en la Semana 1. Inspección de reglas mediante patrones y comodines (ej. `*.class`, `out/`).

## 🛠️ Sesión 4. Laboratorio práctico guiado. Auditoría de higiene y purga del repositorio

**Balance de tiempo:** Docente: 10 min | Estudiante: 40 min

### 1. Auditoría de higiene y purga del repositorio (40 min)

Cada estudiante se asegura de que su repositorio esté impoluto antes del cierre oficial:
* **Paso 1. Auditoría visual de archivos en el árbol de proyectos de IntelliJ:** Detectar si accidentalmente el IDE ha marcado para seguimiento (en color verde o blanco) archivos de la carpeta `out/` o del directorio privado `.idea/`.
* **Paso 2. Retirada visual de archivos no deseados de Git:** En caso de que se hayan colado binarios `.class`, proceder a eliminarlos del control de seguimiento (sin borrarlos físicamente del disco) mediante el comando `git rm --cached` integrado en la vista de control de versiones del IDE.
* **Paso 3. Consolidación de las reglas universales en .gitignore:** Revisión del archivo en la raíz `azahartech/nombre-equipo/.../.gitignore` garantizando que todo el directorio de compilación está formalmente ignorado.
* **Paso 4. Confirmación y sincronización visual con GitHub:** Redacción del commit final de higiene técnica (ej. `chore(ed): limpiar archivos compilados y asegurar gitignore`) y *Push* hacia el repositorio remoto.

### 2. Cierre y verificación de puestos (5 min)

* El docente se conecta a los repositorios web de los estudiantes para auditar rápidamente los *commits* y confirmar que nadie tiene archivos binarios publicados.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendido el uso de la palabra reservada 'final' (constantes).   ║
║ [ ] Refactorizada la versión v0.7 sustituyendo números mágicos.        ║
║ [ ] Asimiladas las diferencias entre Sprint Review y Retrospective.    ║
║ [ ] Repositorio auditado: cero archivos binarios en control de Git.    ║
║ [ ] Archivo .gitignore validado y consolidado para el cierre del Sprint║
╚════════════════════════════════════════════════════════════════════════╝
```