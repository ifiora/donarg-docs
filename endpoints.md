# Endpoints

## Home **'/v1'**

## Auth **'/v1/auth'**

- Path: **POST**  **'/v1/auth/login'** 
- Path: **POST** [ADMIN,POSTA] **'/v1/auth/login/change-password'** 
- Path: **POST** [ADMIN] **'/v1/auth/login/posta'** 
- Path: **POST** [ADMIN] **'/v1/auth/login/check-admin'** 
- Path: **POST** [ADMIN] **'/v1/auth/login/change-password-admin'** 

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






