# **Registro de Usuarios con IA**

## **Descripción**
Este proyecto proporciona una API RESTful desarrollada con **FastAPI**, diseñada para gestionar el registro de usuarios con medidas de seguridad avanzadas. La aplicación incluye autenticación mediante tokens JWT para garantizar un acceso seguro y personalizado. Además, permite realizar diversas operaciones de datos protegidas, asegurando que solo los usuarios autenticados puedan acceder a las funcionalidades.

---

## **Características**
- **Registro de Usuarios**: Cifrado de contraseñas con `bcrypt` para proteger las credenciales.
- **Autenticación**: Uso de tokens JWT (JSON Web Tokens) para la gestión de sesiones.
- **Operaciones Protegidas**: Endpoints que requieren autenticación para ser accesibles.
- **Algoritmos Implementados**:
  - Ordenamiento Bubble Sort.
  - Filtro de números pares.
  - Suma de elementos.
  - Cálculo del valor máximo.
  - Búsqueda binaria.

---

## **Requisitos**
### **Herramientas Necesarias**
1. **Docker** (para el despliegue de la aplicación).
2. **Python 3.9+** (opcional para desarrollo local).
3. **FastAPI** (incluido en las dependencias).

### **Dependencias**
Las dependencias del proyecto están definidas en el archivo `requirements.txt`:
```plaintext
fastapi
uvicorn
passlib
pyjwt



Ejecución del Proyecto
1. Uso con Docker
Construir la Imagen de Docker:
bash
Copiar código
docker build -t fastapi_app .
Iniciar el Contenedor:
bash
Copiar código
docker run -d --name fastapi_container -p 8000:8000 fastapi_app
Acceso a la Aplicación:
Documentación interactiva: http://127.0.0.1:8000/docs
Redacción de solicitudes: http://127.0.0.1:8000/redoc
2. Desarrollo Local
Crear un Entorno Virtual:
bash
Copiar código
python -m venv venv
source venv/bin/activate    # macOS/Linux
.\venv\Scripts\activate     # Windows
Instalar Dependencias:
bash
Copiar código
pip install -r requirements.txt
Ejecutar la Aplicación:
bash
Copiar código
uvicorn main:app --reload
Uso de la API
Autenticación
Registro de Usuarios
Ruta: /register
Método: POST
Ejemplo de Entrada:
json
Copiar código
{
  "username": "usuario1",
  "password": "contraseña123"
}
Ejemplo de Respuesta:
json
Copiar código
{
  "message": "User registered successfully"
}
Inicio de Sesión
Ruta: /login
Método: POST
Ejemplo de Entrada:
json
Copiar código
{
  "username": "usuario1",
  "password": "contraseña123"
}
Ejemplo de Respuesta:
json
Copiar código
{
  "access_token": "tu_token_generado"
}
Endpoints Protegidos
Incluye el token en el encabezado de autorización para acceder a los endpoints protegidos:

makefile
Copiar código
Authorization: Bearer <tu_token>
Endpoints Disponibles
Bubble Sort

Ruta: /bubble-sort
Método: POST
Descripción: Ordena una lista de números con Bubble Sort.
Entrada:
json
Copiar código
{
  "numbers": [5, 3, 8, 1]
}
Salida:
json
Copiar código
{
  "numbers": [1, 3, 5, 8]
}
Filtro de Números Pares

Ruta: /filter-even
Método: POST
Descripción: Devuelve los números pares de una lista.
Entrada:
json
Copiar código
{
  "numbers": [5, 4, 8, 1]
}
Salida:
json
Copiar código
{
  "even_numbers": [4, 8]
}
(Continúa documentando los demás endpoints de manera similar...)

Notas sobre Docker
Comandos Útiles
Listar Imágenes:
bash
Copiar código
docker images
Listar Contenedores:
bash
Copiar código
docker ps -a
Detener un Contenedor:
bash
Copiar código
docker stop fastapi_container
Eliminar un Contenedor:
bash
Copiar código
docker rm fastapi_container
Próximas Mejoras
Implementar una base de datos persistente (por ejemplo, PostgreSQL).
Añadir pruebas automatizadas para los endpoints.
Mejorar las funcionalidades de autenticación con OAuth2 completo.
Contribución
Haz un fork del repositorio.
Crea una rama nueva para tu contribución:
bash
Copiar código
git checkout -b feature/nueva-funcionalidad
Realiza un pull request con tus cambios.
Licencia
Este proyecto se encuentra bajo la licencia MIT.


