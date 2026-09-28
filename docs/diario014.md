# 🚀 Diario de clase: martes, 29 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Martes, 29 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1. PR - Secuencias de escape en cadenas Java

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Pau Ferrer quiere mejorar la salida por consola para que el ticket de entrada sea mucho más visual. Intenta escribir comillas dobles dentro del texto para resaltar el perfil del usuario, pero el código no compila porque Java entiende que la cadena se ha cerrado. Además, quiere crear saltos de línea y tabulaciones sin usar múltiples `System.out.println`.
* Alba Torres interviene: *«El compilador no puede distinguir entre las comillas que cierran una cadena y las comillas que quieres imprimir. Para eso existen las **secuencias de escape**: caracteres invisibles que dan instrucciones de formato a la consola y permiten incluir símbolos reservados. Hoy las aplicaremos para diseñar un ticket estructurado»*.

### 2. Fundamento teórico: secuencias de escape en cadenas Java (10 min)

* **El carácter de escape `\` (barra invertida):** Su función principal es anular el significado especial del carácter que le sigue.
* **Secuencias fundamentales en Java:**
    * `\"` : Imprime unas comillas dobles literales.
    * `\n` : Genera un salto de línea (*newline*).
    * `\t` : Genera una tabulación horizontal para alinear textos y crear columnas.
    * `\\` : Imprime una barra invertida literal (muy útil para rutas de directorios).

### 3. Evolución a ControlAccesoQR v0.8 (35 min)

Actualización conjunta a `ControlAccesoQR v0.8`. Los estudiantes abren el archivo maestro y modifican el bloque de salida final por consola para formatear el resumen de acceso como un ticket oficial estructurado.

* **Paso A. Evolución en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v0.8`)**:
    * PSeInt maneja el formato de consola de forma distinta, pero se introducen textos espaciados para previsualizar y diseñar el ticket algorítmicamente.

* **Paso B. Evolución en Java (`pr/src/ControlAccesoQR.java - v0.8`)**:
    * Implementación de las secuencias `\n`, `\t` y `\"` dentro de los mensajes de salida, consolidando la información de manera más limpia:
      ```java
      System.out.println("\n--- TICKET DE ACCESO ---");
      System.out.println("Usuario:\t\"" + nombrePersona + "\"");
      System.out.println("Perfil:\t\t" + perfilPersona);
      System.out.println("------------------------\n");
      ```

## ⚙️ Sesión 2 (50 min). PR - Aplicación al proyecto propio

**Balance de tiempo:** Docente: 10 min | Estudiante: 40 min

### 1. Trabajo del estudiante: evolución de su proyecto propio (40 min)

* Cada estudiante abre los archivos `.psc` y `.java` correspondientes a la versión `v0.7` de su proyecto elegido de la bolsa de proyectos y la evoluciona a `v0.8`.
* El objetivo es rediseñar completamente la salida por pantalla utilizando las secuencias de escape (`\n`, `\t`, `\"`) para presentar un panel de datos ordenado y legible:
    * En **Aventura conversacional**: formatear la hoja de personaje alineando los atributos (vida, daño) con tabulaciones e imprimiendo el nombre del avatar entre comillas.
    * En **Motor de recomendación**: imprimir un ticket de reseña estructurado donde el título de la película o serie aparezca obligatoriamente entrecomillado.
    * En **Simulador de físicas 2D**: diseñar un panel de telemetría alineado en dos columnas mediante tabulaciones.
    * En **Bóveda de contraseñas**: simular una tabla visual en la terminal alineando los datos del servicio y resaltando la complejidad de la clave entre comillas.
* El docente circula por el aula asegurando que no se abuse de múltiples instrucciones `System.out.println()` donde una sola cadena extensa concatenada con `\n` sea más eficiente.

### 2. Cierre de la sesión de programación (10 min)

* Comprobación visual en la consola integrada de IntelliJ (`Ctrl + Shift + F10`). Se evalúa que las tabulaciones (`\t`) logren el efecto deseado alineando los datos como si fuesen columnas, y que las comillas literales (`\"`) se impriman sin romper la ejecución del archivo.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendido el uso del carácter de escape (\) y su función.        ║
║ [ ] Dominio de las secuencias \n, \t y \" para formatear la consola.   ║
║ [ ] Panel de salida rediseñado exitosamente en un bloque estructurado. ║
║ [ ] Evolucionada la versión v0.8 del proyecto propio sin errores.      ║
╚════════════════════════════════════════════════════════════════════════╝
```
```