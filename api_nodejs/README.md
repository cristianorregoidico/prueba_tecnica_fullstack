# API Node.js - Prueba Técnica

API REST construida con Express.js para la prueba técnica Full Stack.

## Instalación

```bash
npm install
```

## Configuración

1. Copia el archivo `.env.example` a `.env`
2. Ajusta las variables de entorno según sea necesario

## Ejecución

**Modo desarrollo (con nodemon):**
```bash
npm run dev
```

**Modo producción:**
```bash
npm start
```

El servidor estará disponible en `http://localhost:3000`

## Endpoints

- `GET /hello` - Retorna un mensaje de bienvenida

## Estructura

- `server.js` - Configuración principal del servidor Express

## Próximos pasos para el candidato

- Crear controladores en una carpeta `controllers/`
- Crear rutas adicionales en una carpeta `routes/`
- Implementar conexión a servicios externos
- Agregar validaciones y manejo de errores
