# Endpoints

## Home **'/v1'**

## Auth **'/v1/auth'**

- Path: **POST**  **'/v1/auth/login'** 

        Login
        Request:
        {
            email: string;
            password: string; 
        }

        Response:
        {
            usuario: Usuario
        }

- Path: **POST** [ADMIN,POSTA] **'/v1/auth/login/change-password'** 
        
        Request:
        {
            oldPassword: string;
            newPassword: string; 
        }

        Response:
        {
            usuario: Usuario
        }

- Path: **POST** [ADMIN] **'/v1/auth/login/posta'** 

        Crea el usuario de una posta
        Request:
        {
            postaId: string;
            email: string; 
            email: password; 
            email: urlGforms; 
        }

        Response:
        {
            datos: Posta;
            loc: string;
        }

- Path: **POST** [ADMIN] **'/v1/auth/login/check-admin'** 

        Valida si el usuario está logueado como admin y renueva el JWT de autenticación.
        Request:
        { }

        Response:
        { }

- Path: **POST** [ADMIN] **'/v1/auth/login/change-password-admin'** 

        Permite al administrador cambiar la contraseña de un usuario.
        Request:
        {
            id: int;
            password: string; 
        }

        Response:
        {
            usuario: Usuario
        }

## Horario **'/v1/horario'**

- Path: **POST** [ADMIN,POSTA] **'/v1/horario'** 

        Crea un nuevo horario.
        Request:
        {
            dia: int;
            hora: int;
            minuto: int;
            cupo: int;
            habilitado: bool;
            posta: {
                id: int;
            }
        }
- Path: **PUT** [ADMIN,POSTA] **'/v1/horario'** 

        Modifica un horario.
        Request:
        {
            id: int;
            cupo: int;
            habilitado: bool;
            
        }

        Response:
        {
            datos: Horario;
            loc: string;
        }

- Path: **DELETE** [ADMIN,POSTA] **'/v1/horario'** 

        Obtiene el listado de turnos de una posta.
        Request:
        {
            id: int;
            
        }

        Response:
        {
            datos: Horario;
            loc: string;
        }
- Path: **GET** [ADMIN,POSTA] **'/v1/horario/'** 

        Obtiene el listado de turnos de una posta.
        Request:
        {
            id: int;
        }

        Response:
        {
            datos: Horario[];
            loc: string;
        }

- Path: **POST** **'/v1/horario/getPath'** 

        Obtiene los horarios de una posta recibiendo el path de la misma.
        Request:
        {
            path: string;
            
        }

        Response:
        {
            datos: IDiaTurno;
            loc: string;
        }

## Turno **'/v1/turno'**

- Path: **POST** **'/v1/turno'** 

        Crea un turno y envía mail de confirmación.
        Request:
        {
            turno: {
                fecha: Date;
                horario: {
                    id: int;
                };
            }
            
            donante: {
                nombre: string;
                apellido: string;
                email: string;
                sexo: string;
                dni: string;
                telefono: string;
                fecha_nac: Date;
                direccion: {
                    lat: float;
                    lng: float;
                    calle: string;
                    numero: string;
                    piso: string;
                    depto: string;
                    piso: int;
                    codigo_postal: string;
                    localidad: string;
                    provincia: string;
                    ciudad: string;
                    pais: string;
                };
            }
        }

        Response:
        {
            datos: Donante;
            loc: string;
        }

- Path: **PUT** [ADMIN,POSTA] **'/v1/turno'** 

        NO IMPLEMENTADO

- Path: **DELETE** [ADMIN] **'/v1/turno'** 

        NO IMPLEMENTADO

- Path: **GET** [ADMIN,POSTA] **'/v1/turno/tabla'** 

        Obtiene los horarios de una posta recibiendo el path de la misma.
        Request:
        {
            path: string;
            
        }

        Response:
        {
            datos: Turno[];
            loc: string;
        }

- Path: **POST** [ADMIN,POSTA] **'/v1/turno/planilla'** 

        Obtiene los datos para impresión de la planilla de donantes de un día de donación.
        Request:
        {
            id: string;
            dia: Date;
        }

        Response:
        {
            datos: Turno[];
            loc: string;
        }

- Path: **POST** [ADMIN,POSTA] **'/v1/turno/cancelarAdmin'** 

        Permite al administrador cancelar un turno.
        Request:
        {
            id: int;
            razonCancelacion: string;
            
        }

        Response:
        {
            datos: Turno[];
            loc: string;
        }
        
- Path: **POST** **'/v1/turno/cancelarGuid'** 

        Permite al usuario cancelar su turno con el guid del mismo.
        Request:
        {
            guid: string;
            razonCancelacion: string;
        }

        Response:
        {
            datos: Turno[];
            loc: string;
        }
        

- Path: **POST** **'/v1/turno/getGuid'** 

        Datos para la pagina de cancelación.
        Request:
        {
            guid: string;
        }

        Response:
        {
            datos: {
                cancelado: bool;
                nombre: string;
            }
            loc: string;
        }

## Posta **'/v1/posta'**

- Path: **POST** [ADMIN,POSTA] **'/v1/posta'** 

        Crea una posta.
        Request:
        {
            posta: Posta;
        }

        Response:
        {
            datos: Posta;
            loc: string;
        }
- Path: **PUT** [ADMIN,POSTA] **'/v1/posta'** 

        Modifica una posta.
        Request:
        {
            posta: Posta;
        }

        Response:
        {
            datos: Posta;
            loc: string;
        }
        
- Path: **DELETE** [ADMIN,POSTA] **'/v1/posta'** 

        Borra una posta.
        Request:
        {
            id: int;
            
        }

        Response:
        {
            datos: Horario[];
            loc: string;
        }
- Path: **GET** [ADMIN,POSTA] **'/v1/posta'** 

        Obtiene una o multiples posta si recibe id.
        Request:
        {
            id: number;
            
        }

        Response:
        {
            datos: Posta[];
            loc: string;
        }


- Path: **POST** **'/v1/posta/getPath'** 

        Obtiene los datos de la posta.
        Request:
        {
            path: string;
            
        }

        Response:
        {
            datos: Posta;
            loc: string;
        }






