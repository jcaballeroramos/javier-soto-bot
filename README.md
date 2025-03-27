# Bot de Telegram: Javier Soto (Asistente de Dirección)

Este bot de Telegram simula una conversación con Javier Soto, Asistente de Dirección que ha trabajado en proyectos como "La sociedad de la nieve" (J.A. Bayona), "7 días en la Habana" (Elia Suleiman) y con directores como Oliver Stone y Jonathan Glazer. Utiliza OpenAI GPT para generar el texto y ElevenLabs para convertirlo en audio con la voz de Javier.

## Características

- Conversación textual utilizando GPT-4
- Generación de voz con ElevenLabs
- Dos modos de funcionamiento: texto o voz
- Sistema de autorización de usuarios
- Manejo de conversaciones persistentes

## Requisitos

- Node.js (v18 o superior)
- Una cuenta de Telegram y un token de bot (a través de BotFather)
- Una API key de OpenAI
- Una API key de ElevenLabs

## Instalación

1. Clona este repositorio:
   ```bash
   git clone <url-repositorio>
   cd elias-bot
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Crea un archivo `.env` en la raíz del proyecto con las siguientes variables:
   ```
   BOT_TOKEN="tu_token_de_telegram"
   OPENAI_API_KEY="tu_api_key_de_openai"
   ELEVEN_API_KEY="tu_api_key_de_elevenlabs"
   AUTHORIZED_USERS="id_usuario1,id_usuario2"
   ADMIN_USERS="id_usuario_admin"
   ```

   > **Nota:** Para obtener tu ID de Telegram, puedes hablar con @userinfobot en Telegram.

4. Inicia el bot:
   ```bash
   npm start
   ```

## Uso

Una vez que el bot esté en funcionamiento, puedes interactuar con él a través de Telegram:

- `/start` o `/help`: Muestra instrucciones de uso
- `/text`: Cambia a modo de respuestas en texto
- `/voice`: Cambia a modo de respuestas en voz
- `/reset`: Reinicia la conversación

Simplemente envía cualquier mensaje para iniciar una conversación con "Elías".

## Personalización

El bot viene configurado para simular a Javier Soto como Asistente de Dirección, pero puedes modificar el sistema prompt en la función `getSystemPrompt()` de la clase `StateManager` para adaptarlo a cualquier otra personalidad o caso de uso.

Para cambiar la voz, necesitarás reemplazar el ID de voz en la configuración (`CONFIG.ELEVEN_LABS.VOICE_ID`) con el ID de otra voz de tu cuenta de ElevenLabs.

## Licencia

Este proyecto está licenciado bajo la licencia ISC.