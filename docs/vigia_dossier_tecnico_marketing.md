# 🛡️ VIGÍA — Copiloto de Operaciones, Cumplimiento y Gestión (Kernel IA)
## Dossier Oficial Técnico, Operativo y de Posicionamiento Estratégico (Marketing & Compliance)
**Plataforma:** SGH-V1 / SGL-O2 (Sistema de Gestión de Habilitaciones)  
**Autoría & Dirección:** Omar A. Domínguez — OMARDOM Soluciones Digitales  
**Ámbito:** Arquitectura Tecnológica, Gobernanza Regulatoria y Experiencia de Usuario de Misión Crítica  
**Fecha de Emisión:** Marzo 2026  

---

## 🌟 1. Identidad Institucional y Manifiesto de Marca

<p align="center">
  <img src="../../habilitaciones-app/frontend/src/assets/vigia-avatar.png" alt="VIGÍA — Copiloto Oficial SGH-V1" width="180" style="border-radius: 32px; box-shadow: 0 0 35px rgba(6, 182, 212, 0.45); border: 2px solid rgba(6, 182, 212, 0.5);" />
</p>

<p align="center">
  <b>«El compliance normativo no debe ser una carga burocrática ciega, sino una ventaja competitiva en tiempo real.»</b><br>
  <i>VIGÍA es la inteligencia cognitiva omnipresente de SGH-V1: audita, guía y resuelve con elegancia, rigor jurídico y cero fricción.</i>
</p>

### 1.1. La Identidad Dual Canónica
- **Cara al Operador y al Cliente (Frontend / Marketing / UX):** Se denomina oficialmente **`VIGÍA — Copiloto de Operaciones y Cumplimiento`** (o sencillamente **`VIGÍA`**). Posee un avatar femenino con rasgos de autoridad técnica, serenidad y elegancia moderna, transmitiendo cercanía humana y precisión consultiva.
- **En Código, Arquitectura y Contratos (Backend / APIs / Schemas):** Se denomina estrictamente **`KernelIA`** / **`kernel_ia`** (`KernelIAService`, `kernel_cache`, `GET /api/v1/kernel-ia/contexto-operativo`, `data-kernel-cell="..."`), garantizando rigurosidad ingenieril y tipado estricto.

### 1.2. El Propósito Fundamental
En industrias como la **Seguridad Privada, Minería, Oil & Gas, Logística de Caudales y Polvorines ANMAC**, el costo del error humano es inadmisible: una credencial de vigilador vencida, un polvorín sin habilitación quinquenal vigente o un legajo médico sin apto PsyMed derivan en **clausuras judiciales, multas federales millonarias y paralización total de servicios**.

**VIGÍA no es un chatbot conversacional genérico.** Es un **árbitro normativo permanente** que opera integrado en cada pantalla de SGH-V1, previniendo contingencias antes de que ocurran y transformando la incertidumbre regulatoria en certezas operativas.

---

## 💼 2. El Eslabón de Marketing y Propuesta de Valor Empresarial

| Dimensión de Negocio | Enfoque de Software Tradicional | Valor Diferencial con VIGÍA (SGH-V1) |
| :--- | :--- | :--- |
| **Monitoreo de Vencimientos** | Listados planos que requieren auditoría manual semanal en hojas de cálculo. | **Auditoría continua 24/7:** Alertas tempranas preventivas (<30 días) y bloqueos inteligentes automáticos. |
| **Resolución de Alertas** | Carteles rojos pasivos que dicen *"Error"* y obligan al operador a buscar el legajo. | **Principio de Cero Fricción:** 1 clic transporta a la ficha exacta o entrega la planilla de subsanación. |
| **Capacitación del Personal** | Manuales en PDF de 200 páginas que los operadores raramente consultan. | **SOP y Diccionario en Pantalla (F1):** Glosario interactivo de celdas y procedimientos paso a paso. |
| **Gestión de Lotes Masivos** | Edición manual registro por registro cuando una nómina llega incompleta. | **Estrategia A + C:** Filtro en 1 clic de observados y exportador de planillas CSV Excel reversibles con importador. |
| **Relación con Clientes** | Informes estáticos mensuales desactualizados enviados por correo. | **Radar de Riesgo Exportable:** Certificados y diagnósticos de cumplimiento forenses en PDF en tiempo real. |
| **Soberanía y Privacidad** | Datos corporativos sensibles delegados en nubes de terceros (Vercel, Supabase). | **100% Self-Hosted:** Servidor dedicado LatinCloud VPS con control total de bases de datos PostgreSQL. |

---

## ⚡ 3. El Principio de Cero Fricción y la Estrategia A + C

