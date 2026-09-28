# 🚀 Diario de clase: miércoles, 30 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Miércoles, 30 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1. PR - Especificadores de formato en System.out.printf()

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Pau Ferrer observa el ticket generado en la versión anterior. *«Las secuencias de escape han mejorado el diseño, pero al imprimir la temperatura del sensor térmico o el tiempo promedio de estancia, a veces salen números con demasiados decimales (ej. `21.533333333 ºC`), lo que rompe la alineación visual del ticket»*.
* Alba Torres interviene: *«El método `println()` encadena cadenas y números sin control sobre su representación. Para informes profesionales y tickets, en la industria utilizamos la impresión con formato: el método `System.out.printf()`. Hoy dejaremos de concatenar con el símbolo `+` y empezaremos a inyectar variables en plantillas de texto»*.

### 2. Fundamento teórico: especificadores de formato en System.out.printf() (10 min)

* **El concepto de plantilla e inyección:** Cómo `printf` separa el texto estático de las variables, utilizando comodines (especificadores de formato) que se rellenan secuencialmente.
* **Especificadores fundamentales en Java:**
    * `%d` : Para números enteros (`int`).
    * `%f` : Para números de coma flotante (`double`). Explicación del modificador de precisión, ej. `%.2f` para forzar exactamente dos decimales.
    * `%s` : Para cadenas de texto (`String`).
    * `%c` : Para caracteres simples (`char`).
    * `%n` : El salto de línea universal, seguro en cualquier sistema operativo (preferido sobre `\n` dentro de `printf`).

### 3. Evolución a ControlAccesoQR v0.9 (35 min)

Actualización conjunta a `ControlAccesoQR v0.9`. Los estudiantes abren el archivo maestro y refactorizan el bloque de salida final eliminando las concatenaciones tradicionales.

* **Paso A. Evolución en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v0.9`)**:
    * Aunque PSeInt no posee una función idéntica a `printf`, se asientan las bases algorítmicas de truncamiento o redondeo manual de las variables reales antes de imprimirlas para emular el control estricto de formato.

* **Paso B. Evolución en Java (`pr/src/ControlAccesoQR.java - v0.9`)**:
    * Sustitución de `System.out.println` por `System.out.printf` en el bloque del ticket de acceso.
    * Integración de los especificadores para redondear la temperatura a un decimal y alinear las variables:
      ```java
      System.out.printf("Temperatura del sensor: %.1f ºC%n", tempVestibulo);
      System.out.printf("Persona: %s (DNI: %s)%n", nombrePersona, dniPersona);
      ```

## ⚙️ Sesión 2 (50 min). PR - Aplicación al proyecto propio

**Balance de tiempo:** Docente: 10 min | Estudiante: 40 min

### 1. Trabajo del estudiante: evolución de su proyecto propio (40 min)

* Cada estudiante abre los archivos `.psc` y `.java` correspondientes a la versión `v0.8` de su proyecto elegido de la bolsa de proyectos y la evoluciona a `v0.9`.
* El objetivo es eliminar cualquier concatenación engorrosa con `+` en las salidas por pantalla finales y sustituirlas íntegramente por `System.out.printf()`, aplicando máscaras de formato específicas:
    * En **Aventura conversacional**: mostrar el porcentaje de salud del héroe o los multiplicadores de daño limitados a un decimal (`%.1f`).
    * En **Motor de recomendación**: imprimir la nota media de la película forzada a dos decimales (`%.2f`) e inyectar el título de la obra (`%s`).
    * En **Simulador de físicas 2D**: formatear la matriz de telemetría (velocidad, aceleración, masa) utilizando especificadores de número flotante para que todas las métricas queden perfectamente tabuladas.
    * En **Bóveda de contraseñas**: crear un reporte de seguridad inyectando el perfil del servicio y el nivel de entropía formateado como un porcentaje numérico exacto.
* El docente circula por el aula resolviendo errores comunes, como usar accidentalmente `%d` para intentar imprimir un `double` (lo que provoca una excepción de ejecución `IllegalFormatConversionException`) o el olvido del salto de línea `%n` al final de la instrucción.

### 2. Cierre de la sesión de programación (10 min)

* Comprobación en la consola integrada de IntelliJ (`Ctrl + Shift + F10`). Validación de que los números con decimales "infinitos" se han redondeado visualmente y el ticket aparece alineado de manera impecable y profesional.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendida la diferencia técnica entre println() y printf().      ║
║ [ ] Dominio de los especificadores %d, %f, %s, %c y %n.                ║
║ [ ] Aplicado el modificador %.2f para redondear salidas con decimales. ║
║ [ ] Evolucionada la versión v0.9 del proyecto propio sin errores.      ║
╚════════════════════════════════════════════════════════════════════════╝
```
```