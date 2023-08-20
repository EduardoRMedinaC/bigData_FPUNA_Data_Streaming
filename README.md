# bigData_FPUNA_Data_Streaming
Trabajo de data streaming con RedPANDA, PYTHON y KSQLDB - GRUPO 17 DIPLOMADO BIG DATA 2023 - FPUNA


INTEGRANTES DEL GRUPO 17
-Alexis Risaldi
-Rossana Saucedo
-Alma María Rojas
-Emilio Saldivar
-Eduardo Medina

# Proyecto de Análisis de Datos en Tiempo Real con Redpanda, ksqlDB y Kafka

Este proyecto demuestra cómo utilizar Redpanda, ksqlDB y Kafka para realizar análisis de datos en tiempo real. Incluye un productor de datos, un consumidor de datos y consultas predefinidas utilizando ksqlDB.

## Requisitos previos

Asegúrate de tener instalados los siguientes componentes:

- Docker
- Python (3.x recomendado)

## Configuración

1. Clona este repositorio en tu máquina local.
2. Asegúrate de que Docker esté en funcionamiento.
3. Ejecuta el siguiente comando en la raíz del proyecto para iniciar los servicios de Docker definidos en `docker-compose.yml`:

bash

docker-compose up -d

``` 
# Descripción de los Módulos
string_producer.py
Este módulo se encarga de conectarse a una fuente de datos en tiempo real a través de WebSockets, procesar los datos recibidos y enviarlos al clúster Kafka (Redpanda) para su almacenamiento y análisis.

string_consumer.py
Este módulo consume los datos del clúster Kafka (Redpanda) provenientes del productor y realiza cálculos en tiempo real para obtener el precio promedio ponderado y otros datos por cada símbolo.

# Archivo Consultas SQL.txt
Este archivo contiene definiciones de consultas y la creación de tablas Materialized View utilizando el lenguaje ksqlDB. Las consultas y tablas se centran en el procesamiento de datos en tiempo real, como cálculos de promedio ponderado, precios máximos y mínimos, y más.

# Consultas predefinidas
Para ejecutar las consultas predefinidas definidas en Consultas SQL.txt, puedes utilizar la interfaz de línea de comandos de ksqlDB o interactuar directamente con el servidor de ksqlDB y su API.

# Cierre del Proyecto
Para detener y eliminar los servicios de Docker, ejecuta el siguiente comando:

```
bash

docker-compose down
