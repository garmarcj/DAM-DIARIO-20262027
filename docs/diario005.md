---
title: "Miércoles 16 de septiembre de 2026 - Operadores aritméticos y cálculo de estancia"
date: 2026-09-16
modules: "Programación (PR)"
duration: "2 horas lectivas (100 minutos)"
layout: page
---

# 🚀 Diario de clase: miércoles, 16 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027
**Módulo del día:** Programación (PR)  
**Fecha:** Miércoles, 16 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

---

## 🧭 Sesión 1. Operadores aritméticos elementales, cálculo de estancia y concatenación
*Balance de tiempo:* **Docente: 15 min | Estudiante: 35 min**

### 1. Contexto profesional en AzaharTech (5 min)
* Pau Ferrer intenta mostrar en una sola línea los minutos totales del día calculados para una entrada a las `08:15`.
* Ha multiplicado `8 * 60` (480) y le ha sumado los `15` minutos, pero al imprimirlo directamente junto al texto ha obtenido en pantalla: `Minutos de entrada: 48015 min`.
* Alba Torres y Laia Claramunt explican que el operador `+` evalúa de izquierda a derecha; al encontrar texto primero, convierte los números a texto y los concatena en lugar de sumarlos.

### 2. Micro-exposición docente: Aritmética, precedencia y cálculo temporal (10 min)
* **Operadores aritméticos binarios:** Multiplicación (`*`), suma (`+`), resta (`-`).
* **Conversión horaria a minutos:**
  * Para operar con horas y minutos, convertimos todo a una unidad común (minutos transcurridos desde medianoche):
    $$\text{minutos} = (\text{hora} \times 60) + \text{minuto}$$
  * Entrada a las `08:15` $\rightarrow (8 \times 60) + 15 = 480 + 15 = 495\text{ minutos}$.
  * Salida a las `14:10` $\rightarrow (14 \times 60) + 10 = 840 + 10 = 850\text{ minutos}$.
* **Cálculo del tiempo total de estancia en el instituto:**
  * Resta secuencial directa:
    $$\text{minutosEstancia} = \text{minutosSalida} - \text{minutosEntrada}$$
    $$850 - 495 = 355\text{ minutos de permanencia en el centro}.$$
* **La trampa de la concatenación:**
  * `"Minutos: " + 480 + 15` produce `"Minutos: 48015"` (concatenación).
  * `"Minutos: " + (480 + 15)` produce `"Minutos: 495"` (suma prioritaria con paréntesis).

```text
┌────────────────────────────────────────────────────────────────────────┐
│                  EVALUACIÓN DEL OPERADOR '+' EN JAVA                   │
├──────────────────────────────────┬─────────────────────────────────────┤
│ 480 + 15                         │ 495 (Suma aritmética de enteros)    │
│ "Minutos: " + 480 + 15           │ "Minutos: 48015" (Texto concatenado)│
│ "Minutos: " + (480 + 15)         │ "Minutos: 495" (Suma prioritaria)   │
└──────────────────────────────────┴─────────────────────────────────────┘
```

### 3. Andamiaje guiado: Evolución a `ControlAccesoQR v0.3` (25 min)
*Los estudiantes abren el archivo de ayer y lo amplían directamente en PSeInt y en IntelliJ:*

