# HydroSeat — Roadmap Maestro del Proyecto

**Organización:** Crohnoz Labs  
**Código interno del proyecto:** `CL-MED-001`  
**Nombre de trabajo:** `HydroSeat`  
**Estado actual:** Gate G1 — dispositivo médico confirmado; estrategia regulatoria y clasificación en desarrollo  
**Versión del documento:** `0.3.0-medical-device-baseline`  
**Fecha de creación:** 2026-07-21  
**Propietario del proyecto:** Enrique Flores / Crohnoz Labs  
**Herramientas principales:** Autodesk Fusion, Figma, GitHub, impresión 3D, prototipado físico  
**Documento maestro:** Este archivo debe ser usado como punto de entrada para retomar el proyecto en cualquier conversación o sesión futura.

---

## 1. Propósito de este documento

Este archivo define la visión, el alcance, la arquitectura, la metodología, el roadmap, los criterios de avance y el sistema de continuidad del proyecto HydroSeat.

Su objetivo principal es evitar que el proyecto pierda contexto entre sesiones y permitir que cualquier trabajo futuro continúe exactamente desde el último punto validado.

Toda modificación importante del proyecto debe reflejarse aquí o en los documentos vinculados desde aquí.

---

## 2. Resumen ejecutivo

HydroSeat es un asiento terapéutico modular desarrollado por Crohnoz Labs. Su propósito es combinar en un mismo dispositivo:

- ergonomía para trabajo prolongado;
- descarga de presión en la zona perianal;
- baño de asiento con agua tibia;
- hidroterapia localizada de baja presión;
- limpieza y desmontaje rápido;
- compatibilidad con una silla de oficina o silla gamer existente;
- adaptación a usuarios de distintas contexturas, priorizando una geometría apta para usuarios de cadera y glúteos grandes.

El concepto debe evolucionar desde una modificación de bajo presupuesto sobre una silla gamer existente hasta un prototipo funcional, seguro, lavable, modular y técnicamente documentado.

El primer objetivo no es crear un producto comercial. El primer objetivo es demostrar que la geometría, la ergonomía, el sistema de cubeta y la integración con agua pueden funcionar de forma segura y práctica.

---

## 3. Problema que busca resolver

Usuarios con hemorroides, fisuras, dolor perianal, enfermedad inflamatoria intestinal, recuperación posoperatoria u otras molestias pueden necesitar:

- permanecer sentados durante varias horas;
- reducir presión directa en la zona perianal;
- aplicar calor local;
- realizar baños de asiento;
- evitar levantarse constantemente para aplicar terapias separadas;
- mantener comodidad, higiene y privacidad.

Las soluciones actuales suelen estar separadas:

- cojín para hemorroides;
- baño de asiento;
- bidet;
- silla ergonómica;
- sistema de agua caliente;
- hidroterapia.

HydroSeat busca integrar estas funciones en un único módulo terapéutico.

---

## 4. Visión del producto

Crear un asiento terapéutico modular que permita al usuario sentarse cómodamente mientras la zona perianal queda parcialmente sumergida en agua tibia, con apoyo estructural distribuido sobre glúteos e isquiones y sin que el peso corporal recaiga sobre la cubeta de agua.

La visión futura considera:

- un módulo compatible con distintas sillas;
- control de temperatura;
- recirculación;
- hidrojet regulable;
- drenaje;
- secado con aire tibio;
- limpieza simplificada;
- sensores;
- perfiles de usuario;
- versiones domésticas y clínicas.

---

## 5. Principios de diseño

### 5.1 Modularidad

Cada subsistema debe poder diseñarse, probarse, reemplazarse y mejorarse por separado.

### 5.2 Seguridad antes que automatización

El prototipo inicial debe minimizar riesgos eléctricos, térmicos, mecánicos e higiénicos.

### 5.3 El peso no debe descansar sobre el agua

La cubeta no debe actuar como elemento estructural principal. El peso del usuario debe transmitirse hacia un aro o bastidor resistente.

### 5.4 Diseño para usuario grande

La geometría base debe priorizar usuarios de cadera y glúteos grandes. Los usuarios más pequeños podrán adaptarse mediante insertos o cojines intercambiables.

### 5.5 Limpieza como requisito central

Toda pieza en contacto con agua o cuerpo debe poder retirarse, lavarse, secarse y revisarse.

### 5.6 Iteración paramétrica

Las dimensiones críticas deben modelarse como parámetros editables en Autodesk Fusion.

### 5.7 Bajo presupuesto, pero sin improvisaciones peligrosas

Se privilegiarán materiales reutilizados y componentes económicos, pero no se usarán soluciones inseguras cerca de agua, calor o alimentación eléctrica.

### 5.8 Documentación continua

Cada decisión, prueba, error y cambio debe quedar registrado.

---

## 6. Alcance del MVP

El MVP funcional debe demostrar:

1. Que una persona de contextura grande puede sentarse cómodamente.
2. Que el peso queda soportado por una estructura rígida.
3. Que la zona perianal puede quedar parcialmente sumergida.
4. Que la cubeta puede retirarse sin desmontar la silla completa.
5. Que el agua puede mantenerse tibia dentro de un rango seguro.
6. Que el sistema puede drenar y limpiarse.
7. Que no existen fugas en una sesión de prueba.
8. Que el usuario puede levantarse, secarse y vestirse sin una operación compleja.
9. Que el módulo puede montarse sobre una silla gamer sacrificable.
10. Que el sistema puede evolucionar después hacia hydrojet y control electrónico.

---

## 7. Fuera de alcance inicial

Durante las primeras fases no se considera obligatorio:

- certificación médica;
- venta comercial;
- fabricación en serie;
- moldeo por inyección;
- aplicación móvil;
- conectividad Bluetooth;
- perfiles automáticos;
- secado con aire;
- hidrojet de alta complejidad;
- filtración permanente;
- esterilización automática;
- uso clínico profesional;
- validación con terceros.

Estas funciones podrán incorporarse en fases posteriores.

---

## 8. Arquitectura general

```text
HydroSeat
├── HS-001 Seat Module
│   ├── bastidor estructural
│   ├── aro de apoyo
│   ├── acolchado
│   ├── apertura central
│   └── interfaz con silla
├── HS-002 Water Basin Module
│   ├── cubeta extraíble
│   ├── borde de contención
│   ├── drenaje
│   ├── manillas
│   └── sello
├── HS-003 Adaptive Interface
│   ├── membrana flexible
│   ├── pétalos
│   ├── inserto anatómico
│   └── control de salpicaduras
├── HS-004 Thermal Module
│   ├── calentamiento
│   ├── sensor de temperatura
│   ├── corte térmico
│   └── aislación
├── HS-005 Hydrojet Module
│   ├── bomba
│   ├── boquillas
│   ├── regulación
│   └── recirculación
├── HS-006 Drain and Cleaning Module
│   ├── desagüe
│   ├── bandeja
│   ├── mangueras
│   └── desmontaje
├── HS-007 Control Module
│   ├── interfaz
│   ├── temporizador
│   ├── alimentación
│   ├── protección
│   └── sensores
└── HS-008 Accessory Module
    ├── soporte para toalla
    ├── almacenamiento
    ├── protector de piso
    └── elementos consumibles
```

---

## 9. Herramientas del proyecto

### 9.1 Autodesk Fusion

Uso principal:

- CAD paramétrico;
- ensamblajes;
- piezas;
- simulaciones estructurales;
- renders;
- planos;
- exportación STEP, STL y DXF.

### 9.2 Figma

Uso principal:

- conceptos visuales;
- diagramas;
- versiones de diseño;
- documentación gráfica;
- comparaciones;
- moodboard;
- paneles de presentación.

### 9.3 GitHub

Uso principal:

- repositorio maestro;
- issues;
- milestones;
- changelog;
- documentación;
- archivos exportados;
- control de versiones de documentos y firmware.

### 9.4 Impresión 3D

Uso previsto:

- soportes;
- adaptadores;
- boquillas;
- uniones;
- plantillas;
- mecanismos;
- piezas pequeñas;
- prototipos de geometría.

### 9.5 Taller físico

Herramientas previstas:

- silla gamer sacrificable;
- madera o terciado;
- espuma;
- goma EVA;
- tela o cubierta impermeable;
- tornillería;
- herramientas de corte;
- taladro;
- elementos de medición;
- adhesivos apropiados;
- sellos;
- componentes hidráulicos.

---

## 10. Repositorio recomendado

```text
hydroseat/
├── README.md
├── ROADMAP.md
├── CHANGELOG.md
├── STATUS.md
├── LICENSE
├── .gitignore
├── docs/
│   ├── 00_project_overview.md
│   ├── 01_prd.md
│   ├── 02_user_needs.md
│   ├── 03_design_requirements.md
│   ├── 04_risk_register.md
│   ├── 05_test_plan.md
│   ├── 06_materials.md
│   ├── 07_decisions.md
│   ├── 08_measurements.md
│   ├── 09_safety.md
│   └── 10_resume_protocol.md
├── cad/
│   ├── fusion/
│   ├── step/
│   ├── stl/
│   ├── dxf/
│   └── drawings/
├── figma/
│   ├── links.md
│   └── exports/
├── electronics/
│   ├── schematics/
│   ├── bom/
│   ├── wiring/
│   └── firmware/
├── prototypes/
│   ├── v0/
│   ├── v1/
│   ├── v2/
│   └── photos/
├── tests/
│   ├── ergonomic/
│   ├── leak/
│   ├── thermal/
│   ├── load/
│   └── cleaning/
├── purchasing/
│   ├── bom_master.csv
│   ├── suppliers.md
│   └── receipts/
└── references/
    ├── research/
    ├── patents/
    └── images/
```

---

## 11. Parámetros iniciales del CAD

Todos estos valores son preliminares y deben ser medidos o validados.

