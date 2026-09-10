---
title: "Jueves 10 de septiembre de 2026 - Presentación de Programación"
date: 2026-09-10
module: "Programación (PR)"
duration: "2 horas lectivas (100 minutos)"
layout: page
---

# 🚀 BIENVENIDA A AZAHARTECH
## 1.º DAM — Curso Académico 2026/2027
**Módulo:** Programación (PR)  
**Fecha:** Jueves, 10 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

---

## 🧭 Sesión 1. El marco profesional y las reglas

### 1. Presentación de AzaharTech (10 min)
* Os incorporáis como **desarrolladores junior** en la consultora de software **AzaharTech** (Castellón de la Plana).
* Trabajamos de forma coordinada entre **Programación**, **Entornos de Desarrollo** y **Proyecto Intermodular**.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                            ECOSISTEMA                                  │
├───────────────────┬──────────────────────────┬─────────────────────────┤
│ PROGRAMACIÓN (PR) │ ENTORNOS DESARROLLO (ED) │ PROYECTO INTERMODULAR   │
│   [8 h/semana]    │       [3 h/semana]       │       [1 h/semana]      │
│ Construcción del  │ Git, compilación, IDE,   │ Gestión del reto, IA,   │
│ código y lógica.  │ testing y calidad.       │ viabilidad y defensas.  │
└───────────────────┴──────────────────────────┴─────────────────────────┘
```

---

### 2. El caso guía: Sistema de control de asistencia con QR para el IES El Caminàs (5 min)
* **Proyecto.** Sistema de control de asistencia mediante códigos QR dinámicos mostrados en la pantalla del vestíbulo.
* **Propósito.** Es el proyecto de referencia que utilizará el docente para modelar los contenidos en la pizarra y en pantalla.
* **Importante.** **No es el proyecto que evaluará al alumno.** Cada grupo elegirá mañana su propio reto de la **Bolsa de Proyectos Oficial**.

> 🎙️ **Nota:** La app del instituto es el espejo donde mirar cómo se programa, pero cada estudiante desarrollará su propia aplicación a partir del lunes.

---

### 3. Las dos fases del curso y la estructura en Git (10 min)
Para garantizar un aprendizaje real y sin brechas:

| Periodo | Fase | Aula | Dinámica |
| :--- | :--- | :---: | :--- |
| **1.ᵉʳ Trimestre**<br>*(Sep – Dic)* | **Fase I**<br>«Desarrollador junior» | **Trabajo individual** | • Código 100 % propio.<br>• Exámenes y entregas individuales.<br>• Base sólida para todos. |
| **2.º Trimestre**<br>*(Ene – May)* | **Fase II**<br>«Equipo de consultoría» | **Trabajo en equipo** | • Metodología Scrum real.<br>• Reparto de tareas y backlog.<br>• Repositorio colaborativo. |

#### ¿Por qué existe la carpeta de equipo desde hoy?
```text
azahartech/
└── equipo-01/                   <-- Identificador asignado desde el primer día
    └── apellidos-nombre/        <-- Tu espacio personal e intransferible (T1)
        ├── ed/                  <-- Entornos de Desarrollo
        ├── pr/                  <-- Programación
        └── pi/                  <-- Proyecto Intermodular
```
* En enero tu equipo añadirá una carpeta común `proyecto-conjunto/` sin tener que renombrar carpetas ni romper rutas en IntelliJ y Git.

---

### 4. Actividad 1. Cuestionario de diagnóstico (10 min)

> 📲 **Acceso al cuestionario:**. Entra en Aules y rellena el cuestionario

---

### 5. Dudas y debate abierto (15 min)
* Turno de preguntas sobre la evaluación, el material necesario y el ritmo de trabajo del curso.

---

## ⚙️ Sesión 2. Pensamiento computacioanl y modelo IPO

### 1. Actividad 2. «El robot ciego» (20 min)
*Dinámica por parejas para experimentar qué es un algoritmo y por qué ocurren los errores de programación.*

```text
┌───────────────────────────┐         ┌───────────────────────────┐
│     EL PROGRAMADOR        │ ──────► │       EL ROBOT CIEGO      │
│  Escribe 5 instrucciones  │ órdenes │  Ejecuta de forma literal │
│  estrictas en un papel.   │         │  sin interpretar nada.    │
└───────────────────────────┘         └───────────────────────────┘
```

#### Reglas de la dinámica:
1. Por parejas, un estudiante asume el rol de **programador** y el otro de **robot**.
2. El programador escribe en un papel una secuencia de **exactamente 5 órdenes** para lograr que el robot coja un bolígrafo de la mesa y lo deposite dentro de una mochila sin tirarlo.
3. El robot ejecuta las órdenes de forma ciega y literal (si la orden es *"mueve el brazo hacia adelante"* y no indica cuántos centímetros, el robot se mueve hasta chocar).
4. **Puesta en común (5 min):** ¿Quién ha conseguido el objetivo al primer intento? ¿Por qué la máquina ha fallado cuando la instrucción parecía obvia?

> 💡 **Conclusión.** Un ordenador no interpreta intenciones; solo ejecuta instrucciones exactas sobre datos. Un algoritmo debe ser **preciso, ordenado y no ambiguo**.

---

### 2. El modelo universal de la informática: IPO (10 min)

Todo sistema informático responde a este esquema de tres fases consecutivas:

```text
┌─────────────────┐       ┌────────────────────────┐       ┌─────────────────┐
│ ENTRADA (Input) │ ────► │ PROCESAMIENTO (RAM/CPU)│ ────► │ SALIDA (Output) │
└─────────────────┘       └────────────────────────┘       └─────────────────┘
  • Teclado                 • Cálculos matemáticos           • Pantalla
  • Sensores                • Lógica de control              • Archivos / BD
  • Escáner QR              • Transformaciones               • Actuadores
```

* **Ejemplo del IES El Caminàs:**
    * *Entrada:* DNI del alumno + hora de lectura del QR.
    * *Procesamiento:* comprobar si la hora es posterior a las 08:05 h y calcular los minutos de retraso.
    * *Salida:* mensaje en pantalla («Puntual» en verde o «Retraso» en naranja) + registro en la base de datos.

Exact Instructions Challenge - video de Josh Darnit
https://www.youtube.com/watch?v=FN2RM-CHkuI

---

### 3. Actividad 3. Descomposición en papel (15 min)
*Dinámica individual con puesta en común (think-pair-share).*

1. **Piensa en solitario (5 min).** Elige un sistema que utilices a diario (cajero automático, máquina de café, barrera de parking, inicio de sesión en una app) y dibuja en tu libreta las 3 cajas:
    * ¿Qué datos introduce el usuario?
    * ¿Qué cálculos o verificaciones realiza la máquina internamente?
    * ¿Qué resultado devuelve?
2. **Compara con el compañero (5 min).** Intercambia la libreta con el compañero de al lado y comprueba su diagrama:
    * *«¿Qué ocurre si el usuario teclea mal el PIN?»*
    * *«¿Has indicado si el dato es un número o un texto?»*
3. **Puesta en común en la pizarra (5 min).** Dos alumnos voluntarios dibujan su esquema y el resto del aula propone casos límite.

---

### 4. Cierre del día 10 (5 min)

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DE HOY                          ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Presentado el funcionamiento y simulación de AzaharTech.           ║
║ [ ] Aclarada la fase individual del Trimestre 1 en el aula.            ║
║ [ ] Cuestionario de diagnóstico completado por todo el grupo.          ║
║ [ ] Asimilado el concepto de algoritmo y el modelo IPO.                ║                                                                        ║
╚════════════════════════════════════════════════════════════════════════╝
```
