# EtnograUX 

### Plataforma de Registro, Análisis y Catálogo Etnográfico para UX 

Uso para ejercicios de etnografía en Diseño de Interfaces de Usuario 

CC BY Miguel Gea, v1.0 15/10/2026 



**EtnograUX** (basado en la asignatura de  [*Diseño de Interfaces de Usuario*](https://github.com/mgea/DIU)  de la Universidad de Granada) es una herramienta web ligera, independiente y basada en estándares web (*Flat Design*, Tailwind CSS y JavaScript) para la gestión, visualización, análisis cualitativo, validación y exportación de estudios etnográficos de campo aplicados al Diseño de Interacción y Experiencia de Usuario (UX).

Ámbito: **Usabilidad & Evaluación**

Método de Evaluación: **Indagación** ->  **observación** (Field Studies)  (ref: [NNGroup](https://www.nngroup.com/articles/guide-ux-research-methods/))





## Características Principales

- **Explorador y Catálogo de Casos:** Visualización de observaciones mediante tarjetas con ordenación por valoración, relevancia y año, además de filtros dinámicos por perfil de usuario (`#mayor`, `#joven`, `#extranjero`, `#con discapacidad`), categoría (`transporte`, `comercio`, `software`, `hardware`, etc.) y búsqueda textual.

- **Visualizador Bento de Ficha Individual:** Reorganización clara del estudio de caso en bloques temáticos: Datos de Observación, Matriz Cualitativa (5Ws), Evidencias Gráficas, Evaluación y Proceso de Diseño/Metodología.

- **Gestión de Imágenes Locales y Visor Modal:** Soporte para carga de imágenes en Base64 o resolución de rutas locales mediante carpetas. Ajuste visual sin recortes (`object-contain`) y visor flotante a resolución completa.

- **Métricas de Evaluación & Revisiones:** Resumen global con promedio de puntuación (1 a 5 estrellas con soporte para medias estrellas), clasificación de relevancia (*Crítico*, *Destacable*, *No relevante*) y despliegue de todas las observaciones de campo registradas.

- **Editor y Validador JSON Integrado:** Modal con comprobación de sintaxis en tiempo real, formateador automático y opción de exportación/descarga de archivos `.json`.

- **Impresión Optimizada (`@media print`):**
  - **Ficha Individual:** Layout tipo Bento de densidad alta diseñado para encajar en exactamente **1 folio A4 vertical**.
  - **Catálogo:** Rejilla espaciosa de **3 columnas x 3 filas** (9 proyectos por folio) con los filtros activos e identificadores.
  
  

## Estructura del Archivo JSON (`etnografia.json`)

Cada estudio de caso etnográfico se estructura en un único archivo JSON con la siguiente arquitectura de campos:

```json
{
  "observacion": {
    "id": "ETNO-2026-AMGR",
    "estudioCaso": "Dificultad de Elección de Billetes en Cajero Automático",
    "situacion": "Mujer que quiere sacar dinero eligiendo el tipo de billete.",
    "observador": "Elena Valenzuela",
    "donde": "Caixa Bank",
    "fecha": "2026-03-10",
    "ano": 2026,
    "duracion": "30 min (08:00 - 08:30)",
    "metodo": "observación directa",
    "explicacion": "Descripción cualitativa detallada de los hechos observados...",
    "frecuencia": "casual"
  },
  "analisis": {
    "quien": {
      "descripcion": "Mujer adulta de 54 años no habituada a cajeros.",
      "etiquetas": ["mayor", "con discapacidad"]
    },
    "que": "Quiere sacar dinero eligiendo el tipo de billete.",
    "donde": "En Caixa Bank",
    "como": "Sigue las instrucciones táctiles del terminal.",
    "porque": "Necesita efectivo para compras semanales.",
    "queEstaSucediendo": "No encuentra la opción de selección de billetes.",
    "sentimientos": ["frustración", "nerviosismo"],
    "factorCritico": "Interfaz confusa y jerarquía visual deficiente.",
    "comoMejorar": "Simplificar el flujo con botones de acceso directo en alto contraste."
  },
  "evaluacion": {
    "total": 3,
    "val": 4.5,
    "clasificacion": 2.8,
    "observaciones": [
      {
        "observador": "Elena Valenzuela",
        "valoracion": 5,
        "clasificacion": 3,
        "texto": "Caso crítico. Bloquea el flujo en horas de alta concurrencia."
      },
      {
        "observador": "Miguel Gea",
        "valoracion": 4,
        "clasificacion": 2.5,
        "texto": "Requiere rediseño de interfaz táctil."
      }
    ]
  },
  "documentacionGrafica": [
    {
      "url": "logo_diu25_mini.png",
      "pie": "Fotografía del terminal de cajero"
    }
  ],
  "palabrasClave": ["software", "hardware", "comercio"],
  "procesoDisenoMetodologia": {
    "inspiracion": {
      "referentes": ["d.stanford Ethnography Fieldguide"],
      "moodboardUrl": "[https://mgea.github.io/UX-DIU-Checklist/index.html](https://mgea.github.io/UX-DIU-Checklist/index.html)",
      "palabraConcepto": "Accesibilidad en cajeros"
    },
    "metodologia": {
      "marcoframing": "DIU Checklist",
      "fasesProceso": ["Observación directa", "Análisis 5Ws"]
    },
    "herramientas": [
      {
        "categoria": "Recursos",
        "items": ["Formulario DIU", "d.school Fieldguide"]
      }
    ]
  }
}
```





#### Referencias: 

- NNGroup. A Guide to Using User-Experience Research Methods. https://www.nngroup.com/articles/guide-ux-research-methods/ 
- IxDF - Interaction Design Foundation. (2016, November 8). What is Ethnographic Research?. IxDF - Interaction Design Foundation. https://ixdf.org/literature/topics/ethnographic-research 
- Ethnography in UX research[ https://www.userinterviews.com/ux-research-field-guide-chapter/ethnography](https://www.userinterviews.com/ux-research-field-guide-chapter/ethnography)
- d.school: Ethnography Field Guide  https://dschool.stanford.edu/tools/ethnography-field-guide



Código enhanced by GeminiAI

Granada, 15 octubre 2026 
