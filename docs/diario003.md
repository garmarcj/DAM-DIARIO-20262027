---
title: "Lunes 14 de septiembre de 2026 - Inicio del sprint 1"
date: 2026-09-14
modules: "Programación (PR) + Entornos de desarrollo (ED)"
duration: "4 horas lectivas (200 minutos)"
layout: page
---

# 🚀 Diario de clase: lunes, 14 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027
**Módulos:** Programación (PR) + Entornos de desarrollo (ED)  
**Fecha:** Lunes, 14 de septiembre de 2026  
**Duración:** 4 horas lectivas (200 min)

---

## 🧭 Sesión 1. PR - Pensamiento computacional y variables numéricas primitivas
*Balance de tiempo:* **Docente: 15 min | Estudiante: 35 min**

### 1. Contexto profesional en AzaharTech (5 min)
* Arranque del caso guía: sistema de control de acceso por QR para el **IES El Caminàs**.
* Laia Claramunt presenta el reto del día: el terminal debe capturar y registrar en la memoria RAM su número y la lectura térmica del vestíbulo.

### 2. Micro-exposición docente (10 min)
* Qué es un algoritmo: secuencia ordenada Entrada $\rightarrow$ Proceso $\rightarrow$ Salida (modelo IPO).
* Anatomía básica de un archivo Java:
  ```java
  public class ControlAccesoQR {
      public static void main(String[] args) {
          // Instrucciones secuenciales
      }
  }
  ```
* Variables en memoria RAM: identificador en *camelCase* y tipo de dato.
* Tipos numéricos primitivos: `int` (enteros de 32 bits) y `double` (reales con decimales de 64 bits).

### 3. Andamiaje guiado: PSeInt ➔ Java (25 min)
*Los estudiantes diseñan en PSeInt y traducen inmediatamente a Java en IntelliJ:*

