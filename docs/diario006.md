---
title: "Jueves 17 de septiembre de 2026 - Buenas prácticas de código y consolidación v0.3"
date: 2026-09-17
modules: "Programación (PR)"
duration: "2 horas lectivas (100 minutos)"
layout: page
---

# 🚀 Diario de clase: jueves, 17 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027
**Módulo del día:** Programación (PR)  
**Fecha:** Jueves, 17 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

---

## 🧭 Sesión 1. Estándares de calidad de código, autoformateo e inspección en IntelliJ
*Balance de tiempo:* **Docente: 15 min | Estudiante: 35 min**

### 1. Contexto profesional en AzaharTech (5 min)
* Alba Torres y Laia Claramunt revisan en el proyector el código de `ControlAccesoQR.java` alcanzado ayer (versión v0.3).
* El motor de cálculo de estancia funciona a la perfección, pero Laia señala detalles visuales: líneas desalineadas, llaves en posiciones inconsistentes y una advertencia amarilla en el editor sobre el objeto `Scanner` abierto.
* Alba recuerda al equipo: *«En AzaharTech no basta con que el código funcione; el código debe ser legible, seguir las convenciones oficiales de Java y quedar impecablemente estructurado antes de enviarlo al repositorio»*.

### 2. Micro-exposición docente: Limpieza, indentación y comentarios (10 min)
* **Convenciones de nomenclatura oficiales:**
  * *PascalCase* para clases (`ControlAccesoQR`, `MiProyecto`).
  * *camelCase* para variables y métodos (`minutosEstanciaTotal`, `horaEntrada`).
  * Nombres autoexplicativos: evitar variables de una sola letra como `h`, `m` o `t`.
* **Indentación y formateo automático en el IDE:**
  * En Java el estándar son 4 espacios por cada bloque anidado dentro de llaves `{ }`.
  * Atajo universal de IntelliJ IDEA: **`Ctrl + Alt + L`** (en GNU/Linux). Reorganiza y alinea todo el archivo al instante.
* **Gestión de recursos:**
  * La clase `Scanner` abre un flujo de lectura del sistema operativo. Al terminar de usarlo en el `main`, debe cerrarse con `teclado.close();` para evitar advertencias de fuga de recursos (*resource leak*).
* **Comentarios explicativos de línea (`//`):**
  * Se usan para explicar el *porqué* de una fórmula o decisión técnica, no para describir lo que ya es evidente.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   ESTÁNDARES DE LIMPIEZA EN INTELLIJ                   │
