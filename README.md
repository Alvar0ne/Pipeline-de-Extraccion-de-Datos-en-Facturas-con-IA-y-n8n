# Proyecto de automatización de procesamiento de facturas con IA
 
## Contexto del negocio

Las empresas reciben constantemente facturas en formato PDF a través de correo electrónico, lo que obliga a revisar manualmente cada documento para extraer información relevante.

Esto dificulta responder preguntas clave como:

- ¿Cómo registrar automáticamente la información de facturas sin intervención manual?
- ¿Cómo evitar errores en la digitación de datos?
- ¿Cómo escalar el procesamiento de documentos sin aumentar carga operativa?
- ¿Cómo transformar documentos no estructurados en datos utilizables?

El objetivo de este proyecto es automatizar completamente la extracción de datos desde facturas PDF, transformándolos en información estructurada lista para su uso.

## Fuentes de datos

Se trabajó con una fuente principal de entrada:

Fuente 1: Correos electrónicos con facturas
Correos recibidos en Gmail con archivos PDF adjuntos.

Los datos presentan características típicas de documentos no estructurados:

- Información en formato PDF
- Diferente estructura entre facturas
- Texto no estandarizado
- Dificultad para extraer campos de forma directa
- Dependencia de interpretación humana


##  Instalacion y puesta en marcha

Se utilizo un contenerdor en Docker para poder instalar y correr el aplicativo n8n, en este caso fue de forma local  pero con posibilidad de pasarlo a productivo

##  Proceso de automatización

El proyecto fue desarrollado utilizando N8N,  integrando servicios externos e IA para análisis documental.

Etapas principales:

- Detección automática de correos entrantes (Gmail Trigger)
- Extracción del archivo PDF adjunto
- Envío del documento a un modelo de IA para análisis
- Generación de salida estructurada en formato JSON
- Parseo del JSON para obtener campos específicos
- Transformación de datos dentro del flujo
- Carga automática de información en Google Sheets

## Datos extraídos

El flujo extrae automáticamente los siguientes campos del cliente (receptor):

- empresa_cliente
- rut_cliente
- monto_total

Estos datos son normalizados para asegurar consistencia en su almacenamiento.

## Resultados clave

### Automatización completa del proceso

Se logró eliminar completamente la intervención manual en el registro de facturas, pasando de un proceso manual a uno 100% automatizado.


### Estandarización de datos

La salida en formato JSON permite que todos los datos tengan una estructura uniforme, facilitando su uso posterior en análisis o sistemas.

### Escalabilidad del proceso

El sistema puede procesar múltiples correos y facturas sin intervención adicional, permitiendo escalar el volumen de procesamiento sin aumentar recursos. Adicionalmente
puede ser eescalado y transformado para cualquier tipo de archivo PDF.




## Visualizaciones


- Flujo completo en n8n
- Output del análisis del documento
- JSON generado por IA
- Datos registrados en Google Sheets



## Insights estratégicos

- La automatización de documentos no estructurados es clave para optimizar procesos administrativos.
- El uso de IA permite transformar PDFs en datos estructurados sin necesidad de reglas rígidas.
- Integrar correo, procesamiento y almacenamiento en un solo flujo reduce fricción operativa.
- Este tipo de soluciones tiene impacto directo en eficiencia y reducción de costos.


## Herramientas y Tecnologías utilizadas

- Docker
- n8n
- Gmail
- Google Sheets
- API Gemini (análisis de documentos)
- JSON
- Automatización de workflows

## Estructura del proyecto

- screenshots/: imágenes del flujo y resultados
- workflow/: exportación del flujo n8n
- README.md: documentación del proyecto

##Ejecución

El flujo se ejecuta automáticamente al recibir un correo con una factura PDF.

El sistema procesa el documento en tiempo real y registra los datos en Google Sheets sin intervención manual.

##Conclusión

Este proyecto demuestra cómo automatizar completamente un proceso administrativo utilizando integración de herramientas, IA y estructuración de datos.

El valor no está solo en automatizar, sino en convertir documentos no estructurados en información útil, lista para ser utilizada en la toma de decisiones.