```text
seat_width = 560 mm
seat_depth = 500 mm
seat_frame_thickness = 18 mm
seat_cushion_height = 70 mm
central_opening_width = 260 mm
central_opening_length = 320 mm
basin_depth = 80 mm
basin_nominal_water_depth = 45 mm
basin_capacity_target = 3.0 L
max_user_mass_target = 150 kg
design_safety_factor = 2.0
water_temperature_nominal = 38 °C
water_temperature_maximum = 40 °C
module_removal_clearance = 5 mm
```

### Notas

- El ancho debe priorizar una pelvis grande.
- La apertura no debe descargar el peso sobre tejido blando.
- La profundidad de agua deberá probarse físicamente.
- La cubeta debe poder retirarse sin inclinarla excesivamente.
- La estructura debe diseñarse para una carga superior a la masa objetivo.

---

## 12. Requisitos ergonómicos iniciales

- El usuario debe poder sentarse al menos 30 minutos en la primera validación.
- La zona anal no debe recibir presión directa.
- Los muslos no deben quedar comprimidos en el borde frontal.
- La pelvis no debe hundirse de manera inestable.
- La espalda debe conservar el soporte original de la silla.
- La altura final del asiento no debe aumentar excesivamente.
- El centro de gravedad debe mantenerse dentro de la base de ruedas.
- La abertura debe tolerar variación anatómica.
- El sistema debe priorizar usuarios grandes sin excluir usuarios pequeños.
- Debe existir una forma de ajustar el área útil mediante insertos.

---

## 13. Requisitos mecánicos

- La silla no debe volcar durante uso normal.
- El módulo debe anclarse al bastidor existente.
- La cubeta no debe soportar carga estructural principal.
- El bastidor debe resistir carga estática y movimientos al sentarse.
- Debe evitarse concentración de esfuerzo en tornillos individuales.
- Las piezas impresas no deben actuar como único soporte de carga.
- Las uniones deben ser inspeccionables.
- Debe existir acceso para mantenimiento.
- El módulo debe ser desmontable.

---

## 14. Requisitos hidráulicos

- La cubeta debe ser extraíble.
- No debe presentar esquinas difíciles de limpiar.
- Debe soportar agua tibia repetidamente.
- Debe tener rebalse o margen de seguridad.
- El drenaje debe ser controlable.
- Las mangueras deben ser reemplazables.
- La bomba debe ubicarse separada del área estructural.
- La recirculación debe evitar chorros de presión excesiva.
- La boquilla debe ser regulable o intercambiable.
- El sistema debe poder operar inicialmente sin bomba.

---

## 15. Requisitos térmicos

- Temperatura nominal: 37–38 °C.
- Límite de operación inicial: 40 °C.
- Debe existir medición independiente.
- Debe existir corte de seguridad.
- El calentador no debe quedar accesible al cuerpo.
- El sistema debe evitar puntos calientes.
- La calefacción debe poder desconectarse físicamente.
- El primer prototipo con agua deberá usar el método más simple y seguro posible.

---

## 16. Requisitos eléctricos

- Preferir alimentación de baja tensión.
- Evitar 220 V cerca de agua.
- Separar zona húmeda y zona eléctrica.
- Usar conectores protegidos.
- Incorporar fusible.
- Incorporar interruptor general.
- Diseñar desconexión rápida.
- Mantener componentes electrónicos fuera de la cubeta.
- No energizar ningún módulo hasta superar pruebas de estanqueidad.

---

## 17. Requisitos de higiene

- Cubeta lavable y removible.
- Superficies lisas.
- Sin cavidades ocultas.
- Sin materiales porosos en contacto directo con agua.
- Mangueras accesibles.
- Posibilidad de secado completo.
- Evitar recirculación indefinida.
- Definir protocolo de limpieza.
- Definir piezas consumibles.
- Diseñar un soporte lateral para toalla personal.

---

## 18. Riesgos principales

| ID | Riesgo | Impacto | Mitigación inicial |
|---|---|---:|---|
| R-001 | Fuga de agua | Alto | Cubeta independiente y pruebas previas |
| R-002 | Vuelco de silla | Alto | Verificar centro de gravedad y base |
| R-003 | Quemadura | Alto | Límite térmico y sensor independiente |
| R-004 | Riesgo eléctrico | Crítico | Baja tensión y separación física |
| R-005 | Rotura estructural | Alto | Bastidor rígido y factor de seguridad |
| R-006 | Mala distribución de presión | Alto | Pruebas ergonómicas progresivas |
| R-007 | Contaminación | Alto | Diseño desmontable y protocolo de limpieza |
| R-008 | Hydrojet excesivo | Medio/Alto | Baja presión y regulación |
| R-009 | Salpicaduras | Medio | Borde, membrana y pruebas |
| R-010 | Cubeta difícil de retirar | Medio | Guías, manillas y prueba con agua |
| R-011 | Altura de asiento excesiva | Medio | Integración dentro del asiento |
| R-012 | Dependencia de piezas impresas | Alto | Piezas impresas solo como auxiliares |

---

## 19. Roadmap maestro

# Fase 0 — Inicio y continuidad

### Objetivo

Crear la infraestructura del proyecto.

### Entregables

- repositorio GitHub;
- README;
- ROADMAP;
- STATUS;
- CHANGELOG;
- estructura de carpetas;
- archivo de decisiones;
- archivo de riesgos;
- archivo de medidas.

### Criterio de salida

El proyecto puede ser retomado por una nueva sesión sin perder contexto.

---

# Fase 1 — Levantamiento de la silla donante

### Objetivo

Documentar completamente la silla gamer que será modificada.

### Actividades

- fotografiar la silla;
- identificar marca y modelo si es posible;
- desmontar asiento;
- medir ancho;
- medir profundidad;
- medir separación de pernos;
- medir bastidor;
- medir mecanismo de inclinación;
- medir altura;
- medir base;
- medir apoyabrazos;
- medir espuma existente;
- registrar daños;
- registrar capacidad estimada.

### Entregables

- hoja de medidas;
- fotografías;
- bosquejo 2D;
- modelo simplificado de la silla;
- mapa de puntos de anclaje.

### Criterio de salida

Existe información suficiente para diseñar un módulo compatible.

---

# Fase 2 — Requisitos antropométricos y ergonomía

### Objetivo

Definir el rango corporal objetivo.

### Actividades

- medir ancho de cadera sentado;
- medir profundidad glúteo-poplítea;
- estimar posición de isquiones;
- medir posición cómoda;
- definir abertura inicial;
- evaluar usuarios pequeños y grandes;
- definir insertos ajustables;
- documentar postura.

### Entregables

- parámetros antropométricos;
- zonas de apoyo;
- zonas sin presión;
- geometría preliminar.

### Criterio de salida

La forma del asiento tiene una justificación ergonómica.

---

# Fase 3 — Concepto visual y arquitectura

### Objetivo

Traducir requisitos en un concepto claro.

### Actividades

- desarrollar vistas superior, frontal, lateral y corte;
- definir cubeta extraíble;
- definir soporte de toalla;
- definir módulo adaptable;
- definir mecanismo central;
- comparar alternativas.

### Entregables

- tablero Figma;
- arquitectura final del MVP;
- vistas conceptuales;
- selección de concepto.

### Criterio de salida

Existe un concepto único aprobado para pasar a CAD.

---

# Fase 4 — CAD paramétrico del asiento

### Objetivo

Diseñar HS-001 Seat Module.

### Actividades

- crear parámetros;
- modelar bastidor;
- modelar aro;
- modelar apertura;
- modelar soportes;
- modelar anclajes;
- verificar interferencias;
- preparar planos.

### Entregables

- archivo Fusion;
- STEP;
- STL auxiliares;
- planos;
- lista de materiales.

### Criterio de salida

El asiento puede fabricarse sin la cubeta.

---

# Fase 5 — Mockup ergonómico seco

### Objetivo

Validar comodidad sin agua.

### Actividades

- fabricar bastidor;
- montar espuma;
- probar apertura;
- probar altura;
- probar estabilidad;
- registrar presión;
- modificar geometría.

### Entregables

- prototipo seco V0;
- fotos;
- reporte de pruebas;
- cambios requeridos.

### Criterio de salida

El usuario puede sentarse cómodamente durante el periodo definido.

---

# Fase 6 — Cubeta extraíble

### Objetivo

Diseñar HS-002 Water Basin Module.

### Actividades

- definir volumen;
- definir profundidad;
- definir guías;
- definir manillas;
- definir drenaje;
- validar extracción;
- validar limpieza.

### Entregables

- CAD de cubeta;
- prototipo;
- prueba de estanqueidad;
- protocolo de extracción.

### Criterio de salida

La cubeta puede llenarse, instalarse, retirarse y vaciarse sin fuga.

---

# Fase 7 — Prueba húmeda pasiva

### Objetivo

Probar inmersión parcial sin bomba ni calentador integrado.

### Actividades

- usar agua previamente templada;
- medir profundidad real;
- validar contacto;
- observar salpicaduras;
- evaluar comodidad;
- evaluar levantarse y secarse;
- ajustar bordes.

### Entregables

- reporte de inmersión;
- video o fotos técnicas;
- lista de modificaciones;
- aprobación de geometría húmeda.

### Criterio de salida

La inmersión parcial funciona de forma práctica y controlada.

---

# Fase 8 — Interfaz anatómica adaptable

### Objetivo

Desarrollar HS-003 Adaptive Interface.

### Alternativas

- pétalos flexibles;
- membrana;
- insertos intercambiables;
- borde de silicona;
- aro segmentado;
- diafragma mecánico.

### Actividades

- prototipos pequeños;
- pruebas con materiales;
- pruebas de sellado;
- pruebas de comodidad;
- pruebas de limpieza.

### Entregables

- concepto seleccionado;
- prototipo funcional;
- materiales candidatos.

### Criterio de salida

