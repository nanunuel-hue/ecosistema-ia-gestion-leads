# Ecosistema IA - Gestión Inteligente de Leads

## Descripción

Sistema automatizado para recibir, procesar y gestionar consultas de potenciales clientes. El flujo utiliza Make como orquestador, Notion como base de datos, OpenAI para analizar las consultas y Slack para enviar notificaciones al equipo.

## Flujo principal

1. Notion detecta el ingreso de un nuevo lead pendiente.
2. OpenAI analiza la consulta, establece su prioridad y redacta una respuesta.
3. Notion actualiza automáticamente el registro.
4. Slack notifica al equipo para realizar la validación humana.

## Manejo de errores

El escenario posee una ruta alternativa que detecta errores durante el procesamiento y los registra automáticamente en Notion, evitando la pérdida de información.

Durante la prueba, OpenAI devolvió un error 429 por falta de créditos disponibles en la API. El sistema identificó correctamente el inconveniente y ejecutó la ruta de contingencia configurada.

## Tecnologías utilizadas

* Make
* Notion
* OpenAI API
* Slack

## Archivos incluidos

* Documentación completa del proyecto en PDF.
* Blueprint del escenario de Make en formato JSON.

## Estado del proyecto

La estructura, el disparador, los filtros y el manejo de errores fueron configurados y probados. La ejecución completa de la ruta principal queda sujeta a la disponibilidad de créditos en la API de OpenAI.
