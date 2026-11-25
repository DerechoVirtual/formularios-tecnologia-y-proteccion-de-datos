---
name: indice
description: "Índice de los 32 formularios de Contratos tecnológicos, comercio electrónico y protección de datos. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Contratos tecnológicos, comercio electrónico y protección de datos: índice de formularios

> Plugin `formularios-tecnologia-y-proteccion-de-datos` · 32 formularios · normativa revisada el 25-11-2026.

## Qué es

Para el negocio digital: desarrollo de software, hosting, mantenimiento y outsourcing informático, tienda online y condiciones de uso, contratos de encargado y corresponsable del tratamiento, cláusulas y documentos del RGPD y de la LOPDGDD.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contrato de encargado del tratamiento (art. 28 RGPD)»
- «Contrato de desarrollo de software a medida»
- «Condiciones generales de una tienda online»

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-tecnologia-y-proteccion-de-datos:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Contratos, pactos y cláusulas (27)

| Código | Formulario | Skill |
|---|---|---|
| MER-0750 | Contrato de suscripción a plataforma digital de contenidos con opción de aportar contenido propio | `contrato-suscripcion-plataforma-digital-contenidos-mer-0750` |
| MER-0751 | Cláusula de protección de datos para los contratos de trabajo | `clausula-proteccion-datos-contratos-trabajo-mer-0751` |
| MER-0752 | Contrato entre corresponsables del tratamiento de datos personales | `contrato-entre-corresponsables-tratamiento-datos-mer-0752` |
| MER-0753 | Contrato de encargo del tratamiento de datos personales entre responsable y encargado | `contrato-encargo-tratamiento-datos-personales-entre-mer-0753` |
| MER-0754 | Contrato de compraventa de un sitio web | `contrato-compraventa-sitio-web-mer-0754` |
| MER-0758 | Contrato de compraventa de un nombre de dominio | `contrato-compraventa-nombre-dominio-mer-0758` |
| MER-0759 | Contrato de publicidad en internet mediante banners | `contrato-publicidad-internet-mediante-banners-mer-0759` |
| MER-0760 | Contrato de creación y gestión de tienda virtual | `contrato-creacion-gestion-tienda-virtual-mer-0760` |
| MER-0761 | Condiciones generales de uso de un sitio web | `condiciones-generales-uso-sitio-web-mer-0761` |
| MER-0763 | Contrato de diseño de un sitio web | `contrato-diseno-sitio-web-mer-0763` |
| MER-0764 | Contrato de alojamiento web (hosting) | `contrato-alojamiento-web-hosting-mer-0764` |
| MER-0765 | Contrato de enlaces entre portales web (links) | `contrato-enlaces-entre-portales-web-links-mer-0765` |
| MER-0766 | Contrato de suministro de contenidos para sitios web | `contrato-suministro-contenidos-sitios-web-mer-0766` |
| MER-0767 | Condiciones generales de contratación electrónica (modelo) | `condiciones-generales-contratacion-electronica-modelo-mer-0767` |
| MER-0768 | Contrato de mantenimiento de sistemas informáticos | `contrato-mantenimiento-sistemas-informaticos-mer-0768` |
| MER-0770 | Condiciones generales de contratación del servicio de copia de seguridad remota | `condiciones-generales-contratacion-servicio-copia-mer-0770` |
| MER-0771 | Contrato de externalización de servicios informáticos | `contrato-externalizacion-servicios-informaticos-mer-0771` |
| MER-0772 | Contrato de alojamiento de equipos en centro de datos (housing) | `contrato-alojamiento-equipos-centro-datos-housing-mer-0772` |
| MER-0773 | Contrato de prestación de aplicaciones por internet (ASP) | `contrato-prestacion-aplicaciones-internet-asp-mer-0773` |
| MER-0774 | Contrato de servicios de integración de sistemas informáticos | `contrato-servicios-integracion-sistemas-informaticos-mer-0774` |
| MER-0775 | Contrato de cesión de los derechos de explotación de un programa de ordenador | `contrato-cesion-derechos-explotacion-programa-ordenador-mer-0775` |
| MER-0776 | Contrato de desarrollo de un programa informático a medida | `contrato-desarrollo-programa-informatico-medida-mer-0776` |
| MER-0777 | Contrato de mantenimiento de un sitio web | `contrato-mantenimiento-sitio-web-mer-0777` |
| MER-0778 | Contrato de diseño y desarrollo de un sitio web | `contrato-diseno-desarrollo-sitio-web-mer-0778` |
| MER-0779 | Contrato de licencia de uso de un programa informático | `contrato-licencia-uso-programa-informatico-mer-0779` |
| MER-0780 | Contrato de depósito del código fuente de un programa ante un tercero (escrow) | `contrato-deposito-codigo-fuente-programa-ante-tercero-mer-0780` |
| MER-0781 | Contrato de mantenimiento de programas y equipos informáticos | `contrato-mantenimiento-programas-equipos-informaticos-mer-0781` |

### Escritos de trámite y otros (5)

| Código | Formulario | Skill |
|---|---|---|
| MER-0755 | Mantenimiento de equipos informáticos (contrato) | `mantenimiento-equipos-informaticos-contrato-mer-0755` |
| MER-0756 | Asistencia técnica de sistemas informáticos (contrato) | `asistencia-tecnica-sistemas-informaticos-contrato-mer-0756` |
| MER-0757 | Prestación de servicios informáticos (contrato) | `prestacion-servicios-informaticos-contrato-mer-0757` |
| MER-0762 | Registro y renovación de nombres de dominio (contrato) | `registro-renovacion-nombres-dominio-contrato-mer-0762` |
| MER-0769 | Auditoría informática (contrato) | `auditoria-informatica-contrato-mer-0769` |
