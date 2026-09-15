---
title: "Martes 15 de septiembre de 2026 - Tipos alfanuméricos y gestión de memoria"
date: 2026-09-15
modules: "Programación (PR)"
duration: "2 horas lectivas (100 minutos)"
layout: page
---

# 🚀 Diario de clase: martes, 15 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027
**Módulo del día:** Programación (PR)
**Fecha:** Martes, 15 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

---

## 🧭 Sesión 1. Caracteres (`char`), cadenas (`String`), booleanos y el buffer de Scanner
*Balance de tiempo:* **Docente: 15 min | Estudiante: 35 min**

### 1. Contexto profesional en AzaharTech (5 min)
* Pau Ferrer ejecuta la versión v0.1 de ayer: el sistema registra el terminal `101` y la temperatura `21.5`, pero no tiene forma de identificar al estudiante que escanea.
* Laia Claramunt plantea el reto: necesitamos capturar el nombre de la persona, su DNI, el perfil de usuario y saber si está entrando o saliendo.

### 2. Micro-exposición docente: Memoria alfanumérica y lógica (10 min)
* **Carácter individual (`char`):** Ocupa 16 bits (Unicode) y se delimita siempre con comillas simples (`'A'`).
* **Cadena de texto (`String`):** Objeto que almacena secuencias de texto de cualquier longitud, delimitado con comillas dobles (`"Laura Vidal"`).
* **Valor lógico (`boolean`):** Solo admite dos literales reservados: `true` o `false`.
* **La trampa del buffer de teclado en `Scanner`:**
  * Al teclear un número y pulsar *Enter*, el método `nextInt()` lee el número pero deja el salto de línea (`\n`) flotando en el buffer.
  * Si a continuación se invoca `nextLine()`, este lee el `\n` residual y cree que el usuario introdujo una línea vacía.
  * **Solución:** Intercalar una llamada de limpieza previa con `teclado.nextLine();`.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        GESTIÓN DEL BUFFER EN SCANNER                   │
├────────────────────────────────────────────────────────────────────────┤
│ 1. teclado.nextInt();     ──► Lee el número, deja el '\n' en buffer.   │
│ 2. teclado.nextLine();    ──► Limpieza obligatoria: consume el '\n'.   │
│ 3. teclado.nextLine();    ──► Lee ahora sí el texto real del usuario.  │
└────────────────────────────────────────────────────────────────────────┘
```

### 3. Andamiaje guiado: Evolución a `ControlAccesoQR v0.2` (25 min)
*Los estudiantes abren el archivo de ayer y lo amplían directamente en PSeInt y en IntelliJ:*

* **PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc` - v0.2):**
  ```psc
  Algoritmo ControlAccesoQR
      Definir terminalId Como Entero
      Definir tempVestibulo Como Real
      
      Definir nombrePersona, dniPersona Como Cadena
      Definir perfilPersona Como Caracter
      Definir esEntrada Como Logico
      
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
      
      Escribir "Terminal configurado: #", terminalId
      Escribir "Sensor termico: ", tempVestibulo, " ºC"
      Escribir "Persona: ", nombrePersona, " (DNI: ", dniPersona, ")"
      Escribir "Perfil: ", perfilPersona
      Escribir "Sentido del paso:  Entrada (", esEntrada, ")"
  FinAlgoritmo
  ```

* **Java (`pr/src/ControlAccesoQR.java` - v0.2):**
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

          System.out.println("Terminal configurado: #" + terminalId);
          System.out.println("Sensor termico: " + tempVestibulo + " ºC)");
          System.out.println("Persona: " + nombrePersona + " (DNI: " + dniPersona + ")");
          System.out.println("Perfil: " + perfilPersona);
          System.out.println("Sentido del paso:  Entrada (" + esEntrada + ")");
          
          teclado.close();
      }
  }
  ```

### 4. Provocando el error del buffer (10 min)
* Cada estudiante comenta voluntariamente la línea de limpieza `// teclado.nextLine();` en su código y ejecuta el programa.
* Comprueban en pantalla cómo el programa se salta la lectura del nombre. Vuelven a descomentar la línea para interiorizar la solución.

---

## ⚙️ Sesión 2. Evolución acumulativa en el proyecto propio (v0.2)
*Balance de tiempo:* **Docente: 10 min | Estudiante: 40 min**

### 1. Pautas técnicas de adaptación a los proyectos de la bolsa (10 min)
* El docente explica cómo trasladar los tipos alfanuméricos (String, char) y booleanos (boolean) a las cuatro temáticas:
  * En Aventura conversacional: nombre del héroe (String), clase de personaje 'G', 'M', 'P' (char) y si la partida está activa (boolean estaVivo). 
  * En Motor de recomendación: título de la película/libro (String), tipo de contenido 'P', 'M', 'L' (char) y si está marcado como favorito (boolean esFavorito). 
  * En Simulador de físicas 2D: etiqueta del cuerpo (String), tipo de partícula 'N', 'P', 'R' (char) y si tiene la gravedad activada (boolean gravedadActiva). 
  * En Bóveda de contraseñas: nombre del servicio o web (String), nivel de política 'B', 'E', 'C' (char) y si requiere doble factor (boolean requiere2FA).

### 2. Trabajo autónomo en puesto individual (35 min)
* Cada estudiante abre su archivo único en IntelliJ (`pr/src/MiProyecto.java`) y en PSeInt (`pr/pseudocodigo/MiProyecto.psc`).
* Evoluciona el código de la v0.1 a la **v0.2**:
    1. Mantiene las variables numéricas creadas ayer.
    2. Declara al menos una variable `String`, una `char` y una `boolean`.
    3. Aplica la captura con `Scanner` asegurando la limpieza del buffer.
    4. Muestra un resumen claro en consola.
* El docente circula resolviendo dudas de lectura de caracteres individuales y variables lógicas.

### 3. Cierre y verificación técnica (5 min)
* Comprobación en consola de que el programa permite teclear nombres con espacios sin fallos de compilación.

---

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Asimiladas las diferencias entre char (Unicode) y String (texto).  ║
║ [ ] Comprendido el uso de variables lógicas boolean (true/false).      ║
║ [ ] Resuelto y probado el problema del buffer residual en Scanner.     ║
║ [ ] Caso guía ControlAccesoQR evolucionado a la versión v0.2.          ║
║ [ ] Archivo MiProyecto.java del proyecto propio actualizado a v0.2.    ║
╚════════════════════════════════════════════════════════════════════════╝
```
```