* **PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc` - v0.3):**
  ```psc
  Algoritmo ControlAccesoQR
      Definir terminalId Como Entero
      Definir tempVestibulo Como Real
      
      Definir nombrePersona, dniPersona Como Cadena
      Definir perfilPersona Como Caracter
      Definir esEntrada Como Logico
      
      Definir horaEntrada, minutoEntrada Como Entero
      Definir horaSalida, minutoSalida Como Entero
      Definir minutosTotalesEntrada Como Entero
      Definir minutosTotalesSalida Como Entero
      Definir minutosEstanciaTotal Como Entero
      Definir tokenResumen Como Cadena
      
      Escribir "ID del terminal:"
      Leer terminalId
      Escribir "Temperatura del sensor (ºC):"
      Leer tempVestibulo
      
      Escribir "DNI de la persona:"
      Leer dniPersona
      Escribir "Nombre completo:"
      Leer nombrePersona
      Escribir "Perfil de acceso (E = Estudiante, D = Docente, V = Visita):"
      Leer perfilPersona
      
      esEntrada <- Verdadero
      
      Escribir "Introduce hora y minuto de entrada (por ejemplo, 8 15):"
      Leer horaEntrada
      Leer minutoEntrada
      
      Escribir "Introduce hora y minuto de salida (por ejemplo, 14 10):"
      Leer horaSalida
      Leer minutoSalida
      
      minutosTotalesEntrada <- (horaEntrada * 60) + minutoEntrada
      minutosTotalesSalida <- (horaSalida * 60) + minutoSalida
      minutosEstanciaTotal <- minutosTotalesSalida - minutosTotalesEntrada
      
      tokenResumen <- dniPersona + "-ESTANCIA-" + ConvertirATexto(minutosEstanciaTotal)
      
      Escribir "Terminal configurado: #", terminalId
      Escribir "Sensor termico: ", tempVestibulo, " ºC"
      Escribir "Persona: ", nombrePersona, " (DNI: ", dniPersona, ")"
      Escribir "Perfil: ", perfilPersona
      Escribir "Sentido del paso:  Entrada (", esEntrada, ")"
      Escribir "Token:      ", tokenResumen
      Escribir "Horario:    Entrada ", horaEntrada, ":", minutoEntrada, " | Salida ", horaSalida, ":", minutoSalida
      Escribir "Permanencia total en centro: ", minutosEstanciaTotal, " minutos."
  FinAlgoritmo
  ```

* **Java (`pr/src/ControlAccesoQR.java` - v0.3):**
  ```java
  import java.util.Scanner;

  public class ControlAccesoQR {
      public static void main(String[] args) {
          Scanner teclado = new Scanner(System.in);
          
          int terminalId;
          double tempVestibulo;
          
          String dniPersona;
          String nombrePersona;
          char perfilPersona;
          boolean esEntrada;
          
          int horaEntrada;
          int minutoEntrada;
          int horaSalida;
          int minutoSalida;
          int minutosTotalesEntrada;
          int minutosTotalesSalida;
          int minutosEstanciaTotal;
          String tokenResumen;
          
          System.out.print("ID del terminal: ");
          terminalId = teclado.nextInt();
          
          System.out.print("Temperatura del sensor (ºC): ");
          tempVestibulo = teclado.nextDouble();
          teclado.nextLine();
          
          System.out.print("DNI de la persona: ");
          dniPersona = teclado.nextLine();
          
          System.out.print("Nombre completo: ");
          nombrePersona = teclado.nextLine();
          
          System.out.print("Perfil de acceso (E = Estudiante, D = Docente, V = Visita):");
          perfilPersona = teclado.next().charAt(0);
          
          esEntrada = true;
          
          System.out.print("Hora de entrada (0-23): ");
          horaEntrada = teclado.nextInt();
          
          System.out.print("Minuto de entrada (0-59): ");
          minutoEntrada = teclado.nextInt();
          
          System.out.print("Hora de salida (0-23): ");
          horaSalida = teclado.nextInt();
          
          System.out.print("Minuto de salida (0-59): ");
          minutoSalida = teclado.nextInt();
          
          minutosTotalesEntrada = (horaEntrada * 60) + minutoEntrada;
          minutosTotalesSalida = (horaSalida * 60) + minutoSalida;
          minutosEstanciaTotal = minutosTotalesSalida - minutosTotalesEntrada;
          
          tokenResumen = dniPersona + "-ESTANCIA-" + minutosEstanciaTotal;
          
          System.out.println("Terminal configurado: #" + terminalId);
          System.out.println("Sensor termico: " + tempVestibulo + " ºC)");
          System.out.println("Persona: " + nombrePersona + " (DNI: " + dniPersona + ")");
          System.out.println("Perfil: " + perfilPersona);
          System.out.println("Sentido del paso:  Entrada (" + esEntrada + ")");
          System.out.println("Token: " + tokenResumen);
          System.out.println("Horario:    Entrada " + horaEntrada + ":" + minutoEntrada + " | Salida " + horaSalida + ":" + minutoSalida);
          System.out.println("Permanencia total en centro: " + minutosEstanciaTotal + " minutos.");
          
          teclado.close();
      }
  }
  ```

### 4. Provocando el error de concatenación (10 min)
* Cada estudiante elimina temporalmente los paréntesis exteriores en la línea de impresión:
  `System.out.println("Minutos entrada: " + (horaEntrada * 60) + minutoEntrada + " min.");`
* Comprueban cómo una entrada a las `08:15` imprime erróneamente `48015 min`. Vuelven a colocar los paréntesis protectores para fijar el concepto.

---

## ⚙️ Sesión 2. Evolución acumulativa en el proyecto propio (v0.3)
*Balance de tiempo:* **Docente: 10 min | Estudiante: 40 min**

### 1. Pautas técnicas de adaptación a los proyectos de la bolsa (10 min)
* El docente muestra cómo trasladar la combinación de multiplicación, suma y resta a los proyectos individuales:
  * En *Cotizador cloud:* multiplicar horas por precio base y restar el cupón de descuento inicial.
  * En *Simulador de phishing:* multiplicar intentos por tiempo medio y restar bonificaciones por rapidez.
  * En *Simulador de físicas 2D:* calcular la diferencia de posición restando la posición inicial a la posición final calculada.

### 2. Trabajo autónomo en puesto individual (35 min)
* Cada estudiante abre su archivo único en IntelliJ (`pr/src/MiProyecto.java`) y en PSeInt (`pr/pseudocodigo/MiProyecto.psc`).
* Evoluciona el código de la v0.2 a la **v0.3**:
  1. Mantiene todas las variables numéricas, alfanuméricas y booleanas previas.
  2. Añade las variables necesarias para capturar dos instantes o cantidades parciales.
  3. Aplica multiplicación, suma y resta secuenciales.
  4. Muestra un mensaje unificado en consola utilizando paréntesis para proteger las operaciones matemáticas.
* El docente circula comprobando que la salida no presenta concatenaciones numéricas erróneas.

### 3. Cierre y verificación técnica (5 min)
* Comprobación en consola de que los cálculos se ejecutan limpiamente en IntelliJ.

---

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendida la sobrecarga del operador + (suma vs. concatenación). ║
║ [ ] Aplicada la jerarquía con paréntesis en expresiones combinadas.    ║
║ [ ] Realizadas operaciones aritméticas de multiplicación, suma y resta.║
║ [ ] Caso guía ControlAccesoQR evolucionado a la versión v0.3.          ║
║ [ ] Archivo MiProyecto.java del proyecto propio actualizado a v0.3.    ║
╚════════════════════════════════════════════════════════════════════════╝
```
```