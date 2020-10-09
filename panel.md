# Panel de administración 

- Roles - [ROL] indica que urls están restringidas. 
    - Admin
    - Posta
    - Donante (No implementado)
    - Anónimo (No implementado)

- Envio de Mails HTML
    - [Template de Ejemplo](https://github.com/ifiora/donarg-docs/blob/master/confirmacion.html)


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

