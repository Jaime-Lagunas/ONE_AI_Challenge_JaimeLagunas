# ONE_AI_Challenge_JaimeLagunas
Este reto consiste en construir un agente de inteligencia artificial capaz de responder preguntas, utilizando documentos internos en PDF (Sistema RAG) y/o Búsqueda en la Web El agente debe estar disponible para su acceso vía Telegram y funcionará como una base de conocimiento conversacional.

# Challenge ONE AI Tech Builder – Agente de IA con RAG y Web Search

## 📖 Descripción
Este proyecto forma parte del desafío **Oracle Next Education (ONE)** en colaboración con **Alura Latam**. En específico el programa **ONE AI FOR TECH LATAM - G10**
El objetivo es construir un **agente de inteligencia artificial** capaz de responder preguntas utilizando documentos internos en formato PDF y, en caso de ser preguntas o solicitudes que no se encuentren en los PDFs , realizar búsquedas en la web. 
Esto es, un Agente de IA con RAG y Web Search, para este proyecto se usa como canal de comunicación para entrada y salida de datos un bot de Telegram el bot es: **@SoyONEChallenge_bot** 

## 🎯 Objetivo
- Procesar solicitudes recibidas vía **Telegram**. relacionadas con los **Códigos de ética y conducta** que deben ser observados por los servidores públicos del Gobierno del Estado de Oaxaca, México.  
- Consultar documentos internos mediante un sistema **RAG (Retrieval-Augmented Generation)** los documentos son: **ACUERDO POR EL QUE SE EXPIDE EL CÓDIGO DE ÉTICA PARA LAS PERSONAS SERVIDORAS PÚBLICAS DE LA ADMINISTRACIÓN PÚBLICA ESTATAL y CÓDIGO DE CONDUCTA DE LA SECRETARÍA DE HONESTIDAD, TRANSPARENCIA Y FUNCIÓN PÚBLICA**
- Realizar búsquedas en la web con **SerpAPI** cuando el RAG no contiene la información.  
- Desplegar el agente en el servicio de prueba de n8n.
- Responder entregando el resultado del workflow vía telegram indicando en cada mensajen de respuesta al final si dicha información se obtuvo del **RAG** o de la **Web**

## 🛠️ Tecnologías Utilizadas
- **n8n** – Orquestación del flujo de trabajo.  
- **Google Gemini 3 flash preview** – Modelo de chat y embeddings.  
- **Google Gemini Embeddings-001** – Modelo de embeddings.  
- **SerpAPI** – Búsquedas web.  
- **Google Drive** – Almacenamiento de documentos PDF.  
- **Telegram Bot** – Canal de interacción con usuarios.  

## ⚙️ Arquitectura del Flujo


### Entrada desde Telegram
- Telegram Trigger (mensajes entrantes).  
- Telegram Output (respuestas al usuario).  


### Agente / Orquestación
- AI Agent (Gemini 3 Chat Model).  
- Simple Memory.  
- SerpAPI (búsqueda web).  
- Query Data Tool (Embedding).  

### Sistema RAG – Embedding
- Google Drive (repositorio de PDFs).  
- Default Data Loader.  
- Embeddings con Gemini Embeddings-001.  
- Insert Data to Store.  
- Search files and folders.  

## 📸 Evidencia
- Imagen del flujo en n8n.  
- Captura de ejecución en Telegram.
- [Ver arquitectura del flujo](docs/arquitectura_de_Flujo.md)
- [Descargar flujo JSON](docs/Challenge%20ONE%20AI%20Tech%20Builder%20copy.json)

  ## 🤖 Acceso al Bot
Puedes interactuar directamente con el agente de IA a través de Telegram en el siguiente enlace:

[Acceder al bot en Telegram](https://t.me/ChallengeOneAITechBot)

> **⚠️ Nota Importante:**  :smile:
> 
> El flujo utiliza únicamente herramientas gratuitas.  
> Se recomienda no agotar los créditos diarios para que los instructores puedan probarlo adecuadamente 


## 🚀 Repositorio
Este proyecto está publicado en un repositorio público de GitHub con:
- workflow de n8n en formato JSON, lo que realmente se guarda son las estructuras de los nodos y sus conexiones,
- Documentación técnica.  
- Evidencias de ejecución.  

## 🔮 Próximos Pasos
- Extender el sistema RAG a otros formatos (Word, Excel, CSV).  
- Mejorar la memoria del agente para conversaciones más largas.  
- Desplegar en OCI para escalar el servicio o adquirir un servicio como hostinger que cuenta con un plan con n8n

> # 🌟 Agradecimiento Especial  
> 
> 🙌 **Gracias a todos los instructores y equipo de personas que hacen posible el programa ONE** por su dedicación, paciencia y compromiso.  
> 
> 📚 Su guía y acompañamiento han sido fundamentales para completar este desafío y seguir creciendo en el aprendizaje de inteligencia artificial.  🎉
>
> Atte. Jaime Ricardo Lagunas Piñón.

