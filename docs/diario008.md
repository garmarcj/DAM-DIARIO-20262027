# 🚀 Diario de clase: lunes, 21 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulos:** Programación (PR) + Entornos de desarrollo (ED)  
**Fecha:** Lunes, 21 de septiembre de 2026  
**Duración:** 4 horas lectivas (200 min)

## 🧭 Sesión 1. PR - Asignación compuesta, incremento y mutabilidad de memoria

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Pau Ferrer intenta añadir un contador de fichajes al código de la semana anterior repitiendo el nombre de la variable (`personasEnCentro = personasEnCentro + 1`).
* Alba Torres explica que en el código profesional no duplicamos variables a ambos lados del igual: se utilizan operadores compuestos y de incremento para hacer el código más compacto y reducir erratas.

### 2. Micro-exposición docente (10 min)

* Operadores de asignación compuesta en Java: cómo la expresión compacta `total += valor;` equivale a `total = total + valor;` y cómo actúa directamente sobre la celda de memoria RAM.
* Operadores unarios de incremento (`++`) y decremento (`--`).
* Distinción fundamental en memoria entre utilizar estas expresiones frente a la asignación tradicional.

### 3. Andamiaje guiado: PSeInt ➔ Java (versión v0.4) (35 min)

Actualización conjunta a `ControlAccesoQR v0.4`. Los estudiantes abren el archivo maestro y refactorizan el código:
* **Paso A.** Actualización en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v0.4`).
* **Paso B.** Refactorización en Java (`pr/src/ControlAccesoQR.java - v0.4`). Se integran contadores para el aforo disponible y el identificador de los fichajes utilizando los operadores `+=`, `-=` y `++`.

## ⚙️ Sesión 2 (50 min). PR - Refactorización y aplicación al proyecto propio

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 1. Trabajo del estudiante en el proyecto propio (40 min)

* Cada estudiante abre los archivos `.psc` y `.java` de su proyecto elegido de la bolsa de proyectos.
* Aplica la refactorización a la versión `v0.4` utilizando operadores unarios y compuestos:
    * En **Aventura conversacional**: usar `-=` para reducir puntos de vida o `++` para contar turnos.
    * En **Motor de recomendación**: usar `+=` para sumar puntuaciones a la afinidad.
    * En **Simulador de físicas 2D**: usar `+=` para acumular aceleración o distancia.
    * En **Bóveda de contraseñas**: usar `--` para decrementar días restantes de caducidad.
* El docente revisa los puestos asegurándose de que nadie duplique nombres de variables en las asignaciones.

### 2. Cierre de la sesión de programación (5 min)

* Comprobación en consola de que el código compila y que el cálculo matemático funciona igual tras la refactorización (`Ctrl + Shift + F10`).

## 🧭 Sesión 3. ED - La mecánica interna de Git y la trazabilidad

**Balance de tiempo:** Docente: 25 min | Estudiante: 25 min

### 1. El caos de los «cambios varios» en AzaharTech (5 min)

* Laia Claramunt proyecta el historial de GitHub y muestra tres *commits* seguidos con mensajes inútiles: *"cambios"*, *"subiendo cosas que faltaban"* y *"ahora sí que funciona"*.
* Reflexión: Si el proyecto se rompe, el historial no sirve de nada. Cada confirmación debe ser una unidad atómica y documentada para evitar una caja negra opaca.

### 2. Micro-exposición docente: El modelo de datos de Git (10 min)

* Instantáneas frente a diferencias: cómo Git guarda la evolución de los archivos.
* Los tres estados locales obligatorios por los que pasa un archivo:
    1. Modificado (*Modified*) — En el *Working Directory*.
    2. Preparado (*Staged*) — En el *Staging Area*.
    3. Confirmado (*Committed*) — En el *Local Repository*.

### 3. Inspección visual y Conventional Commits (10 min)

* Inspección de cambios: cómo leer el *Git Diff* línea a línea.
* El estándar de calidad de la industria: **Conventional Commits**. Catálogo de prefijos (`feat`, `fix`, `docs`, `refactor`) y las cuatro reglas de oro para redactar mensajes descriptivos que aporten valor.

## 🛠️ Sesión 4. Laboratorio práctico guiado: Flujo Git en IntelliJ IDEA

**Balance de tiempo:** Docente: 10 min | Estudiante: 40 min

### 1. Taller de control de versiones (40 min)

Cada estudiante realiza los pasos técnicos directamente sobre el código `v0.4` que acaba de refactorizar en la clase de Programación:
* **Paso 1.** Localización del panel visual de Git (`Alt + 0` o `Ctrl + K`).
* **Paso 2.** Observación del estado *Modified* en los archivos `.java` y `.psc`.
* **Paso 3.** Inspección visual con el visor Diff de dos columnas en el IDE.
* **Paso 4.** Preparación selectiva (*Staging*) de los cambios correctos.
* **Paso 5.** Redacción del Commit Convencional (ej. `refactor(pr): aplicar operadores compuestos e incrementos en cálculos de aforo`) y confirmación.
* **Paso 6.** (Opcional guiado). Descarte de cambios accidentales en el Directorio de Trabajo (*Rollback*).
* **Paso 7.** Sincronización final con el repositorio remoto (*Push*).

### 2. Cierre y verificación (5 min)

* El docente verifica en los perfiles web de GitHub que todos los proyectos de los alumnos tienen los *commits* sincronizados con la nomenclatura de *Conventional Commits*.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendido el uso de operadores de incremento y asignación.       ║
║ [ ] Refactorizada la versión v0.4 del proyecto propio sin errores.     ║
║ [ ] Asimilados los 3 estados de Git (Modified, Staged, Committed).     ║
║ [ ] Entendido y aplicado el estándar de Conventional Commits.          ║
║ [ ] Cambios atómicos confirmados y enviados a GitHub (Push).           ║
╚════════════════════════════════════════════════════════════════════════╝
```