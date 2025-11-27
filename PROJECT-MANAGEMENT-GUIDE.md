# Guía de Implementación en Herramientas de Gestión

## Propósito
Este documento proporciona instrucciones para trasladar las épicas y historias de usuario a herramientas de gestión de proyectos como Jira, Azure DevOps, Trello, o GitHub Projects.

---

## Estructura Recomendada

### Jerarquía
```
Proyecto: Página de Login Moderna
├── Epic 1: UI/UX Design and Layout
│   ├── Historia de Usuario 1.1
│   ├── Historia de Usuario 1.2
│   ├── Historia de Usuario 1.3
│   └── Historia de Usuario 1.4
├── Epic 2: Form Validation and User Feedback
│   ├── Historia de Usuario 2.1
│   ├── Historia de Usuario 2.2
│   └── ...
└── ...
```

---

## Jira / Jira Software

### Configuración Inicial

1. **Crear un Proyecto**
   - Tipo: Scrum o Kanban
   - Nombre: "Página de Login Moderna"

2. **Configurar Issue Types**
   - Epic
   - Story
   - Task
   - Bug
   - Subtask

3. **Crear Custom Fields (opcional)**
   - Criterios de Aceptación (Textarea)
   - Dependencias (Epic Link)
   - Actividades Técnicas (Checklist)

### Creación de Épicas

**Epic 1: UI/UX Design and Layout**

```
Summary: UI/UX Design and Layout
Issue Type: Epic
Epic Name: UI/UX Design and Layout
Description:
Diseñar e implementar una interfaz de usuario moderna, limpia y responsiva 
para la página de inicio de sesión.

Story Points: 13
Sprint: Sprints 1-2
Labels: frontend, ui, ux, design
Priority: High
```

### Creación de Historias de Usuario

**Historia HU-1.1: Diseño Visual Moderno**

```
Summary: Diseño Visual Moderno
Issue Type: Story
Epic Link: UI/UX Design and Layout
Description:
Como usuario final
Quiero una página de inicio de sesión con un diseño moderno y atractivo
Para que tenga una primera impresión positiva de la aplicación

Criterios de Aceptación:
- El diseño utiliza una paleta de colores moderna y coherente
- Los elementos visuales siguen principios de diseño limpio
- La tipografía es legible y profesional
- Se incluyen elementos visuales como iconos o ilustraciones apropiadas
- El diseño es consistente con guías de diseño modernas

Story Points: 3
Sprint: Sprint 1
Labels: frontend, ui, design
Assignee: [Developer Name]
```

### Creación de Tareas Técnicas

```
Summary: AT-1.1 - Configuración del Proyecto Frontend
Issue Type: Task
Parent: HU-1.1 Diseño Visual Moderno
Description:
- Seleccionar e instalar framework frontend
- Configurar sistema de build
- Establecer estructura de carpetas
- Configurar pre-procesador CSS

Time Estimate: 4h
Labels: frontend, setup
```

---

## Azure DevOps

### Configuración Inicial

1. **Crear un Proyecto**
   - Nombre: "Página de Login Moderna"
   - Proceso: Scrum o Agile

2. **Configurar Work Item Types**
   - Epic
   - Feature (opcional)
   - User Story
   - Task

### Estructura en Azure Boards

```
Epic: UI/UX Design and Layout
├── Feature: Diseño Visual (opcional)
│   ├── User Story: HU-1.1 Diseño Visual Moderno
│   │   ├── Task: AT-1.1 Configuración del Proyecto
│   │   └── Task: AT-1.3 Implementar Estilos
│   └── User Story: HU-1.2 Formulario Intuitivo
└── Feature: Responsive Design
    └── User Story: HU-1.3 Diseño Responsivo
```

### Template de Epic

```
Title: Epic 1: UI/UX Design and Layout
Work Item Type: Epic
State: New
Area Path: Login-Moderna
Iteration Path: Release 1
Priority: 1
Value Area: Business

Description:
Diseñar e implementar una interfaz de usuario moderna, limpia y responsiva 
para la página de inicio de sesión.

Acceptance Criteria:
- Página de login con diseño moderno completada
- Formulario responsivo para todos los dispositivos
- Accesibilidad básica implementada (WCAG 2.1 AA)

Effort: 13
Tags: frontend; ui; design
```

