# 🚀 Diario de clase: miércoles, 23 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Miércoles, 23 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

## 🧭 Sesión 1. PR - Precedencia de operadores y casting en Java

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Pau Ferrer quiere añadir una función al terminal para calcular el tiempo medio de permanencia de las visitas a lo largo del día. Escribe el código `double tiempoMedio = minutosTotales / totalAccesos;`. Sin embargo, al probarlo con `135` minutos y `2` accesos, el resultado por pantalla muestra `67.0` en lugar de `67.5`. ¡Se han perdido los decimales!
* Laia Claramunt interviene: *«El error no está en la variable `tiempoMedio`, que es un `double`. El problema es la precedencia y cómo funciona el motor interno de Java. Al dividir dos variables enteras (`int`), Java realiza una división entera y trunca el decimal **antes** de guardar el resultado. Hoy aprenderemos a forzar la conversión en memoria RAM mediante el **casting** explícito»*.

### 2. Precedencia de operadores y casting en Java (10 min)

* **A. Las conversiones de tipo en la memoria RAM**: Cómo Java realiza conversiones implícitas (de un tipo más pequeño a uno más grande, por ejemplo al guardar un valor `int` dentro de un `double`) y cuándo el lenguaje exige conversiones explícitas o *casting*.
* **B. La solución técnica mediante casting en divisiones**:
    * El uso de `(double)` antepuesto a una variable para convertir temporalmente su valor en la RAM a un número de coma flotante de 64 bits antes de que se ejecute la operación matemática: `(double) minutosTotales / totalAccesos;`.
    * **Precedencia de operadores**: Explicación de la jerarquía de evaluación. El *casting* tiene mayor prioridad que la multiplicación y la división, que a su vez se evalúan antes que la suma y la resta.

### 3. Evolución a ControlAccesoQR v0.6 (35 min)

Actualización conjunta a `ControlAccesoQR v0.6`. Los estudiantes abren el archivo maestro y añaden la lógica para calcular y mostrar métricas estadísticas con precisión decimal:

* **Paso A. Evolución en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v0.6`)**:
    * Se añade la lógica algorítmica para las medias matemáticas.

* **Paso B. Evolución en Java (`pr/src/ControlAccesoQR.java - v0.6`)**:
    * Implementación directa del casting en la fórmula de promedio:
      ```java
      double promedioEstancia = (double) minutosEstanciaTotal / contadorAccesos;
      ```
    * Actualización del bloque de `System.out.println` final para imprimir el dato estadístico comprobando que no hay pérdida de precisión (ej. `67.5 minutos`).

## ⚙️ Sesión 2 (50 min). PR - Aplicación al proyecto propio

**Balance de tiempo:** Docente: 10 min | Estudiante: 40 min

### 1. Trabajo del estudiante: evolución de su proyecto propio (40 min)

* Cada estudiante abre los archivos `.psc` y `.java` correspondientes a su proyecto propio y los evoluciona de la versión `v0.5` a la `v0.6`.
* El objetivo central es implementar una fórmula matemática que requiera una división exacta conservando decimales, aplicando obligatoriamente el *casting* explícito `(double)`:
    * En **Aventura conversacional**: calcular la media de daño infligido por turno o el ratio de precisión del jugador (`(double) impactosAcertados / totalAtaques`).
    * En **Motor de recomendación**: calcular la calificación media exacta de una serie basándose en la suma total de estrellas y el número de reseñas (`(double) sumaEstrellas / totalResenas`).
    * En **Simulador de físicas 2D**: calcular la velocidad media exacta dividiendo la distancia acumulada entre los ciclos o *ticks* de tiempo (`(double) distanciaTotal / ticksTiempo`).
    * En **Bóveda de contraseñas**: obtener el promedio de longitud de las claves registradas frente a una métrica entera (`(double) sumaLongitudes / totalClaves`).
* El docente circula resolviendo dudas individuales sobre la correcta ubicación de los paréntesis de precedencia y el operador de *casting*.

### 2. Cierre de la sesión de programación (10 min)

* Ejecución de pruebas en la consola integrada de IntelliJ (`Ctrl + Shift + F10`). Cada alumno debe forzar casos de prueba impares que generen decimales exactos (ej. `5 / 2 = 2.5`) para comprobar visualmente que su sistema no imprime el temido `.0`.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendida la precedencia de operadores matemáticos en Java.      ║
║ [ ] Dominado el uso del casting explícito (double) en divisiones.      ║
║ [ ] Solucionada la pérdida de precisión al operar con variables int.   ║
║ [ ] Evolucionada la versión v0.6 del proyecto propio sin errores.      ║
╚════════════════════════════════════════════════════════════════════════╝