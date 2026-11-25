# Contratos tecnológicos, comercio electrónico y protección de datos

> Plugin de Claude Code `formularios-tecnologia-y-proteccion-de-datos` · **32 formularios** · Mercantil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para el negocio digital: desarrollo de software, hosting, mantenimiento y outsourcing informático, tienda online y condiciones de uso, contratos de encargado y corresponsable del tratamiento, cláusulas y documentos del RGPD y de la LOPDGDD.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 32 está al final):

- **Contratos, pactos y cláusulas** (27). Por ejemplo: Contrato de suscripción a plataforma digital de contenidos con opción de aportar contenido propio; Cláusula de protección de datos para los contratos de trabajo; Contrato entre corresponsables del tratamiento de datos personales.
- **Escritos de trámite y otros** (5). Por ejemplo: Mantenimiento de equipos informáticos (contrato); Asistencia técnica de sistemas informáticos (contrato); Prestación de servicios informáticos (contrato).

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Contrato de encargado del tratamiento (art. 28 RGPD)»
   - «Contrato de desarrollo de software a medida»
   - «Condiciones generales de una tienda online»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-tecnologia-y-proteccion-de-datos:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-tecnologia-y-proteccion-de-datos:contrato-suscripcion-plataforma-digital-contenidos-mer-0750`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 1.793 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-tecnologia-y-proteccion-de-datos@formularios-tecnologia-y-proteccion-de-datos`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-tecnologia-y-proteccion-de-datos
/plugin install formularios-tecnologia-y-proteccion-de-datos@formularios-tecnologia-y-proteccion-de-datos
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-tecnologia-y-proteccion-de-datos`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-tecnologia-y-proteccion-de-datos/releases/latest/download/formularios-tecnologia-y-proteccion-de-datos.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (32)

| Código | Formulario | Skill |
|---|---|---|
| MER-0750 | Contrato de suscripción a plataforma digital de contenidos con opción de aportar contenido propio | `contrato-suscripcion-plataforma-digital-contenidos-mer-0750` |
| MER-0751 | Cláusula de protección de datos para los contratos de trabajo | `clausula-proteccion-datos-contratos-trabajo-mer-0751` |
| MER-0752 | Contrato entre corresponsables del tratamiento de datos personales | `contrato-entre-corresponsables-tratamiento-datos-mer-0752` |
| MER-0753 | Contrato de encargo del tratamiento de datos personales entre responsable y encargado | `contrato-encargo-tratamiento-datos-personales-entre-mer-0753` |
| MER-0754 | Contrato de compraventa de un sitio web | `contrato-compraventa-sitio-web-mer-0754` |
| MER-0755 | Mantenimiento de equipos informáticos (contrato) | `mantenimiento-equipos-informaticos-contrato-mer-0755` |
| MER-0756 | Asistencia técnica de sistemas informáticos (contrato) | `asistencia-tecnica-sistemas-informaticos-contrato-mer-0756` |
| MER-0757 | Prestación de servicios informáticos (contrato) | `prestacion-servicios-informaticos-contrato-mer-0757` |
| MER-0758 | Contrato de compraventa de un nombre de dominio | `contrato-compraventa-nombre-dominio-mer-0758` |
| MER-0759 | Contrato de publicidad en internet mediante banners | `contrato-publicidad-internet-mediante-banners-mer-0759` |
| MER-0760 | Contrato de creación y gestión de tienda virtual | `contrato-creacion-gestion-tienda-virtual-mer-0760` |
| MER-0761 | Condiciones generales de uso de un sitio web | `condiciones-generales-uso-sitio-web-mer-0761` |
| MER-0762 | Registro y renovación de nombres de dominio (contrato) | `registro-renovacion-nombres-dominio-contrato-mer-0762` |
| MER-0763 | Contrato de diseño de un sitio web | `contrato-diseno-sitio-web-mer-0763` |
| MER-0764 | Contrato de alojamiento web (hosting) | `contrato-alojamiento-web-hosting-mer-0764` |
| MER-0765 | Contrato de enlaces entre portales web (links) | `contrato-enlaces-entre-portales-web-links-mer-0765` |
| MER-0766 | Contrato de suministro de contenidos para sitios web | `contrato-suministro-contenidos-sitios-web-mer-0766` |
| MER-0767 | Condiciones generales de contratación electrónica (modelo) | `condiciones-generales-contratacion-electronica-modelo-mer-0767` |
| MER-0768 | Contrato de mantenimiento de sistemas informáticos | `contrato-mantenimiento-sistemas-informaticos-mer-0768` |
| MER-0769 | Auditoría informática (contrato) | `auditoria-informatica-contrato-mer-0769` |
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

## Privacidad

Ver `PRIVACY.md`.
