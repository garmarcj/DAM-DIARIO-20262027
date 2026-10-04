# 🚀 Diario de clase: jueves, 8 de octubre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Jueves, 8 de octubre de 2026  
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1. PR - Métodos de transformación y extracción en la clase String

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Pau Ferrer está revisando los *logs* de entrada generados por los alumnos del IES El Caminàs. *«Tenemos un problema de calidad de datos. Algunos alumnos teclean su DNI con espacios en blanco al inicio, otros escriben su nombre mezclando mayúsculas y minúsculas de forma caótica (ej. "pAu"), y a veces necesitamos extraer únicamente la primera letra de su perfil para generar el ticket. ¿Tenemos que crear bucles complejos para arreglar cada letra?»*
* Alba Torres interviene con una sonrisa: *«Para nada. La clase `String` en Java incluye una verdadera navaja suiza de herramientas. Hoy dejaremos de limitarnos a inspeccionar cadenas para empezar a transformarlas y trocearlas con métodos de limpieza, reemplazo y extracción. Eso sí, recordando siempre la trampa letal de la inmutabilidad de los objetos»*.

### 2. Fundamento teórico: métodos de transformación y extracción en la clase String (10 min)

* **A. Métodos de limpieza y normalización:**
    * `trim()`: Elimina espacios en blanco o tabulaciones accidentales al principio y al final de la cadena.
    * `toUpperCase()` y `toLowerCase()`: Transformación absoluta, ideal para normalizar entradas de usuario antes de compararlas.
    * `replace(oldChar, newChar)`: Sustitución rápida de caracteres, útil para adaptar formatos (ej. cambiar comas por puntos).
* **B. Extracción de fragmentos de texto: el método substring():**
    * `substring(int beginIndex)`: Devuelve una nueva cadena cortando desde el índice indicado hasta el final.
    * `substring(int beginIndex, int endIndex)`: Corta un fragmento intermedio. Explicación de la **regla estricta del endIndex exclusivo**: el corte se realiza justo antes del índice final, por lo que la longitud de la cadena resultante siempre es exactamente `endIndex - beginIndex`.

### 3. Evolución del caso guía a ControlAccesoQR v1.8 (35 min)

Actualización conjunta a `ControlAccesoQR v1.8`. Los estudiantes abren el archivo maestro para blindar y formatear las entradas de texto introducidas en el escáner:

* **Paso A. Algoritmo en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc — v1.8`)**:
    * Implementación lógica utilizando funciones nativas como `Mayusculas(texto)` y `Subcadena(texto, inicio, fin)` para normalizar el DNI y el perfil del visitante introducido por consola.

* **Paso B. Implementación en Java (`pr/src/ControlAccesoQR.java — v1.8`)**:
    * Refactorización: Reasignación de las variables justo después de ser leídas, aplicando los métodos de limpieza en bloque:
      ```java
      dniPersona = dniPersona.trim().toUpperCase();
      ```
    * Uso de `substring()` para generar un identificador corto en el ticket (por ejemplo, extrayendo los tres primeros caracteres del nombre y concatenándolos).

## ⚙️ Sesión 2 (50 min). PR - Dojo de entrenamiento y katas de código

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 1. Segunda sesión: dojo de entrenamiento y katas de código (45 min)

Cada estudiante trabaja de forma autónoma sobre la versión `v1.8` de su proyecto elegido, aplicando transformaciones estrictas a las cadenas de su dominio:

* **Kata 1 (Cinturón blanco / Nivel base). Transformación y extracción en tu proyecto propio:** 
    * Invocar métodos para forzar el formato del texto y reasignarlo correctamente.
    * En *Aventura*: Forzar el nombre del avatar a mayúsculas y limpiarlo de espacios indeseados.
    * En *Motor de recomendación*: Extraer las tres primeras letras del título de una película (`substring(0, 3)`) para generar un código interno.
    * En *Simulador de físicas*: Normalizar el comando de simulación (ej. "GRAVEDAD") a minúsculas absolutas.
    * En *Bóveda de contraseñas*: Extraer el prefijo (ej. primeros 4 caracteres) del nombre del servicio.
* **Kata 2 (Cinturón marrón / Nivel avanzado). La regla del endIndex y el troceado dinámico:** Utilizar el método `indexOf()` aprendido en la sesión anterior para localizar un separador (por ejemplo, un espacio o un guion) y combinarlo matemáticamente con `substring()` para extraer dinámicamente la segunda palabra de un texto ingresado, sin importar su longitud.
* **Kata 3 (Cinturón negro / «Hacker AzaharTech»). La trampa de la inmutabilidad y el encadenamiento:** Demostrar el error común de invocar `texto.toUpperCase();` sin guardarlo en una variable, evidenciando que el objeto original no muta en el Heap. A continuación, refactorizarlo utilizando **encadenamiento de métodos** (ej. `texto.trim().toUpperCase().replace("A", "X");`) y documentar cuántos objetos anónimos se crean y destruyen en el *String pool* en esa única línea de código.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendido el uso de métodos de normalización: trim, toUpperCase. ║
║ [ ] Dominada la regla del endIndex exclusivo en el método substring(). ║
║ [ ] Asimilada la diferencia entre alterar y reasignar (inmutabilidad). ║
║ [ ] Evolucionada la versión v1.8 del proyecto propio sin errores.      ║
║ [ ] Katas de troceado dinámico y encadenamiento en el pool superadas.  ║
╚════════════════════════════════════════════════════════════════════════╝
```