La interfaz acompaña el cuerpo sin apretar ni generar presión dañina.

---

# Fase 9 — Módulo térmico

### Objetivo

Mantener agua en rango seguro.

### Actividades

- seleccionar método de calentamiento;
- seleccionar sensor;
- seleccionar corte térmico;
- medir velocidad de calentamiento;
- medir estabilidad;
- aislar cubeta;
- diseñar desconexión.

### Entregables

- esquema;
- prueba térmica;
- curva de temperatura;
- límites operativos.

### Criterio de salida

La temperatura se mantiene estable y dentro del rango establecido.

---

# Fase 10 — Hydrojet

### Objetivo

Agregar hidroterapia localizada suave.

### Actividades

- seleccionar bomba;
- diseñar boquillas;
- limitar presión;
- probar flujo;
- probar modos;
- evaluar ruido;
- evaluar limpieza.

### Entregables

- módulo de bomba;
- boquillas;
- pruebas de caudal;
- configuración segura.

### Criterio de salida

El flujo es suave, controlable y no genera molestias ni riesgo.

---

# Fase 11 — Drenaje, limpieza y mantenimiento

### Objetivo

Convertir el sistema en una solución práctica.

### Actividades

- definir drenaje;
- definir ruta de agua;
- definir desmontaje;
- definir limpieza;
- definir secado;
- definir inspección;
- definir consumibles.

### Entregables

- manual de limpieza;
- diagrama de mantenimiento;
- protocolo postuso.

### Criterio de salida

El sistema puede dejarse limpio y seco en un tiempo razonable.

---

# Fase 12 — Control electrónico

### Objetivo

Integrar control básico.

### Funciones posibles

- encendido;
- temperatura;
- temporizador;
- bomba;
- intensidad;
- alarmas;
- apagado;
- sensor de nivel.

### Entregables

- esquema eléctrico;
- firmware;
- panel;
- carcasa;
- pruebas.

### Criterio de salida

El sistema opera con controles simples y seguros.

---

# Fase 13 — Prototipo integrado V1

### Objetivo

Unir todos los módulos validados.

### Entregables

- silla funcional;
- manual de uso;
- lista completa de materiales;
- registro de montaje;
- reporte de pruebas;
- lista de fallas.

### Criterio de salida

El prototipo ejecuta una sesión completa de uso.

---

# Fase 14 — Iteración V2

### Objetivo

Corregir problemas detectados.

### Áreas de mejora

- ergonomía;
- fugas;
- limpieza;
- temperatura;
- presión;
- ruido;
- estabilidad;
- estética;
- desmontaje.

### Criterio de salida

El prototipo V2 es estable y repetible.

---

# Fase 15 — Evaluación de producto

### Objetivo

Determinar si HydroSeat puede evolucionar a producto.

### Actividades

- estimar costo;
- revisar mercado;
- analizar propiedad intelectual;
- evaluar regulación;
- estudiar fabricación;
- evaluar concursos;
- definir público objetivo.

### Entregables

- dossier técnico;
- evaluación comercial;
- mapa regulatorio;
- pitch interno.

---

## 20. Hitos principales

| Hito | Descripción | Estado |
|---|---|---|
| M0 | Proyecto documentado | En curso |
| M1 | Silla medida y modelada | Pendiente |
| M2 | Asiento seco aprobado | Pendiente |
| M3 | Cubeta aprobada | Pendiente |
| M4 | Prueba húmeda pasiva aprobada | Pendiente |
| M5 | Interfaz adaptable aprobada | Pendiente |
| M6 | Temperatura controlada | Pendiente |
| M7 | Hydrojet seguro | Pendiente |
| M8 | Prototipo integrado V1 | Pendiente |
| M9 | Prototipo V2 | Pendiente |
| M10 | Evaluación comercial | Pendiente |

---

## 21. Sistema de estados

Cada tarea debe usar uno de estos estados:

- `BACKLOG`
- `READY`
- `IN PROGRESS`
- `BLOCKED`
- `REVIEW`
- `VALIDATED`
- `REJECTED`
- `DEFERRED`
- `DONE`

---

## 22. Criterios de decisión

Una decisión se considera aprobada cuando:

1. está documentada;
2. tiene una razón técnica;
3. identifica alternativas;
4. registra riesgos;
5. define impacto;
6. queda vinculada a una versión.

Formato:

```md
## DEC-0001 — Título

**Fecha:**  
**Estado:** Propuesta / Aprobada / Rechazada  
**Contexto:**  
**Alternativas:**  
**Decisión:**  
**Motivo:**  
**Impacto:**  
**Revisión futura:**  
```

---

## 23. Convención de versiones

### Documentación

`MAJOR.MINOR.PATCH`

Ejemplo:

- `0.1.0`: documento inicial;
- `0.2.0`: nuevas fases;
- `0.2.1`: correcciones;
- `1.0.0`: roadmap validado.

### Prototipos

- `P0`: concepto físico;
- `P1`: asiento seco;
- `P2`: cubeta;
- `P3`: prueba húmeda;
- `P4`: sistema térmico;
- `P5`: hydrojet;
- `V1`: integración completa;
- `V2`: iteración mejorada.

### CAD

```text
HS-001-seat-v0.1
HS-002-basin-v0.1
HS-003-interface-v0.1
```

---

## 24. Registro de pruebas

Cada prueba debe incluir:

```md
# TEST-XXXX

**Fecha:**  
**Prototipo:**  
**Objetivo:**  
**Configuración:**  
**Materiales:**  
**Procedimiento:**  
**Resultado esperado:**  
**Resultado real:**  
**Problemas:**  
**Fotos o videos:**  
**Conclusión:**  
**Acción siguiente:**  
```

---

## 25. Protocolo para retomar el proyecto

Cada vez que el proyecto se retome, la sesión debe comenzar leyendo:

1. `ROADMAP.md`
2. `STATUS.md`
3. `CHANGELOG.md`
4. última decisión en `docs/07_decisions.md`
5. último reporte de prueba
6. issues abiertos del milestone actual

Después se debe responder:

```text
Estado actual:
Último hito validado:
Trabajo en curso:
Bloqueos:
Decisiones pendientes:
Siguiente acción concreta:
Archivos que deben modificarse:
```

---

## 26. Archivo STATUS.md recomendado

```md
# HydroSeat — Estado actual

**Fecha de actualización:**  
**Versión del proyecto:**  
**Fase activa:**  
**Hito activo:**  
**Responsable:**  

## Último trabajo completado

## Trabajo en curso

## Próxima acción

## Bloqueos

## Decisiones pendientes

## Archivos modificados

## Pruebas realizadas

## Riesgos nuevos

## Notas para la próxima sesión
```

---

## 27. Prompt de reanudación para futuras sesiones

Copiar este bloque al retomar:

```text
Quiero retomar el proyecto HydroSeat de Crohnoz Labs.

Lee primero el archivo ROADMAP.md y cualquier archivo STATUS.md, CHANGELOG.md, decisión técnica o reporte de pruebas disponible.

No reinicies el diseño desde cero. Identifica:
1. última fase completada;
2. fase activa;
3. tareas pendientes;
4. bloqueos;
5. decisiones abiertas;
6. próxima acción técnica concreta.

Después propón el plan de trabajo de la sesión y actualiza los documentos correspondientes al finalizar.
Respeta el nombre Crohnoz Labs exactamente.
```

---

## 28. Estado inicial del proyecto

### Completado

- definición del concepto general;
- elección de Autodesk Fusion como CAD principal;
- elección de Figma para diseño conceptual;
- elección de GitHub para documentación;
- definición de silla gamer como plataforma donante;
- definición de cubeta extraíble;
- definición de prioridad para usuario grande;
- definición de soporte lateral para toalla;
- definición de arquitectura modular;
- creación del roadmap maestro.

### En curso

- preparación del repositorio;
- definición formal de requisitos;
- planificación del levantamiento de medidas.

### Próxima acción recomendada

Realizar el levantamiento completo de la silla donante.

---

## 29. Lista de medidas necesarias para la silla

### Asiento

- ancho total;
- ancho útil;
- profundidad total;
- profundidad útil;
- altura de espuma;
- espesor de base;
- forma del borde frontal;
- curvatura lateral;
- distancia al respaldo.

### Anclajes

- patrón de pernos;
- diámetro;
- separación longitudinal;
- separación transversal;
- espesor de placa;
- posición del mecanismo.

### Silla completa

- altura mínima y máxima;
- ancho de base;
- diámetro de ruedas;
- posición de apoyabrazos;
- inclinación;
- centro aproximado del pistón;
- distancia al borde delantero.

### Usuario

- peso aproximado;
- ancho de cadera sentado;
- profundidad glúteo-poplítea;
- altura cómoda;
- separación entre muslos;
- ubicación aproximada de apoyo principal.

---

## 30. Checklist de la próxima sesión física

- [ ] Fotografiar silla desde seis ángulos.
- [ ] Medir asiento.
- [ ] Medir pernos.
- [ ] Retirar cojín si es posible.
- [ ] Fotografiar estructura inferior.
- [ ] Identificar piezas reutilizables.
- [ ] Registrar materiales.
- [ ] Registrar daños.
- [ ] Definir qué partes pueden cortarse.
- [ ] Crear croquis inicial.
- [ ] Actualizar STATUS.md.
- [ ] Crear issue para HS-001.

---

## 31. Definición de éxito del proyecto

HydroSeat se considerará técnicamente exitoso cuando:

- soporte de forma estable al usuario objetivo;
- reduzca presión en la zona perianal;
- permita inmersión parcial controlada;
- no presente fugas;
- mantenga temperatura segura;
- pueda limpiarse;
- pueda desmontarse;
- pueda fabricarse nuevamente usando documentación;
- no dependa de una única pieza improvisada;
- tenga un proceso de uso claro;
- tenga riesgos documentados;
- tenga una versión de diseño reproducible.

