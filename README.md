# 🚀 Prueba Técnica: Full Stack Developer / AI

¡Hola! Bienvenido/a a la prueba técnica práctica. Este repositorio contiene el código base necesario para que puedas demostrar tus habilidades en el desarrollo de integraciones con Inteligencia Artificial.

## 🛠️ Sobre este repositorio

Para esta prueba, te damos total libertad de elegir el ecosistema en el que te sientas más cómodo/a. En este repositorio encontrarás dos carpetas con un esqueleto básico (boilerplate) ya configurado:

* 📁 **`api_nodejs`**: Servidor base construido con Node.js y Express.
* 📁 **`api_python`**: Servidor base construido con Python y Flask.

**Instrucción:** Elige **solo una** de las dos carpetas para desarrollar tu solución.

---

## 🏢 Contexto del Caso Práctico (El Problema de Negocio)

Actualmente, nuestro equipo de atención al cliente recibe cientos de correos diarios con dudas repetitivas. Queremos implementar un sistema inteligente que optimice este flujo. 

El objetivo del sistema completo sería interceptar estos correos, utilizar un LLM (Large Language Model) para analizar si la respuesta existe en nuestra base de conocimientos, redactar una respuesta adecuada y tomar una decisión:
* Si la **confianza de la IA es mayor al 90%**, el correo se envía automáticamente al cliente.
* Si la **confianza es menor al 90%** (o la IA no sabe la respuesta), debe dejar un borrador en nuestro sistema interno para revisión humana.

---

## 💻 El Reto de Código (Requerimiento Específico)

No esperamos que construyas toda la aplicación ni la conexión a la base de datos de correos en esta prueba. Tu objetivo es programar **la pieza central y más crítica** de esta arquitectura.

Deberás crear un Endpoint (ej. `POST /api/process-email`) que reciba el texto de un correo entrante, orqueste la llamada a la IA y devuelva la decisión estructurada.

### Tareas específicas:
1.  **Crear el Endpoint:** Define la ruta que recibirá el payload del correo.
2.  **Integración con IA:** Escribe el controlador que realiza la consulta al LLM. *Nota: Puedes usar una API Key real de OpenAI/Anthropic o usar la suministrada de Gemini.*
3.  **Ingeniería de Prompts:** Define claramente el prompt dentro del código. Separa las instrucciones del sistema (System Prompt) del mensaje del usuario.
4.  **Salida Estructurada (JSON):** Obliga al modelo de lenguaje a devolver una respuesta estructurada (no texto libre). El endpoint debe terminar retornando un JSON similar a este:
    
## 🎯 Qué evaluaremos en tu código:
- Manejo de Asincronía: Uso correcto de async/await (o equivalentes) al interactuar con servicios externos.
- Estructuración del Prompt: Claridad en las instrucciones dadas al modelo para evitar alucinaciones y garantizar el formato JSON.
- Manejo de Errores (Resiliencia): Uso adecuado de bloques Try/Catch. ¿Qué pasa si la API de OpenAI se cae, da timeout o devuelve un JSON malformado? Tu código no debe colapsar.
- Código Limpio: Nomenclatura clara, modularidad y separación de responsabilidades (ej. no poner toda la lógica de negocio directamente en el archivo de rutas).

## 🚀 Cómo empezar

- Entra a la carpeta de tu elección (cd api_nodejs o cd api_python).
- Revisa el archivo README.md interno de esa carpeta para instalar las dependencias e iniciar el servidor de desarrollo.
- ¡Escribe tu solución!

Durante la entrevista técnica, te pediremos que compartas tu pantalla, expliques tu código y hagamos un par de pruebas enviando correos de ejemplo a tu endpoint. 

¡Mucho éxito!