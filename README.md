# Documentación DonARG

#### https://donarg.quieroserdonante.com.ar/


## FRONTEND PÚBLICO


- Path: **'/'** - Mapa
    - Tipos de Posta:
        - Posta. Turnos todas las semanas.
        - Colecta. Turnos solo 1 dia puntual.
        - Centro. Solo información de contacto. (No maneja sus turnos por la plataforma).
- Path: **'/sangre/{nombre_colecta}'** - Postas / Colectas de sangre
- Path: **'/plasma/{nombre_colecta}'** - Postas / Colectas Colectas de plasma
    - Stepper con pasos
        - Paso 1: Display de cards con contenido dinamico. (Turnos disponibles)
        - Paso 2: 
            Formulario de carga de datos del donante
            Dirección validada por google maps
        - Paso 3: Confirmación del turno.

## PANEL 
- Roles - [ROL] indica que urls están restringidas. 
    - Admin
    - Posta
    - Donante (No implementado)
    - Anónimo (No implementado)

- Envio de Mails automaticos
    - 


- Path: **'/login'** - Ingreso al panel
- Path: **'/panel'** [ADMIN] - Pagina principal del panel
    - Listado de postas
    - Mapa de postas

- Path: **'/panel/posta/{id_posta?}'** [ADMIN] - Gestor de postas (ABM)
    - Modificacion de datos de la posta.
    - Turnos: 
        - Tabla de turnos.
        - Impresión de la planilla de los turnos de cualquier dia.
        - Cancelación de turnos.
    - Horarios:
        - Listado de Horarios habilitados.
        - Alta de horarios.
        - Cambio de cupos, habilitar / deshabilitar horario, borrar horario.

- Path: **'panel/planilla;{datos_planilla(id de laposta, año, mes, día)'** [ADMIN,POSTA] - Impresión de planillas.

- Path: **'/admin-posta'** [POSTA] - Pagina del administrador de la posta.
    - Turnos: 
        - Tabla de turnos.
        - Impresión de la planilla de los turnos de cualquier dia.
        - Cancelación de turnos.
    - Horarios:
        - Listado de Horarios habilitados.
        - Alta de horarios.
        - Cambio de cupos, habilitar / deshabilitar horario, borrar horario.