---

## 32. Nota de seguridad

Este proyecto parte como prototipo experimental de uso personal.

No debe presentarse como dispositivo médico ni utilizarse clínicamente sin evaluación técnica, sanitaria y regulatoria adecuada.

Las primeras pruebas deberán realizarse en etapas:

1. estructura seca;
2. cubeta fuera de la silla;
3. estanqueidad;
4. agua sin electricidad;
5. agua tibia premezclada;
6. módulos eléctricos externos;
7. integración progresiva.

Nunca se debe combinar agua y alimentación eléctrica improvisada.

---

## 33. Regla de oro del proyecto

> Ningún avance se considera completo hasta que quede medido, documentado, fotografiado, versionado y validado.

---

## 34. Próximo paso oficial

**Fase activa:** Fase 1 — Levantamiento de la silla donante.

**Acción inmediata:**

Crear una ficha de medición y completar las dimensiones reales de la silla gamer que se sacrificará para el prototipo.



---

# 35. REVISIÓN COMERCIAL Y REGULATORIA — VERSIÓN 0.2.0

## 35.1 Cambio de objetivo del proyecto

A partir de esta versión, HydroSeat deja de planificarse únicamente como un prototipo experimental personal y pasa a gestionarse como un **producto potencialmente comercializable** diseñado por **Crohnoz Labs**.

Esto obliga a incorporar desde el inicio:

- estrategia regulatoria;
- control formal del diseño;
- trazabilidad de requisitos;
- gestión de riesgos durante todo el ciclo de vida;
- evidencia de verificación y validación;
- control de proveedores y materiales;
- trazabilidad de unidades y lotes;
- documentación de fabricación;
- instrucciones y etiquetado;
- vigilancia posventa;
- gestión de reclamos, incidentes, correcciones y retiros;
- protección de propiedad intelectual;
- evaluación clínica o de desempeño, cuando corresponda;
- cumplimiento eléctrico, mecánico, térmico, biológico e higiénico.

El producto no podrá considerarse listo para venta porque “el prototipo funciona”. La liberación comercial exigirá evidencia documentada de que el diseño cumple todos sus requisitos y que los riesgos residuales son aceptables.

---

# 36. DECISIÓN REGULATORIA FUNDAMENTAL

## 36.1 La finalidad prevista determina la categoría del producto

Antes de diseñar publicidad, envase, manual o funciones finales se deberá congelar una **declaración de finalidad prevista**.

Dos rutas preliminares:

### Ruta A — Producto de bienestar y confort

Ejemplo conceptual de finalidad prevista:

> Asiento de confort con baño tibio destinado al bienestar, relajación y apoyo ergonómico durante periodos breves de uso doméstico.

Esta ruta evita atribuir al producto diagnóstico, prevención, tratamiento o alivio de enfermedades. Sin embargo, no garantiza por sí sola que la autoridad lo considere fuera del ámbito sanitario. La clasificación debe analizar el diseño completo, el uso real, las instrucciones, la publicidad y las reivindicaciones.

### Ruta B — Dispositivo médico terapéutico

Ejemplo conceptual de finalidad prevista:

> Dispositivo destinado a aliviar temporalmente molestias perianales mediante descarga de presión, baño de asiento tibio e hidroterapia localizada.

Con una finalidad terapéutica explícita, HydroSeat probablemente deberá tratarse desde el comienzo como un dispositivo médico activo o un sistema con componentes activos. La clase exacta y las obligaciones aplicables deberán ser confirmadas mediante análisis regulatorio formal y, de ser posible, consulta escrita al Instituto de Salud Pública de Chile.

## 36.2 Regla de control de claims

Ninguna publicación, presentación, etiqueta o demostración podrá afirmar que HydroSeat:

- cura hemorroides;
- trata enfermedad de Crohn;
- previene complicaciones;
- acelera cicatrización;
- reemplaza una evaluación médica;
- sirve para recuperación posoperatoria;
- reduce inflamación;
- tiene eficacia clínica;

salvo que esa afirmación esté incluida en la finalidad prevista, respaldada por evidencia suficiente y permitida por la ruta regulatoria adoptada.

## 36.3 Entregable obligatorio

Crear:

`docs/regulatory/REG-001_intended_use_and_claims.md`

Este documento debe incluir:

- finalidad prevista;
- usuario previsto;
- paciente previsto;
- indicaciones;
- contraindicaciones;
- entorno de uso;
- duración y frecuencia;
- partes del cuerpo en contacto;
- principio de funcionamiento;
- claims permitidos;
- claims prohibidos;
- advertencias preliminares;
- clasificación regulatoria preliminar;
- mercados objetivo.

---

# 37. MARCO REGULATORIO DE REFERENCIA

## 37.1 Chile

El proyecto deberá considerar, como mínimo:

- Código Sanitario, especialmente el régimen aplicable a dispositivos médicos;
- Decreto Supremo N.º 825 de 1998 del Ministerio de Salud;
- decretos exentos que incorporen categorías de dispositivos al régimen de control;
- requisitos, guías, resoluciones e instructivos del Instituto de Salud Pública;
- exigencias de la SEREMI de Salud aplicables a fabricación, almacenamiento o distribución;
- exigencias de la Superintendencia de Electricidad y Combustibles para productos eléctricos;
- Ley N.º 19.496 sobre protección de los derechos de los consumidores;
- reglas de rotulado, seguridad, garantía, publicidad y responsabilidad aplicables;
- normativa ambiental, residuos y embalajes que corresponda;
- obligaciones tributarias, municipales, laborales y de seguridad ocupacional de Crohnoz Labs.

## 37.2 Situación regulatoria dinámica

El marco chileno de dispositivos médicos está evolucionando. Por lo tanto:

- la clasificación no se congelará únicamente con información obtenida al inicio;
- se realizará una revisión regulatoria al menos en cada gate mayor;
- antes del diseño final se verificará la versión vigente de leyes, decretos, guías y normas;
- antes de vender se solicitará revisión profesional regulatoria y legal;
- cualquier respuesta informal deberá registrarse como orientación, no como autorización.

## 37.3 Mercados futuros

El diseño podrá prepararse para convergencia futura con:

- Unión Europea;
- Estados Unidos;
- otros países de Latinoamérica.

No se iniciará un expediente internacional completo durante el MVP, pero las decisiones de diseño deberán evitar incompatibilidades innecesarias.

---

# 38. NORMAS TÉCNICAS OBJETIVO

La lista siguiente es una **matriz preliminar de aplicabilidad**. No implica que todas las normas sean obligatorias ni que las ediciones aquí mencionadas sean las que finalmente exija la autoridad.

| Área | Referencia preliminar | Aplicación esperada |
|---|---|---|
| Sistema de calidad | ISO 13485 | Diseño, producción, trazabilidad y control documental |
| Gestión de riesgos | ISO 14971 | Riesgo durante todo el ciclo de vida |
| Principios esenciales | NCh-ISO 16142-1 | Seguridad y desempeño de dispositivos médicos |
| Evaluación biológica | ISO 10993-1 y partes aplicables | Materiales en contacto directo o indirecto |
| Información del fabricante | ISO 20417 | Etiquetas, identificación e instrucciones |
| Símbolos | ISO 15223-1 | Símbolos de rotulado, si aplica |
| Usabilidad | IEC 62366-1 | Riesgos derivados de uso y errores previsibles |
| Equipo electromédico | IEC 60601-1 | Si se clasifica como equipo médico eléctrico |
| Uso domiciliario | IEC 60601-1-11 | Si es equipo médico eléctrico para hogar |
| EMC | IEC 60601-1-2 | Compatibilidad electromagnética, si aplica |
| Software | IEC 62304 | Si el software cumple funciones de seguridad |
| Seguridad de producto eléctrico | Normas IEC/NCh aplicables | Si se comercializa como aparato eléctrico no médico |
| Protección contra ingreso | IEC 60529 | Clasificación IP de envolventes |
| Muebles/asientos | Normas de resistencia y estabilidad aplicables | Estructura, fatiga, carga y vuelco |
| Calidad de agua y limpieza | Método validado propio/norma aplicable | Contaminación, limpieza y secado |
| Ciberseguridad | Guías aplicables | Solo si incorpora conectividad |

## 38.1 Registro de normas

Crear:

`docs/regulatory/REG-002_standards_matrix.xlsx` o `.csv`

Campos mínimos:

- ID;
- norma;
- edición;
- jurisdicción;
- obligatoria/recomendada/por confirmar;
- sección del producto;
- requisito relacionado;
- evidencia requerida;
- responsable;
- estado;
- fecha de revisión;
- fuente oficial.

## 38.2 Regla de versiones normativas

No se debe asumir que una edición encontrada en una conversación anterior continúa vigente. La edición deberá verificarse en la fecha de cada revisión regulatoria.

---

# 39. SISTEMA DE GESTIÓN DE CALIDAD DESDE EL INICIO

Crohnoz Labs no necesita certificarse inmediatamente bajo ISO 13485 para comenzar el concepto, pero sí deberá trabajar con una estructura documental compatible desde las primeras fases.

## 39.1 Procedimientos mínimos

Crear progresivamente:

```text
qms/
├── QMS-001_control_documental.md
├── QMS-002_control_registros.md
├── QMS-003_control_cambios_diseno.md
├── QMS-004_gestion_riesgos.md
├── QMS-005_control_proveedores.md
├── QMS-006_compras_y_recepcion.md
├── QMS-007_identificacion_trazabilidad.md
├── QMS-008_no_conformidades.md
├── QMS-009_CAPA.md
├── QMS-010_reclamos.md
├── QMS-011_vigilancia_posventa.md
├── QMS-012_retiro_producto.md
├── QMS-013_calibracion_equipos.md
├── QMS-014_capacitacion.md
├── QMS-015_liberacion_producto.md
└── QMS-016_auditoria_interna.md
```