### 3.1. La Ley de Oro de la Usabilidad
> ### 🎯 "SI VIGÍA DETECTA FALTANTES O ALERTAS, DEBE PERMITIR LLEGAR AL FALTANTE O ENTREGAR EL INSTRUMENTO PARA RESOLVERLO EN EL ACTO; JAMÁS OBLIGAR AL OPERADOR A SALIR A BUSCAR POR EL SISTEMA."

Las notificaciones huérfanas degradan la productividad. VIGÍA implementa contratos donde **toda sugerencia o alerta incluye una acción directa (`accion_url` y `accion_tipo`)**.

### 3.2. Estrategia Ante Escenarios de Gran Escala (ej. 300 Vigiladores Incompletos)
Cuando un cliente corporativo o consultora ingresa un lote voluminoso donde VIGÍA dictamina observaciones, el sistema despliega la **Estrategia Combinada A + C**:

```text
                                [ VIGÍA DETECTA CONTINGENCIA MASIVA ]
                                                  │
                 ┌────────────────────────────────┴────────────────────────────────┐
                 ▼                                                                 ▼
      [ ESTRATEGIA A — FILTRO 1 CLIC ]                              [ ESTRATEGIA C — SUBSANACIÓN A ESCALA ]
      - 1 Clic: /personas?status=INCOMPLETOS                        - Lotes masivos (>= 50 registros)
      - Grilla reduce universo solo a observados                   - Exportación 1 Clic CSV con UTF-8 BOM (\uFEFF)
      - Banner de retorno VIGÍA en cabecera                         - Apertura perfecta en Excel sin errores de tildes
      - Badges visuales "⚠️ Incompleto"                             - Estructura idéntica al Importador de Nómina
      - Edición quirúrgica inmediata                                - RRHH completa celdas y reingresa por Carga Masiva
```

- **Acción Inmediata en el HUD de VIGÍA:**
  En el Drawer y en la Sala de Espera, las alertas de VIGÍA ofrecen botones interactivos automáticos:
  - `[ 📝 Ficha Personal ]` → Salto directo a `/personas/{dni}?tab=legajo`.
  - `[ 🏢 Ver Ficha Empresa ]` → Salto directo a `/empresas/{id}?tab=habilitaciones`.
  - `[ 🔍 Filtrar Observados ]` → Aplica el filtro en la tabla activa.
  - `[ 📥 Exportar Planilla ]` → Descarga el archivo de subsanación en CSV UTF-8 BOM.

---

## 🏛️ 4. Los 8 Pilares Cognitivos en Vivo

Todo diagnóstico proyectado por VIGÍA se desglosa en 8 pilares cardinales accesibles mediante el botón flotante HUD o atajo de teclado `F1` / `Ctrl+Espacio`:

```text
+-------------------------------------------------------------------------------+
|                       VIGÍA — DRAWER COGNITIVO HUD (F1)                       |
+-------------------------------------------------------------------------------+
| [Sector & SOP] | [Rol & RBAC] | [Celdas & Inputs] | [Diagnóstico] | [Radar]   |
+-------------------------------------------------------------------------------+
| 1. SECTOR & ETAPA ACTIVA   : Módulo en uso y función dentro del macro-flujo.  |
| 2. ROL ACTIVO              : Identidad del usuario y ámbito multi-tenant.     |
| 3. MATRIZ DE PERMISOS      : Acciones autorizadas vs restringidas por perfil. |
| 4. DICCIONARIO DE CELDAS   : Propósito legal, validación y formato de campos. |
| 5. GUÍA PASO A PASO (SOP)  : Procedimiento operativo estándar reglamentario.   |
| 6. DIAGNÓSTICO VIVO        : Evaluación continua (OPERATIVO | OBSERVADO).     |
| 7. MICRO-ACCIONES 1 CLIC   : Botones para mitigar riesgos en tiempo real.     |
| 8. RADAR DE RIESGO & AUDIT : Base legal y exportación forense a texto y PDF.  |
+-------------------------------------------------------------------------------+
```

---

## 🔬 5. Arquitectura Técnica de Misión Crítica (Kernel IA)

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│                             FRONTEND SPA (REACT 19)                         │
│  - MainLayout > KernelIaProvider (Contexto Global)                          │
│  - Botón Flotante HUD reactivo con animación y severidad dinámica           │
│  - Inspector Cero-Invasivo con HTML5 data-kernel-cell="..."                 │
│  - 14 Sectores en Lazy-Loading (import() dinámico, latencia <10ms SLA)      │
└──────────────────────────────────────┬──────────────────────────────────────┘
                                       │ HTTP REST / JWT
                                       ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                          BACKEND API (FASTAPI)                              │