---

## GitHub Projects

### Configuración Inicial

1. **Crear un Project (Beta)**
   - Template: Team backlog
   - Nombre: "Login Page - Epic Tracking"

2. **Configurar Views**
   - Board por Epic
   - Table por Sprint
   - Roadmap por Timeline

### Estructura de Issues

**Epic como Issue con Label**

```markdown
# Epic 1: UI/UX Design and Layout

## Descripción
Diseñar e implementar una interfaz de usuario moderna, limpia y responsiva.

## Historias de Usuario
- [ ] #101 HU-1.1: Diseño Visual Moderno
- [ ] #102 HU-1.2: Formulario de Login Intuitivo
- [ ] #103 HU-1.3: Diseño Responsivo
- [ ] #104 HU-1.4: Accesibilidad Básica

## Estimación
- Story Points: 13
- Duración: 1-2 sprints

## Labels
`epic` `frontend` `ui-ux` `sprint-1` `sprint-2`
```

**Historia de Usuario como Issue**

```markdown
# HU-1.1: Diseño Visual Moderno

## Historia
**Como** usuario final
**Quiero** una página de inicio de sesión con un diseño moderno
**Para que** tenga una primera impresión positiva

## Criterios de Aceptación
- [ ] Paleta de colores moderna y coherente
- [ ] Elementos visuales con diseño limpio
- [ ] Tipografía legible y profesional
- [ ] Iconos o ilustraciones apropiadas
- [ ] Consistencia con guías de diseño modernas

## Actividades Técnicas
- [ ] AT-1.1: Configuración del Proyecto Frontend
- [ ] AT-1.3: Implementar Estilos y Diseño Visual

## Labels
`user-story` `epic-1` `frontend` `ui` `sprint-1`

## Linked to Epic
#100
```

---

## Trello

### Configuración de Tablero

**Listas:**
- Backlog
- Sprint 1
- Sprint 2
- En Progreso
- En Revisión
- Listo

**Power-Ups Recomendados:**
- Card Repeater
- Custom Fields
- Card Dependencies

### Estructura de Tarjetas

**Tarjeta de Epic**

```
Título: 🎯 Epic 1: UI/UX Design and Layout

Descripción:
Diseñar e implementar una interfaz de usuario moderna, limpia y responsiva.

Story Points: 13
Sprint: 1-2

Checklist - Historias de Usuario:
□ HU-1.1: Diseño Visual Moderno
□ HU-1.2: Formulario de Login Intuitivo
□ HU-1.3: Diseño Responsivo
□ HU-1.4: Accesibilidad Básica

Labels: Epic, Frontend, UI/UX
```

**Tarjeta de Historia de Usuario**

```
Título: HU-1.1: Diseño Visual Moderno

Descripción:
Como usuario final
Quiero una página de inicio de sesión con un diseño moderno
Para que tenga una primera impresión positiva

Criterios de Aceptación:
□ Paleta de colores moderna
□ Diseño limpio
□ Tipografía legible
□ Iconos apropiados
□ Consistencia con guías modernas

Actividades:
□ AT-1.1: Config Proyecto Frontend
□ AT-1.3: Implementar Estilos

Story Points: 3
Epic: Epic 1

Labels: User Story, Epic-1, Frontend, Sprint-1
```

---

## Monday.com

### Configuración de Board

**Grupos (Groups):**
- Epic 1: UI/UX Design
- Epic 2: Validation
- Epic 3: Security
- Epic 4: Integration

**Columnas Recomendadas:**
- Item (Historia/Tarea)
- Owner (Asignado a)
- Status (Estado)
- Sprint (Número)
- Story Points
- Priority (Prioridad)
- Timeline (Fechas)

### Estructura de Items