## 39.2 Registros controlados

Todo registro deberá incluir:

- código;
- título;
- versión;
- autor;
- revisor;
- aprobador;
- fecha;
- historial de cambios;
- estado;
- ubicación del archivo fuente;
- relación con requisitos o riesgos.

## 39.3 Integridad de registros

Los resultados desfavorables no deben borrarse. Se deben conservar:

- fallas;
- prototipos descartados;
- fotografías;
- resultados de carga;
- fugas;
- sobretemperatura;
- irritación;
- problemas de limpieza;
- errores de uso;
- reclamos.

---

# 40. CONTROL FORMAL DEL DISEÑO

## 40.1 Estructura de trazabilidad

El diseño deberá mantener una cadena verificable:

```text
Necesidad del usuario
    ↓
Finalidad prevista
    ↓
Requisito de usuario
    ↓
Requisito de sistema
    ↓
Requisito de subsistema
    ↓
Especificación de diseño
    ↓
Método de verificación
    ↓
Resultado
    ↓
Validación con uso previsto
```

## 40.2 Matriz de trazabilidad

Crear:

`docs/design/DES-001_requirements_traceability_matrix.csv`

Columnas mínimas:

- ID de necesidad;
- ID de requisito;
- fuente;
- justificación;
- riesgo asociado;
- pieza o subsistema;
- método de verificación;
- criterio de aceptación;
- resultado;
- evidencia;
- versión;
- estado.

## 40.3 Baselines de diseño

Se usarán líneas base formales:

- `BL-00 Concept`;
- `BL-01 Requirements`;
- `BL-02 Architecture`;
- `BL-03 Dry Prototype`;
- `BL-04 Wet Prototype`;
- `BL-05 Engineering Prototype`;
- `BL-06 Design Verification`;
- `BL-07 Design Validation`;
- `BL-08 Preproduction`;
- `BL-09 Commercial Release`.

Una baseline no puede alterarse sin solicitud de cambio.

## 40.4 Solicitud de cambio

Formato mínimo:

```md
# ECR-XXXX — Engineering Change Request

**Origen:**  
**Descripción del cambio:**  
**Motivo:**  
**Piezas afectadas:**  
**Requisitos afectados:**  
**Riesgos afectados:**  
**Pruebas que deben repetirse:**  
**Impacto regulatorio:**  
**Impacto en inventario:**  
**Aprobación:**  
```

---

# 41. EXPEDIENTES DEL PRODUCTO

## 41.1 DHF — Design History File

Debe demostrar cómo se desarrolló HydroSeat.

Contenido:

- plan de diseño;
- entradas;
- salidas;
- revisiones;
- verificaciones;
- validaciones;
- riesgos;
- cambios;
- decisiones;
- aprobaciones.

## 41.2 DMR — Device Master Record

Debe describir cómo fabricar una unidad aprobada.

Contenido:

- planos liberados;
- especificaciones;
- BOM;
- instrucciones de montaje;
- procesos;
- inspecciones;
- firmware;
- etiquetado;
- envase;
- manual;
- criterios de liberación.

## 41.3 DHR — Device History Record

Debe demostrar qué ocurrió con cada unidad o lote fabricado.

Contenido:

- número de serie;
- lote;
- materiales;
- proveedores;
- versión de diseño;
- operario;
- fecha;
- pruebas;
- desviaciones;
- resultado de liberación.

## 41.4 Archivo de gestión de riesgos

Debe mantenerse separado pero vinculado a requisitos, pruebas y posventa.

---

# 42. PLAN DE GESTIÓN DE RIESGOS AMPLIADO

## 42.1 Categorías de peligros

Como mínimo:

- mecánicos;
- vuelco;
- atrapamiento;
- corte;
- rotura;
- fatiga estructural;
- eléctricos;
- térmicos;
- agua y electricidad;
- presión del chorro;
- succión;
- contaminación microbiológica;
- biofilm;
- irritación química;
- biocompatibilidad;
- limpieza incompleta;
- uso compartido;
- error de montaje;
- uso por persona contraindicada;
- permanencia excesiva;
- pérdida de sensibilidad;
- fallo de sensor;
- fallo de software;
- derrame sobre piso;
- caída al levantarse;
- incompatibilidad con silla;
- sobrecarga;
- uso infantil;
- mascotas;
- transporte;
- almacenamiento;
- mantenimiento incorrecto;
- eliminación final.

## 42.2 Jerarquía de controles

Los riesgos deberán reducirse en este orden:

1. seguridad inherente por diseño;
2. medidas de protección;
3. información de seguridad.

Una advertencia no debe utilizarse para reemplazar una solución de diseño técnicamente viable.

## 42.3 Riesgo residual

Cada riesgo residual deberá:

- evaluarse;
- justificarse;
- compararse con beneficio;
- comunicarse cuando corresponda;
- revisarse con datos posventa.

---

# 43. BIOCOMPATIBILIDAD Y MATERIALES

## 43.1 Clasificación de contacto

Se deberá definir para cada pieza:

- contacto con piel intacta;
- contacto con piel comprometida;
- contacto con mucosa;
- contacto indirecto mediante agua;
- duración acumulada;
- frecuencia;
- temperatura;
- agentes de limpieza.

## 43.2 Prohibiciones iniciales

Para piezas húmedas de prototipos de uso humano no se aprobarán automáticamente:

- resinas 3D sin caracterización;
- filamentos porosos sin sellado validado;
- MDF expuesto;
- pinturas desconocidas;
- silicona de construcción sin ficha técnica;
- adhesivos no identificados;
- mangueras reutilizadas sin trazabilidad;
- metales con corrosión;
- componentes con lubricantes expuestos.

## 43.3 Selección de materiales

Cada material deberá registrar:

- fabricante;
- código;
- lote;
- composición declarada;
- ficha técnica;
- ficha de seguridad;
- temperatura de uso;
- compatibilidad química;
- método de limpieza;
- trazabilidad;
- justificación de contacto.

---

# 44. ARQUITECTURA DE SEGURIDAD ELÉCTRICA

## 44.1 Principio rector

El diseño comercial deberá minimizar energía eléctrica dentro de la zona húmeda.

## 44.2 Arquitectura preferida

- fuente certificada externa;
- muy baja tensión en la silla;
- separación física de potencia y agua;
- conectores codificados;
- protección contra inversión;
- fusible;
- limitación de corriente;
- corte térmico independiente;
- sensor de nivel;
- detección de falla;
- puesta a tierra cuando corresponda;
- envolventes con protección adecuada;
- componentes reemplazables solo mediante procedimiento definido.

## 44.3 Ensayos preliminares

- continuidad;
- aislamiento;
- fuga;
- temperatura anormal;
- bloqueo de bomba;
- sensor desconectado;
- sensor cortocircuitado;
- derrame;
- ingreso de agua;
- caída de tensión;
- recuperación después de falla.

La selección de ensayos finales dependerá de la clasificación regulatoria y de las normas aplicables.

---

# 45. INGENIERÍA DE USABILIDAD

## 45.1 Usuarios previstos

Evaluar al menos:

- usuario de contextura grande;
- usuario pequeño;
- adulto mayor;
- usuario con movilidad reducida;
- usuario con dolor;
- cuidador;
- personal de limpieza o mantenimiento.

## 45.2 Tareas críticas

- instalar cubeta;
- verificar nivel;
- preparar agua;
- comprobar temperatura;
- sentarse;
- ajustar chorro;
- levantarse;
- secarse;
- drenar;
- retirar cubeta;
- limpiar;
- volver a montar;
- detectar una falla;
- apagar de emergencia.

## 45.3 Errores previsibles

- llenar en exceso;
- usar agua demasiado caliente;
- sentarse sin cubeta correctamente instalada;
- activar bomba sin agua;
- montar manguera al revés;
- bloquear drenaje;
- usar productos químicos incompatibles;
- compartir sin limpiar;
- superar peso;
- usar durante demasiado tiempo;
- moverse bruscamente;
- modificar boquillas;
- conectar fuente no aprobada.

---

# 46. VERIFICACIÓN Y VALIDACIÓN

## 46.1 Diferencia obligatoria

- **Verificación:** demostrar que las salidas de diseño cumplen los requisitos técnicos.
- **Validación:** demostrar que el producto final satisface las necesidades del usuario y el uso previsto.

## 46.2 Plan maestro de pruebas

Crear:

`tests/VV-PLAN-001_master_verification_validation_plan.md`

Debe incluir:

- requisitos;
- método;
- muestra;
- equipo;
- calibración;
- criterio de aceptación;
- condiciones;
- responsable;
- protocolo;
- reporte;
- desviaciones.

## 46.3 Familias mínimas de pruebas

### Mecánicas

- carga estática;
- carga dinámica;
- fatiga;
- impacto al sentarse;
- estabilidad;
- vuelco;
- apoyabrazos;
- anclajes;
- extracción de cubeta;
- abuso razonablemente previsible.

### Hidráulicas

- estanqueidad;
- rebalse;
- drenaje;
- bloqueo;
- desconexión;
- fuga de manguera;
- caudal;
- presión;
- salpicaduras.

### Térmicas

- precisión;
- uniformidad;
- sobretemperatura;
- calentamiento prolongado;
- falla de sensor;
- corte independiente;
- superficie accesible.

### Higiene

- desmontaje;
- limpieza;
- secado;
- retención de agua;
- zonas inaccesibles;
- resistencia a agentes de limpieza;
- crecimiento microbiano, si corresponde.

### Human factors

- comprensión de instrucciones;
- montaje;
- uso;
- errores críticos;
- levantarse;
- limpieza;
- emergencia.

### Transporte y almacenamiento

- vibración;
- caída;
- humedad;
- temperatura;
- embalaje;
- corrosión.

## 46.4 Prohibición de pruebas humanas prematuras

No se realizarán pruebas de uso corporal con:

