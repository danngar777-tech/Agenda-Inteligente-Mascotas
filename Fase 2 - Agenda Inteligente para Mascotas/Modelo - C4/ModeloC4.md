# Modelo C4

## Introducción

El Modelo C4 permite representar la arquitectura del sistema mediante diferentes niveles de abstracción, facilitando la comprensión de los componentes y sus interacciones.

## Nivel 1: Contexto

Este nivel muestra la interacción entre el usuario y el Sistema de Agenda Inteligente para Mascotas, así como los sistemas externos utilizados para el envío de recordatorios.



```mermaid
flowchart LR

    Usuario["👤 Propietario de Mascota"]

    Sistema["🐾 Sistema de Agenda Inteligente para Mascotas"]

    Correo["📧 Servicio de Correo Electrónico"]

    Usuario -->|Gestiona mascotas, citas y vacunas| Sistema
    Sistema -->|Envía recordatorios| Correo
```



## Nivel 2: Contenedores

Este nivel presenta los componentes principales del sistema: Aplicación Web, API Backend y Base de Datos.

```mermaid
flowchart LR

    Usuario["👤 Usuario"]

    Frontend["🌐 Aplicación Web
    Frontend"]

    Backend["⚙️ API Backend"]

    BD[("🗄️ Base de Datos MySQL")]

    Usuario -->|Interactúa| Frontend

    Frontend -->|Solicita información| Backend

    Backend -->|Lee y almacena datos| BD

    BD -->|Devuelve información| Backend

    Backend -->|Responde| Frontend

    Frontend -->|Muestra resultados| Usuario
```

## Conclusión

Los diagramas C4 permiten comprender de forma clara la estructura general del sistema y la distribución de responsabilidades entre sus diferentes componentes, facilitando futuras etapas de desarrollo y mantenimiento.