```
Item: HU-1.1 - Diseño Visual Moderno
Group: Epic 1: UI/UX Design
Owner: [Developer]
Status: To Do
Sprint: Sprint 1
Story Points: 3
Priority: High
Timeline: Week 1-2
```

---

## Linear

### Configuración

1. **Crear un Proyecto**
   - Nombre: "Login Page Modernization"

2. **Configurar Labels**
   - epic-1, epic-2, epic-3, epic-4
   - frontend, backend, testing
   - priority-high, priority-medium

### Template de Issue

```
Title: UI/UX Design and Layout

Type: Epic
Project: Login Page Modernization
Labels: epic, frontend, ui-ux
Priority: High
Estimate: 13

Description:
Diseñar e implementar una interfaz de usuario moderna, limpia y responsiva.

Child Issues:
- HU-1.1: Diseño Visual Moderno
- HU-1.2: Formulario de Login Intuitivo
- HU-1.3: Diseño Responsivo
- HU-1.4: Accesibilidad Básica
```

---

## ClickUp

### Jerarquía en ClickUp

```
Space: Desarrollo
├── Folder: Login Page Project
    ├── List: Epic 1 - UI/UX
    │   ├── Task: HU-1.1 Diseño Visual
    │   │   └── Subtask: AT-1.1 Config Proyecto
    │   └── Task: HU-1.2 Formulario
    ├── List: Epic 2 - Validation
    └── List: Epic 3 - Security
```

### Custom Fields

- Epic Number (Dropdown: 1, 2, 3, 4)
- Story Points (Number)
- Sprint (Dropdown: Sprint 1-10)
- Epic Status (Progress Bar)

---

## Mejores Prácticas Generales

### 1. Naming Conventions

```
Epic:    Epic N: [Nombre Descriptivo]
Story:   HU-N.M: [Título de Historia]
Task:    AT-N.M: [Título de Actividad]
Bug:     BUG-[ID]: [Descripción]
```

### 2. Labels / Tags Recomendados

- **Por Tipo:** `epic`, `user-story`, `task`, `bug`
- **Por Área:** `frontend`, `backend`, `devops`, `testing`
- **Por Sprint:** `sprint-1`, `sprint-2`, etc.
- **Por Prioridad:** `priority-high`, `priority-medium`, `priority-low`
- **Por Estado:** `blocked`, `in-progress`, `in-review`, `done`

### 3. Estimación

- **Planning Poker:** Usar para estimar en equipo
- **T-Shirt Sizing:** S, M, L, XL (alternativa a story points)
- **Fibonacci:** 1, 2, 3, 5, 8, 13, 21 (para story points)

### 4. Workflow States

```
To Do → In Progress → In Review → Testing → Done
```

### 5. Definition of Done (DoD)

Añadir checklist estándar en cada historia:

```
□ Código implementado y funcional
□ Unit tests escritos y pasando
□ Code review completado
□ Documentación actualizada
□ Testing manual realizado
□ Criterios de aceptación cumplidos
□ Merged a develop/main
```

---

## Scripts de Importación

### CSV para Jira

```csv
Summary,Issue Type,Epic Link,Description,Story Points,Sprint,Labels
"UI/UX Design and Layout","Epic","","Diseñar interfaz moderna",13,"Sprint 1-2","frontend,ui"
"HU-1.1: Diseño Visual Moderno","Story","UI/UX Design and Layout","Como usuario...",3,"Sprint 1","frontend,ui"
```

### JSON para GitHub

```json
{
  "title": "Epic 1: UI/UX Design and Layout",
  "body": "Diseñar e implementar interfaz moderna",
  "labels": ["epic", "frontend", "ui-ux"],
  "milestone": "Sprint 1",
  "assignees": []
}
```

---

## Recursos Adicionales

- [Jira Documentation](https://www.atlassian.com/software/jira/guides)
- [Azure DevOps Best Practices](https://docs.microsoft.com/en-us/azure/devops/)
- [GitHub Projects Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
- [Agile Alliance Resources](https://www.agilealliance.org/agile101/)

---

**Última Actualización:** 2025-11-27
**Versión:** 1.0