- estructura no validada;
- electricidad no validada;
- temperatura sin doble protección;
- materiales desconocidos;
- agua recirculada no controlada;
- boquillas de presión no caracterizada.

---

# 47. EVIDENCIA CLÍNICA Y DE DESEMPEÑO

Si HydroSeat se comercializa con finalidad terapéutica, Crohnoz Labs deberá definir una estrategia de evidencia.

Puede incluir:

- revisión bibliográfica;
- equivalencia con métodos conocidos;
- evaluación de desempeño;
- estudio de usabilidad;
- estudio piloto;
- evaluación clínica formal, si corresponde.

Antes de realizar estudios con personas distintas del desarrollador se deberá evaluar:

- protocolo;
- consentimiento;
- privacidad;
- seguro;
- revisión ética;
- investigador competente;
- criterios de inclusión/exclusión;
- reporte de eventos adversos.

---

# 48. INDUSTRIALIZACIÓN Y FABRICACIÓN

## 48.1 Diseño para manufactura

El producto final deberá evitar depender de:

- cortes manuales no repetibles;
- dimensiones tomadas “a ojo”;
- adhesivos sin dosificación;
- impresiones 3D críticas sin control;
- modificaciones artesanales por unidad;
- proveedores únicos no evaluados.

## 48.2 Plan de proceso

Cada operación deberá definir:

- entrada;
- herramienta;
- parámetros;
- operario;
- inspección;
- salida;
- registro;
- criterio de aceptación.

## 48.3 Inspección

Se definirán:

- inspección de recepción;
- inspección en proceso;
- prueba final;
- liberación;
- segregación de no conformes.

---

# 49. PROVEEDORES Y COMPONENTES

## 49.1 Clasificación

- críticos para seguridad;
- críticos para desempeño;
- no críticos.

## 49.2 Componentes críticos preliminares

- fuente de poder;
- calentador;
- sensor térmico;
- corte térmico;
- bomba;
- cubeta;
- sello;
- estructura;
- anclajes;
- materiales en contacto;
- firmware de control.

## 49.3 Expediente de proveedor

- identidad;
- país;
- certificaciones;
- ficha técnica;
- lote;
- historial;
- inspecciones;
- cambios;
- proveedor alternativo.

---

# 50. TRAZABILIDAD Y CONFIGURACIÓN

Cada prototipo desde P1 deberá tener:

- ID único;
- versión CAD;
- versión BOM;
- versión firmware;
- fecha;
- fotografías;
- materiales;
- resultados de prueba;
- desviaciones;
- disposición final.

Formato:

`HS-P3-2026-001`

Cada unidad comercial deberá tener número de serie o lote definido por el plan de trazabilidad.

---

# 51. ETIQUETADO, MANUAL Y EMPAQUE

El diseño documental debe comenzar antes de finalizar el producto.

## 51.1 Etiqueta preliminar

- fabricante;
- modelo;
- número de serie/lote;
- alimentación;
- potencia;
- límites de peso;
- límites de temperatura;
- clasificación de protección;
- advertencias;
- datos regulatorios;
- fecha de fabricación;
- símbolos aplicables.

## 51.2 Instrucciones

- finalidad;
- usuarios;
- indicaciones;
- contraindicaciones;
- instalación;
- preparación;
- uso;
- límites;
- limpieza;
- mantenimiento;
- solución de problemas;
- almacenamiento;
- eliminación;
- contacto;
- incidentes;
- garantía.

## 51.3 Publicidad

Toda pieza comercial deberá ser revisada contra `REG-001` antes de publicación.

---

# 52. POSVENTA Y TECNOVIGILANCIA

Antes de vender deberá existir un sistema para:

- recibir reclamos;
- evaluar gravedad;
- rastrear unidades;
- investigar causas;
- reportar incidentes cuando corresponda;
- ejecutar correcciones;
- actualizar riesgos;
- retirar producto;
- informar usuarios;
- conservar registros.

Indicadores mínimos:

- tasa de fugas;
- fallas térmicas;
- fallas de bomba;
- irritación;
- dificultad de limpieza;
- caídas;
- errores de uso;
- devoluciones;
- reparaciones.

---

# 53. PROPIEDAD INTELECTUAL Y CONFIDENCIALIDAD

## 53.1 Acciones tempranas

- registrar fecha y autoría de conceptos;
- conservar bocetos;
- documentar evolución;
- realizar búsqueda de anterioridades;
- evitar publicar detalles críticos antes de evaluar protección;
- definir qué será patente, diseño industrial, marca, secreto o código protegido.

## 53.2 Marca

El nombre HydroSeat es provisional. Antes de comercializar deberá revisarse disponibilidad de marca y dominio.

## 53.3 Repositorio

No todo el expediente técnico debe ser público. Se recomienda:

- repositorio privado de ingeniería;
- repositorio público separado para comunicación;
- control de acceso;
- respaldo cifrado;
- política de divulgación.

---

# 54. PRESUPUESTO POR ETAPAS

El proyecto deberá separar:

1. investigación;
2. CAD;
3. prototipo seco;
4. prototipo húmedo;
5. electrónica;
6. ensayos internos;
7. laboratorio externo;
8. propiedad intelectual;
9. consultoría regulatoria;
10. certificación;
11. preproducción;
12. herramientas;
13. envase;
14. lote piloto;
15. garantía y posventa.

No se aprobará una inversión grande sin completar el gate anterior.

---

# 55. ROADMAP COMERCIAL REESTRUCTURADO POR GATES

## Gate G0 — Oportunidad aprobada

Requiere:

- problema definido;
- usuarios;
- mercado preliminar;
- competidores;
- viabilidad inicial;
- decisión de continuar.

## Gate G1 — Estrategia regulatoria aprobada

Requiere:

- finalidad prevista;
- claims;
- clasificación preliminar;
- mercados;
- normas;
- consulta regulatoria planificada;
- presupuesto regulatorio.

## Gate G2 — Requisitos congelados

Requiere:

- PRD;
- necesidades;
- requisitos;
- riesgos iniciales;
- arquitectura;
- matriz de trazabilidad.

## Gate G3 — Concepto seleccionado

Requiere:

- alternativas comparadas;
- análisis de riesgos;
- concepto Figma;
- interfaz con silla;
- plan de verificación.

## Gate G4 — Prototipo seco validado internamente

Requiere:

- estructura;
- carga;
- estabilidad;
- ergonomía preliminar;
- revisión formal.

## Gate G5 — Prototipo húmedo validado internamente

Requiere:

- estanqueidad;
- drenaje;
- extracción;
- limpieza;
- temperatura pasiva;
- riesgos actualizados.

## Gate G6 — Prototipo de ingeniería

Requiere:

- bomba;
- calentamiento;
- controles;
- protección;
- materiales definidos;
- firmware controlado.

## Gate G7 — Diseño verificado

Requiere:

- todos los requisitos técnicos probados;
- reportes aprobados;
- desviaciones cerradas;
- expediente de riesgos actualizado.

## Gate G8 — Diseño validado

Requiere:

- uso previsto;
- usuarios representativos;
- usabilidad;
- manual;
- claims;
- beneficio-riesgo.

## Gate G9 — Diseño transferido a producción

Requiere:

- DMR;
- procesos;
- proveedores;
- inspecciones;
- trazabilidad;
- lote piloto.

## Gate G10 — Liberación regulatoria y comercial

Requiere:

- autorizaciones aplicables;
- certificaciones;
- etiquetado;
- garantía;
- posventa;
- retiro;
- aprobación ejecutiva de Crohnoz Labs.

---

# 56. CRITERIOS DE NO-GO

El proyecto debe detenerse o rediseñarse si ocurre alguno de estos casos:

- no se puede garantizar estabilidad;
- el peso recae sobre la cubeta;
- no puede limpiarse completamente;
- la temperatura no puede limitarse con independencia;
- existe energía peligrosa en zona húmeda;
- los materiales no pueden justificarse;
- el costo de cumplimiento vuelve inviable el producto;
- la finalidad prevista requiere evidencia inalcanzable;
- el uso genera riesgos superiores al beneficio;
- no puede fabricarse de forma repetible;
- no puede trazarse una unidad;
- la autoridad determina una ruta incompatible con el plan comercial.

---

# 57. NUEVA ESTRUCTURA DOCUMENTAL

```text
hydroseat/
├── README.md
├── ROADMAP_MASTER.md
├── STATUS.md
├── CHANGELOG.md
├── governance/
├── qms/
├── regulatory/
├── design_history_file/
│   ├── planning/
│   ├── inputs/
│   ├── outputs/
│   ├── reviews/
│   ├── verification/
│   ├── validation/
│   └── changes/
├── risk_management_file/
├── device_master_record/
├── device_history_records/
├── cad/
├── electronics/
├── firmware/
├── prototypes/
├── tests/
├── usability/
├── clinical/
├── suppliers/
├── manufacturing/
├── labeling/
├── post_market/
├── intellectual_property/
└── references/
```

---

# 58. ESTADO REVISADO Y PRÓXIMO TRABAJO

## Estado

**Fase activa revisada:** Gate G1 — Estrategia regulatoria y finalidad prevista.

La medición de la silla sigue siendo necesaria, pero ya no es el primer trabajo formal. Antes debe definirse qué producto pretende vender Crohnoz Labs.

## Próximos documentos, en orden

1. `REG-001_intended_use_and_claims.md`
2. `REG-002_regulatory_classification_preliminary.md`
3. `REG-003_standards_matrix.csv`
4. `DES-001_user_needs.md`
5. `DES-002_product_requirements.md`
6. `RMF-001_risk_management_plan.md`
7. `DES-003_chair_measurement_protocol.md`
8. `STATUS.md`

## Próxima decisión obligatoria

Seleccionar una ruta provisional:

- bienestar/confort;
- dispositivo médico terapéutico.