├──────────────────────────────────┬─────────────────────────────────────┤
│ Ctrl + Alt + L                   │ Autoformatear e indentar el código  │
│ Barra lateral derecha (icono)    │ Visto verde: «No problems found»    │
│ teclado.close();                 │ Cierre formal del canal de lectura  │
└──────────────────────────────────┴─────────────────────────────────────┘
```

### 3. Taller guiado: Refactorización y pulido de `ControlAccesoQR v0.3` (25 min)
*Los estudiantes abren su archivo `ControlAccesoQR.java`, aplican las herramientas de formateo y añaden comentarios técnicos explicativos:*

* **Java (`pr/src/ControlAccesoQR.java` - v0.3 consolidada):**
  ```java
  /**
   * SISTEMA DE CONTROL DE ASISTENCIA POR CÓDIGO QR
   * Cliente: IES El Caminàs (Castellón de la Plana)
   * Consultora: AzaharTech Software Consulting
   * 
   * Versión 0.3: Captura completa de datos, cálculo de estancia horaria y formato limpio.
   * Módulo: Programación (PR) - Sprint 1 (RA1)
   */
  import java.util.Scanner;

  public class ControlAccesoQR {
      public static void main(String[] args) {
          // Canal de lectura de la entrada estándar
          Scanner teclado = new Scanner(System.in);

          // 1. Variables del terminal físico (Día 1)
          int terminalId;
          double tempVestibulo;

          // 2. Variables de identidad del usuario (Día 2)
          String dniPersona;
          String nombrePersona;
          char perfilPersona;
          boolean esEntrada;

          // 3. Variables de registro horario y estancia (Día 3)
          int horaEntrada;
          int minutoEntrada;
          int horaSalida;
          int minutoSalida;
          int minutosTotalesEntrada;
          int minutosTotalesSalida;
          int minutosEstanciaTotal;
          String tokenResumen;

          // Entrada de datos del hardware y usuario
          System.out.println("=================================================");
          System.out.println("   AZAHARTECH - TERMINAL DE ACCESO VESTÍBULO     ");
          System.out.println("   Cliente: IES El Caminàs (Curso 2026/2027)     ");
          System.out.println("=================================================");
          System.out.print("ID del terminal: ");
          terminalId = teclado.nextInt();

          System.out.print("Temperatura del sensor (ºC): ");
          tempVestibulo = teclado.nextDouble();
          teclado.nextLine(); // Limpieza obligatoria del buffer de entrada

          System.out.print("DNI de la persona: ");
          dniPersona = teclado.nextLine();

          System.out.print("Nombre completo: ");
          nombrePersona = teclado.nextLine();

          System.out.print("Perfil de acceso (E = Estudiante, D = Docente, V = Visita): ");
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

          // Conversión a minutos transcurridos
          minutosTotalesEntrada = (horaEntrada * 60) + minutoEntrada;
          minutosTotalesSalida = (horaSalida * 60) + minutoSalida;

          // Cálculo directo del tiempo total de permanencia en el centro
          minutosEstanciaTotal = minutosTotalesSalida - minutosTotalesEntrada;

          // Composición de cadena identificativa del registro
          tokenResumen = dniPersona + "-ESTANCIA-" + minutosEstanciaTotal;

          // Salida con formato
          System.out.println("---------------------------------------------");
          System.out.println("Terminal configurado:        #" + terminalId);
          System.out.println("Sensor termico:              " + tempVestibulo + " ºC)");
          System.out.println("Persona:                     " + nombrePersona + " (DNI: " + dniPersona + ")");
          System.out.println("Perfil:                      " + perfilPersona);
          System.out.println("Sentido del paso:            Entrada (" + esEntrada + ")");
          System.out.println("Token:                       " + tokenResumen);
          System.out.println("Horario:                     Entrada " + horaEntrada + ":" + minutoEntrada + " | Salida " + horaSalida + ":" + minutoSalida);
          System.out.println("Permanencia total en centro: " + minutosEstanciaTotal + " minutos.");
    
          // Cierre del recurso para evitar advertencias del compilador
          teclado.close();
      }
  }
  ```

### 4. Dinámica de inspección de código (10 min)
* Cada estudiante pulsa `Ctrl + Alt + L` en su IntelliJ para observar cómo se reordenan automáticamente los márgenes y operadores.
* Revisan la esquina superior derecha del editor: debe mostrar el icono del visto en verde (*«No problems found»*), acreditando que no hay advertencias de estilo.

---

## ⚙️ Sesión 2. Consolidación y versionado visual del proyecto propio (v0.3)
*Balance de tiempo:* **Docente: 10 min | Estudiante: 40 min**

### 1. Pautas técnicas de auditoría antes del guardado (10 min)
* El docente explica los 4 criterios de aceptación que debe cumplir el archivo `MiProyecto.java` para dar por superada la primera semana:
    1. Compilación limpia sin dependencias rotas.
    2. Nombres de variables autoexplicativos en *camelCase*.
    3. Cálculo secuencial con paréntesis protectores funcionando en consola.
    4. Código autoformateado y recurso `Scanner` cerrado.

### 2. Trabajo autónomo en puesto individual (35 min)
* Cada estudiante abre su archivo único en IntelliJ (`pr/src/MiProyecto.java`) y en PSeInt (`pr/pseudocodigo/MiProyecto.psc`).
* Aplica la auditoría completa sobre su proyecto propio:
    1. Revisa que el algoritmo de PSeInt y el código Java de la versión v0.3 son equivalentes.
    2. Añade comentarios explicativos en la cabecera y en las operaciones de cálculo.
    3. Ejecuta dos pruebas consecutivas en consola con datos reales de su temática para confirmar que la salida no presenta errores.
* **Subida a GitHub desde la interfaz de IntelliJ:**
    1. Pulsa el atajo **`Ctrl + K`** (o haz clic en el icono verde de verificación **Commit** en la barra lateral izquierda).
    2. En el panel de Commit, marca las casillas de los archivos modificados dentro de `pr/` (`MiProyecto.java` y `MiProyecto.psc`).
    3. En la caja de texto para el mensaje, escribe siguiendo el estándar convencional:  
       `feat(pr): consolidar version v0.3 con captura de datos, calculos aritmeticos y limpieza de codigo`
    4. Despliega el botón azul inferior y selecciona **«Commit and Push»**.
    5. En la ventana de confirmación que aparece, pulsa **Push** para enviar los cambios a GitHub.

```text
┌────────────────────────────────────────────────────────────────────────┐
│               FLUJO DE GUARDADO Y SINCRONIZACIÓN EN INTELLIJ           │
├────────────────────────────────────────────────────────────────────────┤
│ 1. Ctrl + K                       ──► Abre el panel visual de Commit.  │
│ 2. Marcar casillas de pr/         ──► Prepara los archivos (Stage).    │
│ 3. Escribir mensaje convencional  ──► Describe el cambio realizado.    │
│ 4. Pulsar «Commit and Push»       ──► Graba en local y sube a GitHub.  │
└────────────────────────────────────────────────────────────────────────┘
```

### 3. Cierre y verificación en GitHub (5 min)
* Comprobación en el navegador web de que la versión v0.3 de `MiProyecto.java` y su pseudocódigo están visibles y con su commit registrado en el repositorio remoto.

---

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Aplicadas las convenciones de estilo oficiales (camelCase/Pascal). ║
║ [ ] Código autoformateado en IntelliJ mediante Ctrl + Alt + L.         ║
║ [ ] Resuelto el cierre formal del recurso Scanner con .close().        ║
║ [ ] Caso guía ControlAccesoQR consolidado en su versión v0.3 limpia.   ║
║ [ ] Versión v0.3 de MiProyecto.java y pseudocódigo subidos a GitHub.   ║
╚════════════════════════════════════════════════════════════════════════╝
```
