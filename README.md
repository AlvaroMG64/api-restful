<p align="center">
  <a href="https://laravel.com" target="_blank">
    <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
  </a>
</p>

# API RESTful con Laravel

Esta es una API RESTful construida con Laravel que permite registrar usuarios, iniciar sesión, gestionar posts y usar tokens de autenticación mediante **Sanctum**.

---

## Endpoints disponibles

| Método | Endpoint | Descripción |
|--------|---------|-------------|
| POST   | `/api/register` | Registro de usuario |
| POST   | `/api/login` | Login de usuario |
| POST   | `/api/logout` | Logout (requiere token) |
| GET    | `/api/posts` | Listar posts (requiere token) |
| GET    | `/api/posts/{id}` | Mostrar post por ID (requiere token) |
| POST   | `/api/posts` | Crear post (requiere token) |
| PUT/PATCH | `/api/posts/{id}` | Actualizar post (requiere token) |
| DELETE | `/api/posts/{id}` | Borrar post (requiere token) |

---

## Autenticación

Todos los endpoints, excepto `register` y `login`, requieren **Bearer Token** en el header:

Authorization: Bearer Token
Accept: application/json
Content-Type: application/json


> Los tokens ya están visibles en las capturas de las pruebas.

---

## Pruebas realizadas en Postman

### Registro y Login

**Prueba 1: Registro correcto**  
![Captura01](capturas/Captura01.png)

**Prueba 2: Registro email duplicado**  
![Captura02](capturas/Captura02.png)

**Prueba 3: Login correcto**  
![Captura03](capturas/Captura03.png)

**Prueba 4: Login incorrecto**  
![Captura04](capturas/Captura04.png)

---

### Gestión de Posts

**Prueba 5: GET posts con token**  
![Captura05](capturas/Captura05.png)

**Prueba 6: GET posts sin token**  
![Captura06](capturas/Captura06.png)

**Prueba 7: GET post con ID inexistente**  
![Captura07](capturas/Captura07.png)

---

### Logout

**Prueba 8: Logout correcto**  
![Captura08](capturas/Captura08.png)

**Prueba 9: Logout sin token**  
![Captura09](capturas/Captura09.png)

**Prueba 10: Logout con token incorrecto**  
![Captura10](capturas/Captura10.png)

---

### Actualización y Eliminación de Posts

**Prueba 11: PUT post correcto**  
![Captura11](capturas/Captura11.png)

**Prueba 12: PUT sin token**  
![Captura12](capturas/Captura12.png)

**Prueba 13: PUT con ID inexistente**  
![Captura13](capturas/Captura13.png)

**Prueba 14: DELETE post correcto**  
![Captura14](capturas/Captura14.png)

**Prueba 15: DELETE sin token**  
![Captura15](capturas/Captura15.png)

**Prueba 16: DELETE con ID inexistente**  
![Captura16](capturas/Captura16.png)

---

**Autoría**

Álvaro Mozo Gaspar