La decisión puede revisarse, pero debe existir antes de continuar con diseño comercial, publicidad y validación.

---

# 59. FUENTES REGULATORIAS DE PARTIDA

Estas fuentes deben verificarse nuevamente antes de cada gate regulatorio:

- Instituto de Salud Pública de Chile — Agencia Nacional de Dispositivos Médicos.
- Biblioteca del Congreso Nacional — Código Sanitario y Decreto Supremo N.º 825/1998.
- Decreto Exento N.º 25/2026 del Ministerio de Salud.
- Instituto Nacional de Normalización.
- Superintendencia de Electricidad y Combustibles.
- ISO e IEC para estado vigente de normas.

---

# 60. APROBACIÓN DE ESTA REVISIÓN

**Versión:** `0.2.0-regulatory-by-design`  
**Estado:** Borrador para revisión del fundador  
**Organización:** Crohnoz Labs  
**Cambio principal:** transformación del roadmap de prototipo personal a desarrollo de producto comercial regulado.



---

# 61. DECISIÓN ESTRATÉGICA APROBADA — DISPOSITIVO MÉDICO

## 61.1 Decisión

Crohnoz Labs desarrollará HydroSeat deliberadamente como un **dispositivo médico terapéutico**, no como un simple producto de bienestar.

Esta decisión se adopta desde la etapa conceptual para impedir que materiales, arquitectura, procesos, ensayos, software, etiquetado o documentación temprana creen incompatibilidades con una futura autorización sanitaria o certificación.

## 61.2 Finalidad prevista preliminar

> HydroSeat es un dispositivo médico de uso domiciliario destinado a proporcionar descarga controlada de presión, baño de asiento con temperatura regulada e hidroterapia localizada de baja intensidad para el alivio temporal de molestias en la región perianal, bajo las indicaciones, contraindicaciones y condiciones de uso definidas por el fabricante.

Esta redacción es provisional. Debe ser revisada con apoyo clínico y regulatorio antes de congelar la línea base `BL-01 Requirements`.

## 61.3 Consecuencias de la decisión

Desde esta versión:

- toda decisión se evaluará bajo una perspectiva de dispositivo médico;
- la seguridad y el desempeño clínicamente relevantes tendrán prioridad sobre costo y estética;
- las piezas que contacten directa o indirectamente al usuario deberán tener trazabilidad;
- la arquitectura eléctrica se diseñará bajo principios de equipo médico para uso domiciliario;
- la gestión de riesgos comenzará antes del CAD detallado;
- la verificación y validación se definirán junto con los requisitos;
- la publicidad futura no podrá superar la evidencia aprobada;
- el prototipo artesanal será únicamente una herramienta de aprendizaje y no una unidad vendible;
- ninguna unidad podrá venderse hasta completar la liberación regulatoria y de calidad aplicable.

---

# 62. POLÍTICA DE CALIDAD DE CROHNOZ LABS PARA HYDROSEAT

Crohnoz Labs se compromete a diseñar, desarrollar, fabricar y mantener HydroSeat mediante procesos controlados que:

1. cumplan los requisitos regulatorios aplicables;
2. protejan a pacientes, usuarios, cuidadores y terceros;
3. aseguren desempeño consistente para la finalidad prevista;
4. integren gestión de riesgos durante todo el ciclo de vida;
5. utilicen materiales y componentes trazables;
6. mantengan evidencia objetiva de conformidad;
7. investiguen no conformidades, incidentes y reclamos;
8. impulsen mejora continua sin comprometer la configuración aprobada;
9. impidan la liberación de producto no conforme;
10. mantengan independencia entre ejecución, revisión y aprobación cuando el tamaño de la organización lo permita.

La política deberá transformarse posteriormente en un documento controlado del sistema de gestión de calidad.

---

# 63. JERARQUÍA DEL SISTEMA DE CALIDAD

## 63.1 Norma principal

La norma central del sistema de gestión de calidad será:

- **ISO 13485:2016**, o la edición vigente reconocida por los mercados objetivo al momento de certificación.

ISO 13485 será la columna vertebral porque está diseñada específicamente para organizaciones que desarrollan y fabrican dispositivos médicos.

## 63.2 Familia ISO 9000

Crohnoz Labs adoptará:

- **ISO 9000:2026** como referencia de fundamentos y vocabulario;
- **ISO 9001** como sistema de requisitos generales de calidad cuando resulte compatible y aporte valor organizacional;
- la edición vigente de ISO 9001 al momento de implementar o certificar el sistema.

### Aclaración crítica

ISO 9000 no es una certificación de producto ni un estándar de materiales. Es una norma de fundamentos y vocabulario.

ISO 9001 tampoco reemplaza ISO 13485. HydroSeat deberá priorizar ISO 13485 para el sistema regulado de dispositivos médicos. Crohnoz Labs podrá buscar conformidad o certificación adicional con ISO 9001, pero solo si implementa también todos sus requisitos y controla expresamente las diferencias entre ambos sistemas.

## 63.3 Objetivo de certificación

Objetivo de mediano plazo:

1. implementar un QMS compatible con ISO 13485 desde la etapa temprana;
2. realizar auditorías internas;
3. cerrar brechas;
4. certificar el alcance de diseño y desarrollo cuando exista suficiente madurez;
5. ampliar posteriormente el alcance a fabricación y servicio;
6. evaluar certificación paralela ISO 9001 para Crohnoz Labs.

La certificación del QMS no sustituye la conformidad técnica ni la autorización del dispositivo.

---

# 64. BASELINE DE NORMAS Y GUÍAS OBJETIVO

Las ediciones se verificarán antes de cada compra, ensayo, certificación y presentación regulatoria.

## 64.1 Gestión, riesgo y ciclo de vida

| Referencia | Rol |
|---|---|
| ISO 13485:2016 | Sistema de gestión de calidad para dispositivos médicos |
| ISO 9000:2026 | Fundamentos y vocabulario de calidad |
| ISO 9001, edición vigente | Sistema general de calidad complementario |
| ISO 14971:2019 | Gestión de riesgos del dispositivo |
| ISO/TR 24971:2020 | Guía de aplicación de ISO 14971 |
| ISO 20417, edición vigente | Información suministrada por el fabricante |
| ISO 15223-1, edición vigente | Símbolos de etiquetado |
| IEC 62366-1, edición vigente | Ingeniería de usabilidad |
| IEC 62304, edición vigente | Ciclo de vida de software, si existe software con función médica o de seguridad |

## 64.2 Seguridad biológica y materiales

| Referencia | Aplicación preliminar |
|---|---|
| ISO 10993-1:2025 | Plan general de evaluación biológica |
| ISO 10993-5 | Citotoxicidad, si corresponde |
| ISO 10993-10 | Sensibilización cutánea, si corresponde |
| ISO 10993-23 | Irritación, si corresponde |
| ISO 10993-12 | Preparación de muestras |
| ISO 10993-18 | Caracterización química |
| ISO 10993-17 | Evaluación toxicológica de constituyentes, si corresponde |
| ISO 10993-11 | Toxicidad sistémica, si el análisis lo exige |
| ISO 10993-7 | Solo si se utiliza esterilización con óxido de etileno |
| ISO 18562, partes aplicables | Solo si se incorpora una vía respiratoria, actualmente no prevista |

La selección final de partes de ISO 10993 dependerá de la naturaleza, duración y localización del contacto. No se ensayará “toda la familia” sin una evaluación biológica basada en riesgo.

## 64.3 Seguridad eléctrica y desempeño esencial

Si HydroSeat incorpora calentamiento, bomba, sensores o controles eléctricos y conserva finalidad médica:

| Referencia | Aplicación preliminar |
|---|---|
| IEC 60601-1 | Seguridad básica y desempeño esencial |
| IEC 60601-1-2 | Compatibilidad electromagnética |
| IEC 60601-1-6 | Usabilidad vinculada a IEC 62366-1 |
| IEC 60601-1-11 | Equipo médico eléctrico para entorno domiciliario |
| IEC 60529 | Protección IP de envolventes |
| IEC 62304 | Software, cuando corresponda |
| IEC 81001-5-1 | Ciberseguridad, si se agrega conectividad o software de salud en red |

La aplicabilidad exacta deberá ser confirmada por un laboratorio competente y por la ruta regulatoria elegida.

## 64.4 Limpieza y reprocesamiento

Se elaborará un método validado de limpieza y desinfección coherente con:

- materiales;
- microorganismos relevantes;
- tipo de contacto;
- uso individual o compartido;
- vida útil;
- frecuencia;
- agentes químicos;
- temperatura;
- geometría y zonas de retención.

Si el producto se vende exclusivamente para un único usuario, esto debe quedar explícito. Si se pretende uso clínico o multiusuario, la exigencia de reprocesamiento aumentará sustancialmente.

## 64.5 Mecánica, mobiliario y accesibilidad

Se investigarán y asignarán formalmente normas para:

- carga estática;
- fatiga;
- estabilidad;
- vuelco;
- durabilidad;
- ruedas;
- mecanismos de ajuste;
- atrapamiento;
- superficies accesibles;
- transferencia de usuarios con movilidad reducida.

La silla donante del prototipo no define la arquitectura comercial. El producto final deberá contar con una plataforma estructural propia o una interfaz cuyo rango de compatibilidad pueda verificarse.

---

# 65. CLASIFICACIÓN DEL CONTACTO CORPORAL — HIPÓTESIS CONSERVADORA

Hasta que un especialista defina lo contrario, se adoptará la hipótesis conservadora de que:

- existe contacto directo con piel perianal;
- puede existir contacto con piel irritada, lesionada o comprometida;
- existe contacto indirecto mediante agua recirculada;
- el uso es repetido;
- la exposición es de duración limitada por sesión, pero acumulativa;
- puede existir contaminación fecal;
- el usuario puede presentar inmunosupresión o sensibilidad aumentada.

Esta hipótesis elevará los controles de:

