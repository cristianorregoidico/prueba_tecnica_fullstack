# API Python - Prueba Técnica

API REST construida con Flask para la prueba técnica Full Stack.

## Instalación

**Crear entorno virtual:**
```bash
python3 -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

**Instalar dependencias:**
```bash
pip install -r requirements.txt
```

## Configuración

1. Copia el archivo `.env.example` a `.env`
2. Ajusta las variables de entorno según sea necesario

## Ejecución

**Modo desarrollo:**
```bash
python app.py
```

El servidor estará disponible en `http://localhost:5000`

## Endpoints

- `GET /hello` - Retorna un mensaje de bienvenida

## Estructura

- `app.py` - Configuración principal de la aplicación Flask

## Próximos pasos para el candidato

- Crear controladores en un módulo `controllers/`
- Crear rutas en un módulo `routes/`
- Implementar conexión a servicios externos
- Agregar validaciones y manejo de errores