* **PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc` - v0.1):**
  ```psc
  Algoritmo ControlAccesoQR
      Definir terminalId Como Entero
      Definir tempVestibulo Como Real
      
      Escribir "ID del terminal:"
      Leer terminalId
      Escribir "Temperatura sensor (ºC):"
      Leer tempVestibulo
      
      Escribir "Terminal configurado: #", terminalId
      Escribir "Sensor termico: ", tempVestibulo, " ºC"
  FinAlgoritmo
  ```
* **Java (`pr/src/ControlAccesoQR.java` - v0.1):**
  ```java
  import java.util.Scanner;

  public class ControlAccesoQR {
      public static void main(String[] args) {
          Scanner teclado = new Scanner(System.in);
          
          int terminalId;
          double tempVestibulo;
          
          System.out.print("ID del terminal: ");
          terminalId = teclado.nextInt();
          
          System.out.print("Temperatura sensor (ºC): ");
          tempVestibulo = teclado.nextDouble();
          
          System.out.println("Terminal configurado: #" + terminalId);
          System.out.println("Sensor térmico: " + tempVestibulo + " ºC");
          
          teclado.close();
      }
  }
  ```

### 4. Puesta en común (10 min)
* Resolución de dudas en pantalla: la importancia del punto y coma (`;`), coincidencia exacta del nombre de archivo y clase, y el cierre de llaves `{}`.

---

## ⚙️ Sesión 2 (50 min). PR - Entrada de datos y aplicación al proyecto propio
*Balance de tiempo:* **Docente: 10 min | Estudiante: 40 min**

### 1. Pautas técnicas para el proyecto propio (10 min)
* El docente explica cómo extrapolar las variables numéricas a los proyectos de la bolsa (por ejemplo: horas de cómputo en *Cotizador cloud*, segundos de reacción en *Simulador de phishing*, masa/radio en *Simulador de físicas 2D*).

### 2. Trabajo del estudiante en el proyecto propio (35 min)
* Cada estudiante crea en su espacio personal (`azahartech/nombre-equipo/apellidos-nombre/pr/`):
    1. `pr/pseudocodigo/MiProyecto.psc` (versión v0.1).
    2. `pr/src/MiProyecto.java` (versión v0.1).
* Declara al menos una variable `int` y una variable `double` representativas de su proyecto.
* Captura datos mediante `Scanner` y muestra la confirmación por consola.
* El docente circula por el aula resolviendo incidencias individuales de tipado y lectura.

### 3. Cierre de la sesión de programación (5 min)
* Comprobación en consola de que el código compila y ejecuta sin errores (`Ctrl + Shift + F10`).

## 🧭 Sesión 3. ED - Sistema de información y ciclo de vida del software (SDLC)
*Balance de tiempo:* **Docente: 15 min | Estudiante: 35 min**

### 1. Micro-exposición docente (15 min)
* **Programa vs. Sistema de información:** Un programa es solo una pieza; un Sistema de Información (SI) articula 5 componentes: Hardware, Software, Datos, Personas y Procesos.
* **Ciclo de vida del software (SDLC):** Análisis $\rightarrow$ Diseño $\rightarrow$ Codificación $\rightarrow$ Pruebas $\rightarrow$ Despliegue $\rightarrow$ Mantenimiento.
* **La regla del coste de corrección:** Un error no detectado en el análisis cuesta hasta 100 veces más corregirlo en producción.

```text
┌─────────────────────────────────────────────────────────────────────────┐
│               LOS 5 COMPONENTES DE UN SISTEMA DE INFORMACIÓN            │
├───────────────────┬─────────────────────────────────────────────────────┤
│ 1. Hardware       │ Dispositivos físicos (pantallas, terminales, CPU).  │
│ 2. Software       │ Programas y backend en Java que desarrollamos.      │
│ 3. Datos          │ Materia prima (censos, registros, marcas de tiempo).│
│ 4. Personas       │ Usuarios finales, administradores y operadores.     │
│ 5. Procesos       │ Reglas operativas y normativas de la organización.  │
└───────────────────┴─────────────────────────────────────────────────────┘
```

### 2. Actividad. Identificación de componentes (20 min)
* Cada estudiante redacta en su libreta o en un archivo borrador el análisis de los 5 componentes aplicados al proyecto que eligió de la bolsa de proyectos.
* Debe identificar:
    * Al menos 2 dispositivos de hardware requeridos.
    * Qué datos en bruto manejará su aplicación.
    * Dos perfiles de personas (usuarios) distintos.
    * Un proceso de negocio claro que el software automatizará.

### 3. Puesta en común (15 min)
* Debate guiado: tres alumnos exponen sus componentes y el grupo analiza si se ha confundido algún dato con un proceso o un componente software con hardware.

---

## 🛠️ Sesión 4. Taller práctico de puesta a punto (OpenJDK 21 + IntelliJ IDEA)
*Balance de tiempo:* **Docente: 15 min | Estudiante: 35 min**

### 1. Fundamento técnico del entorno (15 min)
* Cómo funciona Java: Código fuente (`.java`) $\rightarrow$ Compilador `javac` $\rightarrow$ Bytecode (`.class`) $\rightarrow$ Máquina Virtual de Java (JVM).
* Principio WORA (*Write Once, Run Anywhere*).
* Anatomía de un IDE profesional: editor inteligente, gestor de compilación, depurador y control de versiones.

```text
 [ Código fuente (.java) ] ──(javac)──► [ Bytecode (.class) ] ──(JVM)──► [ Procesador / SO ]
```

### 2. Taller guiado (30 min)
* Cada estudiante realiza en su puesto de trabajo los siguientes pasos técnicos:
    1. Abre la terminal del sistema y verifica la instalación del compilador:
       ```bash
       java --version
       javac --version
       ```
    2. Abre **IntelliJ IDEA Community Edition**:
        * Configura la codificación global del proyecto en `UTF-8` (*Settings -> File Encodings*).
        * Asocia el SDK oficial a **OpenJDK 21**.
    3. Abre el archivo de tu proyecto y verifica que compila y ejecuta en la consola integrada.
    4. Realiza una captura completa de pantalla mostrando IntelliJ, el código y la terminal con `java --version`.
    5. Guarda la imagen con el nombre exacto **`entorno.png`** en su carpeta temporal (se moverá a su ruta definitiva en la sesión de Git).

### 3. Cierre y verificación de puestos (5 min)
* El docente comprueba visualmente que todos los puestos tienen OpenJDK 21 verificado y la captura `entorno.png` lista.

---

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Ecosistema de desarrollo verificado con OpenJDK 21 e IntelliJ.     ║
║ [ ] Evidencia 1 de Entornos de desarrollo generada (entorno.png).      ║
║ [ ] Comprendida la estructura de un programa Java y el modelo IPO.     ║
║ [ ] Asimilados los tipos primitivos int y double en memoria RAM.       ║
║ [ ] Primera versión (v0.1) del proyecto propio diseñada y compilada.   ║
╚════════════════════════════════════════════════════════════════════════╝
```

