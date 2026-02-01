Tema:
Agente IA [Agente Inteligente de Promesas de Pago]


Integrantes:
- Keyla Domenica Molina Rosado (@keyladome7)
- Andy Francisco Monserrate Robles (0957260045)
- José Gregorio Ponce Pérez (@JppsSmd)
- Melannie Dayanna García Solís (0943821744)
- William Ariel Rosado Rodríguez (@williamr122)
- Diego Sebastián Jiménez Coronel (@DSJC26)
- Mabel Alejandra Victores Anchundia (@maebalej-stack)
- Andrés Paul Jaramillo Guapulema (0952468395)
- Erick Alexander Melendez Rojas (0953398401)
- Josué Kenni Hurtado Santos (@josuehurta)

1. DESCRIPCIÓN
   Nuestro agente IA permite una negociación, donde el cliente puede proponer montos y fechas de pago de forma natural (ej: "pago el próximo lunes", "pago el próximo mes", "pago el próximo año"), y el sistema se encarga de estructurar bien esa información. El agente interactúa mediante texto y voz, procesa y actualiza automáticamente una base de datos en Excel, evaluando el riesgo crediticio en tiempo real.

2. ANÁLISIS
   Registro de promesas de pago mediante texto o voz
   Cálculo automático de riesgo basado en el porcentaje de abono (Umbral del 40%).
   Conversión de lenguaje natural a fechas reales.
   Requerimientos: El sistema debe ser capaz de "recordar" lo dicho en la conversación y persistir los datos en un Excel.
   El sistema captura audio, lo transcribe y analiza el tono emocional.
   Seguridad: No se exponen llaves API; se gestionan mediante variables de entorno con python-dotenv.

3. DISEÑO
   Tecnologías: Streamlit: Interfaz de usuario.
   Google GenAI: Procesamiento multimodal (Texto/Audio).
   gTTS: Respuesta por voz.
   Pandas: Manejo de base de datos en Excel.
   Pytest: Aseguramiento de calidad (QA).

4. Para ejecutar el proyecto, siga estos pasos:

Ejecución:

4.1 Crear y activar el Entorno Virtual

python -m venv venv

.\venv\Scripts\activate

4.2 Instalar dependencias

pip install -r requirements.txt

4.3 Configuración de Api Key
edita el archivo (.env.ejemplo) a (.env) y dentro de ese archivo se debe agregar la clave: GOOGLE_API_KEY=SU_API_AQUI.

4.4 Ejecutar la aplicación

streamlit run src/main.py

4.5 Ejecutar Pruebas (Opcional)
Para verificar que la lógica de riesgo y la base de datos funcionan correctamente:

python -m pytest tests/test.py

Link del video: https://drive.google.com/file/d/17faq_gOhX-RxNnZT5zGpYx2K7sjLy4y2/view?usp=sharing
