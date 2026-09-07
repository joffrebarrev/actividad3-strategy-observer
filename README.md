# Actividad 3: Patrones de Comportamiento (Strategy & Observer)

Este repositorio contiene la solución e implementación de la **Actividad 3** para la materia de **Diseño de Software** (Universidad de Especialidades Espíritu Santo - UEES).

El proyecto demuestra el uso práctico y combinado de los patrones de diseño **Strategy** y **Observer** aplicados a un **Sistema de Gestión de Tutorías Universitarias** desarrollado en **Java 21** y gestionado con **Apache Maven**.

---

## 🎯 Objetivos del Proyecto

1. **Patrón Strategy (Estrategias de Cancelación):**
   - Permitir la modificación dinámica del comportamiento de cancelación de tutorías sin alterar la clase del contexto (`ServicioCancelacion`).
   - Implementar diferentes políticas de reembolso y restricciones temporales (Cancelación Normal, Prioritaria, Grupal y de Emergencia).

2. **Patrón Observer (Sistema de Notificaciones Multi-canal):**
   - Desacoplar el sujeto (`Reserva`) de sus suscriptores u observadores.
   - Notificar automáticamente a múltiples paneles y canales cuando el estado de una reserva cambia (Email, Calendario, Panel de Estudiante, Panel de Docente).

3. **Demostración de Retos:**
   - Incorporación de reglas de negocio extendidas (estrategias grupales/emergencia y notificadores de interfaz) demostradas en ejecuciones de prueba.

---

## 🏗️ Estructura del Proyecto

```text
actividad3-strategy-observer/
├── pom.xml
└── src/
    ├── main/
    │   └── java/
    │       └── edu/
    │           └── uees/
    │               └── disenosoftware/
    │                   ├── app/
    │                   │   └── Main.java
    │                   ├── domain/
    │                   │   ├── EstadoReserva.java
    │                   │   └── Reserva.java
    │                   ├── observer/
    │                   │   ├── CalendarioObserver.java
    │                   │   ├── EmailObserver.java
    │                   │   ├── PanelDocenteObserver.java
    │                   │   ├── PanelEstudianteObserver.java
    │                   │   └── ReservaObserver.java
    │                   └── strategy/
    │                       ├── CancelacionEmergencia.java
    │                       ├── CancelacionGrupal.java
    │                       ├── CancelacionNormal.java
    │                       ├── CancelacionPrioritaria.java
    │                       ├── PoliticaCancelacion.java
    │                       └── ServicioCancelacion.java
    └── test/
        └── java/
            └── edu/
                └── uees/
                    └── disenosoftware/
                        └── AppTest.java
```

---

## 🛠️ Tecnologías Utilizadas

- **Lenguaje:** Java 21 (LTS)
- **Gestor de Dependencias y Construcción:** Apache Maven 3.x
- **Control de Versiones:** Git & GitHub

---

## 🚀 Compilación y Ejecución

### Prerrequisitos
- JDK 21 instalado y configurado en el `PATH`.
- Apache Maven instalado.

### Comandos de Construcción y Ejecución

1. **Limpiar y compilar el proyecto:**
   ```bash
   mvn clean compile
   ```

2. **Ejecutar las pruebas unitarias:**
   ```bash
   mvn test
   ```

3. **Ejecutar la aplicación principal (`Main`):**
   ```bash
   mvn exec:java -Dexec.mainClass="edu.uees.disenosoftware.app.Main"
   ```

---

## 📋 Commits del Repositorio

El proyecto mantiene un historial de commits claro y estructurado según los requerimientos académicos:

1. `feat: implementar estrategias de cancelacion`
2. `feat: notificar cambios de reserva con observer`
3. `feat: agregar estrategias y observadores de reto`
4. `docs: agregar UML de patrones de comportamiento`

---

## 👤 Autor

- **Nombre:** Joffre Barre Veliz
- **Email Institucional:** joffre.barre@uees.edu.ec
- **Institución:** Universidad de Especialidades Espíritu Santo (UEES)
- **Materia:** Diseño de Software
