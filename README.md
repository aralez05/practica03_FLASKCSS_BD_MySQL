# Práctica 03 - Flask CSS MySQL

Aplicación Web de registro de clientes desarrollada con Flask, CSS y MySQL.

## Estructura del proyecto

```
practica03_FLASKCSS_BD_MySQL/
├── .gitignore
├── .venv/
├── app.py
├── CMySql.py
├── requirements.txt
├── README.md
├── static/
│   └── css/
│       └── estilos.css
└── templates/
    ├── index.html
    ├── mostrar_cliente.html
    └── listar_clientes.html
```

## Requisitos

- Python 3
- Flask
- MySQL Server
- mysql-connector-python

## Configuración de la base de datos

```sql
CREATE DATABASE comercio;
USE comercio;

CREATE TABLE clientes (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(50) NOT NULL,
    apellido_paterno VARCHAR(50) NOT NULL,
    apellido_materno VARCHAR(50),
    fecha_nacimiento DATE,
    genero VARCHAR(15),
    correo VARCHAR(100) NOT NULL,
    telefono VARCHAR(20),
    estado VARCHAR(50),
    ciudad VARCHAR(50),
    codigo_postal VARCHAR(10),
    tipo_cliente VARCHAR(20),
    intereses VARCHAR(200),
    limite_credito DECIMAL(10,2),
    observaciones VARCHAR(250)
);
```

## Instalación

1. Crear entorno virtual:
   ```
   python -m venv .venv
   ```

2. Activar entorno virtual:
   ```
   .venv/Scripts/Activate.ps1   # Windows PowerShell
   source .venv/bin/activate     # Linux/Mac
   ```

3. Instalar dependencias:
   ```
   pip install -r requirements.txt
   ```

4. Ejecutar la aplicación:
   ```
   python app.py
   ```

5. Abrir en el navegador: http://localhost:5000
