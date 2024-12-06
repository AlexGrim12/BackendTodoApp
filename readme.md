# Backend de Aplicación de Tareas

Este proyecto implementa un backend para una aplicación de tareas utilizando Flask y SQLite. Incluye funcionalidades para crear, leer, actualizar y eliminar tareas (CRUD).

## Requisitos Previos
- Python 3.8+
- pip (Gestor de paquetes de Python)

## Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/AlexGrim12/BackendTodoApp
   cd BackendTodoApp
   ```

2. **Crear un entorno virtual**
   ```bash
   # En Windows
   python -m venv venv

   # En macOS/Linux
   python3 -m venv venv
   ```

3. **Activar el entorno virtual**
   ```bash
   # En Windows
   venv\Scripts\activate

   # En macOS/Linux
   source venv/bin/activate
   ```

4. **Instalar dependencias**
   ```bash
   pip install -r requirements.txt
   ```

5. **Inicializar la base de datos**
   Al iniciar la aplicación, se creará automáticamente la base de datos SQLite con una tabla `tasks`.

## Ejecutar la Aplicación
1. **Ejecutar el servidor**
   ```bash
   python app.py
   ```
   Por defecto, la aplicación correrá en `http://localhost:5000`.

2. **Rutas disponibles**
   - **GET** `/tasks`: Obtiene la lista de todas las tareas.
   - **POST** `/tasks`: Crea una nueva tarea.
     ```json
     {
       "title": "Nombre de la tarea",
       "description": "Descripción de la tarea"
     }
     ```
   - **PUT** `/tasks/<task_id>`: Actualiza el estado de una tarea (completada o no).
     ```json
     {
       "completed": true
     }
     ```
   - **DELETE** `/tasks/<task_id>`: Elimina una tarea.


## Dependencias
Las dependencias necesarias están definidas en el archivo `requirements.txt`:

```plaintext
Flask
Flask-Cors
```