│  - Ruta: GET /api/v1/kernel-ia/contexto-operativo                           │
│  - Servicio: KernelIAService                                                │
│  - Caché en Memoria: KernelIACache (30s TTL, invalidación post-mutación)    │
│  - Evaluación Paralela Asíncrona (asyncio.gather):                          │
│      ├── EmpresaEvaluator   (CABA, PBA, ANMAC, PNA, Seguros RC)             │
│      ├── PersonaEvaluator   (Legajos, DNI, Domicilios, Asignaciones)        │
│      ├── TramiteEvaluator   (Cuellos de botella >2d recepción, >3d psymed)  │
│      └── ComercialEvaluator (Gestiones terminadas sin remito / Factura ARCA)│
└──────────────────────────────────────┬──────────────────────────────────────┘
                                       │ PostgreSQL 16 (LatinCloud VPS)
                                       ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                        BASE CORPORATIVA SGHV1DB                             │
│  - Tablas Auditadas: Personas, Empresas, Trámites, Habilitaciones, Remitos  │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 5.1. Inspector Cero-Invasivo (`data-kernel-cell`)
- **Prohibición de Wrappers JSX:** Queda descartado envolver inputs en componentes pesados que rompen la grilla CSS o los layouts responsivos de Tailwind CSS.
- **Detección Holográfica:** Mediante `KernelInspectorOverlay.jsx`, el usuario activa el modo inspección y posa el mouse sobre cualquier input. VIGÍA proyecta un halo cian holográfico interactivo `[ ⌖ DNI del Vigilador (Clic para explicar) ]`. Al hacer clic, abre automáticamente la pestaña **Celdas & Inputs** enseñando formato legal, validaciones y permisos RBAC.

### 5.2. Evaluación Asíncrona en Paralelo (<180ms Backend SLA)
Los evaluadores de dominio corren en paralelo sin bloquear el loop principal de eventos de FastAPI mediante `asyncio.gather(..., return_exceptions=True)`. Si un evaluador encuentra una anomalía, los restantes continúan y el sistema entrega un dictamen holístico sin caídas.

### 5.3. Caché Volátil en Memoria con Invalidación Post-Mutación
Para proteger la base de datos PostgreSQL de saturación ante consultas repetitivas de operadores, `KernelIACache` retiene las respuestas por 30 segundos. Cada vez que se crea o edita un registro (persona, empresa o trámite), el backend invoca automáticamente `POST /api/v1/kernel-ia/invalidar-cache`, asegurando que la próxima consulta lea datos frescos.

---

## 👑 6. La Cuarta Ley de Oro de SGH-V1: El Espejo Cognitivo

Junto a las Tres Leyes de Oro del NOC-PANEL (Espejo Absoluto, Cero Rollbacks Silenciosos, Servidor Limpio), rige de forma permanente la **Cuarta Ley de Oro**:

> ### ⚡ "TODO CAMBIO, NUEVO MODAL, RUTA, FORMULARIO O INSTRUMENTO DENTRO DE SGH-V1 DEBE SINCRONIZARSE OBLIGATORIAMENTE CON VIGÍA ANTES DE CONSIDERARSE TERMINADO."

### Protocolo de Sincronización Mandatorio:
1. **Inputs y Celdas:** Anotar con `data-kernel-cell="..."` y registrar en el array `celdas_modal` del sector en `src/data/kernel/sectors/`.
2. **Rutas Nuevas:** Mapear en `src/data/kernel/index.js` con chunk lazy-loaded propio.
3. **Nuevas Reglas de Negocio:** Incorporar al `procedimiento_sop` y al evaluador correspondiente en `app/domain/kernel_ia/evaluators/`.
4. **Mutaciones de Estado:** Invalidar caché volátil en endpoints de escritura.
5. **Auditoría Mandatoria para Agentes de IA:** Todo reporte final de desarrollo debe certificar el cumplimiento del Espejo Cognitivo de VIGÍA.

---

## 📈 7. Impacto Operativo y Conclusión Ejecutiva

Con la incorporación de **VIGÍA**, SGH-V1 deja de ser un software administrativo pasivo para convertirse en una **plataforma activa de defensa y eficiencia empresarial**.

- **Para el Operador Técnico:** Trabaja con la tranquilidad de contar con un copiloto que valida cada paso, previene errores de formato y le resuelve contingencias masivas en 1 clic.
- **Para los Gerentes y Directores:** Asegura trazabilidad total, predictibilidad de costos, erradicación de clausuras regulatorias y auditorías forenses instantáneas.
- **Para la Consultora y Clientes:** Representa un activo tecnológico de vanguardia que certifica el máximo estándar de seguridad corporativa y soberanía tecnológica 100% Self-Hosted.
