# Proyecto de Gestión de Turnos

Este proyecto es una plataforma para gestionar turnos. Se compone de dos partes:

- **Frontend:** Utilizando [Astro](https://astro.build/) y Node.js.
- **Backend:** Con [Flask](https://flask.palletsprojects.com/) y JWT para autenticación.

## Tecnologías Utilizadas

### Frontend
- **Astro:** Framework moderno para construir sitios web.  
  - Página oficial: [astro.build](https://astro.build/)
- **Node.js y npm:** Requeridos para ejecutar Astro.  
  - Descarga Node.js: [nodejs.org](https://nodejs.org/en/download/)

### Backend
- **Python:** Lenguaje de programación para el backend.  
  - Descarga Python: [python.org/downloads](https://www.python.org/downloads/)
- **Flask:** Microframework para construir aplicaciones web en Python.  
  - Documentación: [Flask](https://flask.palletsprojects.com/)
- **Otros módulos de Python:** Flask-CORS, Flask-SQLAlchemy, Flask-Migrate, Flask-Bcrypt, Flask-JWT-Extended, entre otros.  
  - Todos se instalan mediante `pip` usando el archivo `requirements.txt`.

## Configuración del Proyecto

### 1. Clonar el Repositorio
Clona el repositorio en tu máquina local:

```bash
git clone <URL_DEL_REPOSITORIO>
cd <nombre_del_repositorio>
```

---

## Configuración del Backend

### 1. Crear y Activar el Entorno Virtual
Crea un entorno virtual para aislar las dependencias:

```bash
python -m venv venv
```

- En Windows:
  ```bash
  venv\Scripts\activate
  ```
- En Mac/Linux:
  ```bash
  source venv/bin/activate
  ```

### 2. Instalar Dependencias del Backend
Instala las dependencias con:

```bash
pip install -r requirements.txt
```

### 3. Configurar Variables de Entorno
Crea un archivo `.env` en la raíz del proyecto con el siguiente contenido:

```bash
DATABASE_URL=sqlite:///app.db
JWT_SECRET_KEY=tu_clave_secreta
```

_Reemplaza `tu_clave_secreta` por una cadena segura._

### 4. Inicializar la Base de Datos
Ejecuta los siguientes comandos para inicializar la base de datos y aplicar las migraciones:

```bash
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
```

### 5. Ejecutar el Servidor Backend
Levanta el servidor de desarrollo:

```bash
python flask_server.py
```

El servidor se ejecutará en [http://127.0.0.1:3000/](http://127.0.0.1:3000/).

---

## Configuración del Frontend

### 1. Ubicación del Frontend
Navega a la carpeta del frontend (por ejemplo, `frontend/`):

```bash
cd frontend
```

### 2. Instalar Dependencias del Frontend
Instala las dependencias utilizando npm:

```bash
npm install
```

### 3. Ejecutar el Servidor de Desarrollo del Frontend
Levanta el servidor de desarrollo:

```bash
npm run dev
```

Generalmente, Astro levanta el proyecto en [http://localhost:3000](http://localhost:3000) o en otro puerto indicado en la configuración.

---

## Rutas Disponibles en el Backend

- **POST /register:** Registra un nuevo usuario.
- **POST /login:** Inicia sesión y obtiene un token JWT.
- **GET /protected:** Ruta protegida, requiere autenticación JWT.

---

## Contribución

Si deseas contribuir:

1. Haz un fork del repositorio.
2. Crea una nueva rama:  
   ```bash
   git checkout -b feature/nueva-caracteristica
   ```
3. Realiza tus cambios y haz commit:  
   ```bash
   git commit -am "Agrega nueva característica"
   ```
4. Haz push a tu rama:  
   ```bash
   git push origin feature/nueva-caracteristica
   ```
5. Crea un Pull Request.

---

## Enlaces de Descarga

- **Python:** [python.org/downloads](https://www.python.org/downloads/)
- **Flask:** [flask.palletsprojects.com](https://flask.palletsprojects.com/)
- **Node.js:** [nodejs.org/en/download](https://nodejs.org/en/download/)
- **Astro:** [astro.build](https://astro.build/)
- **Express (si llegas a usarlo en el backend o en otro servicio):** [expressjs.com](https://expressjs.com/)

---

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

