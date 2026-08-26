# Documentación de Módulos

## Introducción

El Sistema de Agenda Inteligente para Mascotas está compuesto por varios módulos funcionales que permiten gestionar la información de los usuarios, mascotas, citas médicas, historial clínico y recordatorios automáticos.

---

# Módulo de Usuarios

## Descripción

Permite el registro y autenticación de los usuarios de la plataforma.

## Requisitos asociados

- RF1 Registro de usuarios

## Entradas

- Correo electrónico
- Contraseña

## Salidas

- Inicio de sesión exitoso
- Mensajes de validación

## Endpoints Propuestos

POST /api/usuarios/registro/
Registrar un nuevo usuario.

POST /api/usuarios/login/
Permitir el inicio de sesión.

GET /api/usuarios/{id}/
Consultar información de un usuario.

---

# Módulo de Gestión de Mascotas

## Descripción

Permite registrar, consultar, editar y actualizar la información asociada a las mascotas.

## Requisitos asociados

- RF2 Registro de mascotas
- RF3 Gestión de información de mascotas

## Entradas

- Nombre
- Especie
- Raza
- Edad
- Sexo

## Salidas

- Confirmación de registro
- Actualización de información

## Endpoints Propuestos

POST /api/mascotas/
Registrar una mascota.

GET /api/mascotas/
Consultar mascotas registradas.

GET /api/mascotas/{id}/
Consultar una mascota específica.

PUT /api/mascotas/{id}/
Actualizar información de una mascota.

DELETE /api/mascotas/{id}/
Eliminar una mascota.

---

# Módulo de Agenda

## Descripción

Administra las citas veterinarias, vacunaciones y servicios de cuidado.

## Requisitos asociados

- RF4 Agendamiento de citas
- RF5 Visualización de calendario

## Entradas

- Fecha
- Hora
- Tipo de cita
- Mascota

## Salidas

- Evento registrado
- Actualización del calendario

## Endpoints Propuestos

POST /api/citas/
Registrar una nueva cita.

GET /api/citas/
Consultar citas registradas.

GET /api/citas/{id}/
Consultar una cita específica.

PUT /api/citas/{id}/
Modificar una cita.

DELETE /api/citas/{id}/
Cancelar una cita.

---

# Módulo de Historial Médico

## Descripción

Permite almacenar registros médicos, vacunas, tratamientos y observaciones clínicas.

## Requisitos asociados

- RF6 Registro de historial de salud
- RF8 Consulta del historial

## Entradas

- Vacunas
- Tratamientos
- Observaciones

## Salidas

- Historial actualizado

## Endpoints Propuestos

POST /api/historial/
Registrar información médica.

GET /api/historial/{mascotaId}/
Consultar historial de una mascota.

PUT /api/historial/{id}/
Actualizar registro médico.

---

# Módulo de Recordatorios

## Descripción

Genera alertas para citas, vacunas y tratamientos programados.

## Requisitos asociados

- RF7 Generación de recordatorios

## Entradas

- Fecha del evento
- Tipo de evento

## Salidas

- Notificaciones automáticas

## Endpoints Propuestos

GET /api/recordatorios/
Consultar recordatorios pendientes.

POST /api/recordatorios/
Generar un nuevo recordatorio.

PUT /api/recordatorios/{id}/
Marcar recordatorio como atendido o leído.