- materiales;
- limpieza;
- contaminación;
- geometría;
- presión;
- temperatura;
- instrucciones;
- contraindicaciones.

No se asumirá contacto equivalente a piel intacta convencional sin justificación clínica y regulatoria.

---

# 66. EQUIPO CLÍNICO Y REGULATORIO MÍNIMO

Antes de congelar requisitos médicos, Crohnoz Labs deberá incorporar asesoría documentada de:

- profesional regulatorio de dispositivos médicos;
- médico con competencia relevante, idealmente coloproctología;
- enfermería o profesional clínico con experiencia en cuidado perianal;
- ingeniería biomédica o eléctrica;
- diseño industrial y ergonomía;
- especialista en materiales o evaluación biológica;
- laboratorio de ensayos;
- abogado con experiencia sanitaria y responsabilidad de producto.

El fundador puede liderar el proyecto, pero no debe autoaprobar aspectos clínicos, regulatorios y de seguridad para los cuales no posee competencia formal.

---

# 67. DESARROLLO DEL PROTOTIPO BAJO EXENCIÓN INTERNA

## 67.1 Clasificación de los prototipos

- `CONCEPT ONLY`: forma o visualización; no usar con personas.
- `BENCH ONLY`: prueba de banco; no usar con personas.
- `DRY HUMAN FACTORS`: prueba humana seca, con riesgo aprobado.
- `WET PASSIVE`: agua previamente templada, sin electricidad integrada.
- `ENGINEERING`: componentes activos, solo después de ensayos.
- `DESIGN VERIFICATION UNIT`: fabricada bajo configuración controlada.
- `DESIGN VALIDATION UNIT`: equivalente al producto final.
- `COMMERCIAL UNIT`: liberada bajo QMS y regulación.

## 67.2 Etiquetado obligatorio del prototipo

Cada prototipo deberá llevar:

> PROTOTIPO DE INVESTIGACIÓN — NO VENDER — NO USAR CLÍNICAMENTE

## 67.3 Materiales del prototipo

Los materiales no conformes pueden usarse para validar volumen, ajuste o ensamblaje, pero:

- deberán identificarse como sustitutos;
- no podrán sustentar biocompatibilidad;
- no podrán utilizarse en validación final;
- sus resultados no podrán extrapolarse automáticamente;
- deberán registrarse en el DHR del prototipo.

---

# 68. ESTRATEGIA DE MATERIALES MÉDICOS

## 68.1 No existe un único sello “grado médico”

La aceptación de un material no dependerá solamente de que el proveedor lo anuncie como “medical grade”.

Será necesario considerar:

- formulación exacta;
- aditivos;
- colorantes;
- lubricantes;
- proceso;
- proveedor;
- lote;
- contacto;
- duración;
- limpieza;
- envejecimiento;
- evaluación química;
- evaluación toxicológica;
- evidencia biológica.

## 68.2 Materiales candidatos

Para etapas posteriores podrán evaluarse:

- siliconas de adición con documentación apropiada;
- elastómeros termoplásticos de formulación controlada;
- polímeros moldeados con trazabilidad;
- acero inoxidable adecuado para condiciones húmedas;
- aluminio protegido fuera de contacto crítico;
- espumas cerradas encapsuladas;
- textiles médicos o cubiertas impermeables validadas.

La selección definitiva se realizará mediante un `Material Selection Record`.

## 68.3 Impresión 3D

La impresión 3D podrá utilizarse en:

- utillajes;
- plantillas;
- maquetas;
- carcasas no críticas;
- pruebas geométricas.

Su uso en piezas de contacto, canales húmedos o soporte estructural final requerirá validación específica del material, proceso, acabado, limpieza y repetibilidad.

---

# 69. DESEMPEÑO ESENCIAL PRELIMINAR

Se considera desempeño esencial todo aquello cuya pérdida pueda provocar un riesgo inaceptable.

Hipótesis iniciales:

- limitar la temperatura del agua;
- impedir activación de calentamiento sin condición segura;
- impedir presión o succión dañina;
- mantener integridad estructural;
- mantener estabilidad;
- evitar liberación involuntaria de cubeta;
- mantener separación eléctrica;
- permitir apagado inmediato;
- mantener flujo dentro de rango;
- prevenir rebalse razonablemente previsible.

Estas funciones deberán vincularse a riesgos y ensayos.

---

# 70. OBJETIVOS DE DISEÑO CUANTIFICABLES — PENDIENTES DE VALIDACIÓN

Los valores siguientes son objetivos de ingeniería, no especificaciones médicas finales:

| Parámetro | Objetivo inicial |
|---|---:|
| Masa máxima de usuario | 150 kg mínimo de uso declarado |
| Carga de diseño estructural | Definida por ensayo y factor de seguridad |
| Temperatura nominal | 37–38 °C |
| Límite superior controlado | No mayor a 40 °C, sujeto a evaluación clínica |
| Duración por sesión | Por definir clínicamente |
| Profundidad de inmersión | Por validar anatómica y clínicamente |
| Presión del hydrojet | Por caracterizar y limitar |
| Tiempo de desmontaje | Objetivo menor a 2 minutos |
| Tiempo de limpieza | Objetivo menor a 10 minutos |
| Retención residual de agua | Criterio por definir |
| Vida útil | Por definir mediante análisis y ensayos |
| Nivel acústico | Por definir |
| Clasificación IP | Por definir después de arquitectura |
| Uso | Inicialmente individual y domiciliario |

No se incorporará un valor a la etiqueta o manual sin evidencia que lo respalde.

---

# 71. ACTUALIZACIÓN DEL ROADMAP — NUEVO ORDEN OBLIGATORIO

## Bloque A — Fundamentos regulatorios y clínicos

1. aprobar decisión de dispositivo médico;
2. definir finalidad prevista;
3. definir población, indicaciones y contraindicaciones;
4. obtener opinión clínica;
5. elaborar clasificación preliminar;
6. consultar formalmente al ISP;
7. definir mercados iniciales;
8. construir matriz de normas;
9. aprobar estrategia regulatoria.

## Bloque B — Sistema de calidad

1. control documental;
2. control de registros;
3. gestión de riesgos;
4. diseño y desarrollo;
5. cambios;
6. proveedores;
7. no conformidades;
8. CAPA;
9. calibración;
10. capacitación.

## Bloque C — Diseño

1. necesidades de usuario;
2. requisitos;
3. riesgos;
4. arquitectura;
5. concepto;
6. CAD;
7. prototipos;
8. revisiones formales.

## Bloque D — Verificación, validación y transferencia

1. verificación;
2. evaluación biológica;
3. EMC y seguridad eléctrica;
4. usabilidad;
5. validación;
6. transferencia;
7. lote piloto;
8. liberación.

No se permitirá que la urgencia por fabricar salte los bloques A y B.

---

# 72. PRÓXIMOS ENTREGABLES APROBADOS

El trabajo inmediato ya no será construir la silla. Se deberán crear, en este orden:

1. `REG-001_intended_use_indications_contraindications.md`
2. `REG-002_chile_classification_strategy.md`
3. `CLN-001_clinical_needs_and_claims_plan.md`
4. `QMS-001_quality_manual_scope.md`
5. `QMS-002_document_and_record_control.md`
6. `RMF-001_risk_management_plan.md`
7. `REG-003_standards_applicability_matrix.csv`
8. `DES-001_user_needs.md`
9. `DES-002_system_requirements.md`
10. `DES-003_chair_measurement_protocol.md`

Solo después se iniciará el modelado detallado.

---

# 73. ESTADO OFICIAL DESPUÉS DE ESTA DECISIÓN

**Ruta de producto:** Dispositivo médico terapéutico.  
**Entorno inicial previsto:** Domiciliario.  
**Usuario inicial previsto:** Adulto.  
**Uso inicial previsto:** Individual.  
**Estado del diseño:** Conceptual.  
**Estado regulatorio:** Clasificación pendiente.  
**Estado de QMS:** Planificación.  
**Estado de riesgos:** Archivo por abrir.  
**Estado de prototipo:** No iniciado formalmente.  
**Venta permitida:** No.  
**Ensayo humano activo permitido:** No, hasta aprobar protocolo por etapa.  
**Próximo gate:** G1 — estrategia regulatoria aprobada.

---

# 74. NOTA DE CONTROL DE EDICIONES ISO

El proyecto no fijará para siempre las ediciones indicadas en este documento.

Al 21 de julio de 2026:

- ISO 9000:2026 se encuentra publicada;
- ISO 9001:2015 sigue siendo la edición sustituible mientras ISO 9001:2026 se encuentra en proceso final de publicación;
- ISO 13485:2016 continúa vigente y fue confirmada en 2025;
- ISO 14971:2019 continúa vigente y fue confirmada en 2025;
- ISO 10993-1:2025 es la edición publicada vigente.

Antes de auditoría o presentación regulatoria deberá revisarse:

- edición vigente;
- transición permitida;
- adopción nacional NCh;
- versión armonizada o reconocida por la jurisdicción;
- correcciones y enmiendas;
- interpretación del organismo certificador.

---

# 75. APROBACIÓN DE BASELINE MÉDICA

**Baseline:** `BL-MED-00`  
**Versión:** `0.3.0-medical-device-baseline`  
**Decisión:** HydroSeat será desarrollado como dispositivo médico.  
**Sistema de calidad principal:** ISO 13485.  
**Sistema complementario:** familia ISO 9000 e ISO 9001 cuando corresponda.  
**Gestión de riesgos:** ISO 14971.  
**Evaluación biológica:** ISO 10993 basada en riesgo.  
**Seguridad eléctrica prevista:** familia IEC 60601, sujeta a aplicabilidad.  
**Fabricante previsto:** Crohnoz Labs.  
**Estado:** Aprobado conceptualmente por el fundador; pendiente de revisión clínica y regulatoria externa.

