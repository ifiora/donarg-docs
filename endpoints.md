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
- Path: **PUT** [ADMIN,POSTA] **'/v1/horario'** 
- Path: **DELETE** [ADMIN,POSTA] **'/v1/horario'** 
- Path: **GET** [ADMIN,POSTA] **'/v1/horario'** 
- Path: **POST** **'/v1/horario/getPath'** 


## Turno **'/v1/turno'**

- Path: **POST** **'/v1/turno'** 
- Path: **PUT** [ADMIN,POSTA] **'/v1/turno'** 
- Path: **DELETE** [ADMIN] **'/v1/turno'** 


- Path: **GET** [ADMIN,POSTA] **'/v1/turno/tabla'** 
- Path: **POST** [ADMIN,POSTA] **'/v1/turno/planilla'** 
- Path: **POST** [ADMIN,POSTA] **'/v1/turno/cancelarAdmin'** 
- Path: **POST** **'/v1/turno/cancelarGuid'** 
- Path: **POST** **'/v1/turno/getGuid'** 

## Posta **'/v1/posta'**

- Path: **POST** [ADMIN,POSTA] **'/v1/horario'** 
- Path: **PUT** [ADMIN,POSTA] **'/v1/horario'** 
- Path: **DELETE** [ADMIN,POSTA] **'/v1/horario'** 
- Path: **GET** [ADMIN,POSTA] **'/v1/horario'** 
- Path: **POST** **'/v1/horario/getPath'** 






