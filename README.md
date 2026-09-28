# Laboratorio de procesamiento de texto

Proyecto académico desarrollado para la asignatura **Procesamiento de Lenguaje Natural** de la Especialización en Inteligencia Artificial de la Universidad de Cundinamarca.

## Integrantes

- Jhoan Ricardo Ávila Gutiérrez
- Freddy Alexander Forero Rojas
- Harold Duque Castañeda

## Contenido de la entrega

- `procesamiento_texto_nlp.ipynb`: notebook completo para Google Colab. Conserva los resultados y las gráficas de la última ejecución verificada.

## Temas implementados

El notebook está organizado en tres bloques:

1. **Fundamentos de NLP**
   - Normalización de texto.
   - Stemming y lematización.
   - Eliminación de stopwords.
   - Term Frequency e Inverse Document Frequency.
   - Part-of-Speech Tagging.
   - Parsing.
   - Reconocimiento de entidades nombradas (NER).

2. **Generación de texto con un LLM**
   - Consumo de un modelo Gemini mediante API.
   - Registro de respuestas, tiempos y estados.
   - Métricas y visualizaciones básicas de monitoreo.

3. **Análisis del conjunto YouTube Statistics**
   - Descarga y limpieza automática de los datos.
   - Question Answering.
   - Summarization.
   - Sentence Similarity.
   - Text Classification.
   - Translation.
   - Text Generation.
   - Text Mining.
   - Predicción experimental del desempeño de videos.
   - Persistencia de artefactos y metadatos de ejecución.
   - Interfaz de usuario con Gradio.

## Resultados principales

- Registros iniciales: **1.881 videos** y **18.409 comentarios**.
- Registros después de la limpieza: **1.867 videos** y **18.159 comentarios**.
- Clasificación de sentimiento: exactitud de **0,7271** y F1 ponderado de **0,74**.
- Predicción de visualizaciones con Random Forest: **R² de 0,5415**, MAE de **1,2343** y RMSE de **1,6314** sobre la variable transformada.
- El notebook genera los artefactos `modelo_youtube.joblib`, `metricas_modelo.csv` y `metadatos.json` durante la ejecución.

## Cómo abrirlo en Google Colab

1. Descargue `procesamiento_texto_nlp.ipynb` desde este repositorio.
2. Ingrese a [Google Colab](https://colab.research.google.com/).
3. Seleccione **Archivo > Subir notebook** y cargue el archivo.
4. Use un entorno de ejecución de Python 3. Una GPU es opcional, pero puede acelerar la descarga y ejecución de los modelos.
5. Ejecute las celdas en orden con **Entorno de ejecución > Ejecutar todo**.

## Configuración del bloque LLM

El bloque que consume Gemini requiere una clave personal si se ejecuta nuevamente desde cero. La clave **no está incluida en el notebook ni en el repositorio**.

En Google Colab:

1. Abra el panel **Secretos** (icono de llave).
2. Cree un secreto llamado exactamente `GEMINI_API_KEY`.
3. Pegue la clave como valor.
4. Habilite el acceso del secreto al notebook.

Los bloques de análisis de YouTube utilizan modelos públicos y no dependen de esta clave.

## Datos y modelos

El conjunto [YouTube Statistics](https://www.kaggle.com/datasets/advaypatil/youtube-statistics) se descarga automáticamente con `kagglehub`. También se descargan desde Hugging Face los modelos necesarios para Question Answering y traducción. Por esta razón, la primera ejecución requiere conexión a Internet y puede tardar algunos minutos.

## Observaciones de reproducibilidad

- El notebook fue verificado con **83 celdas** y **90 resultados guardados**, sin salidas de error.
- Los resultados pueden variar ligeramente entre ejecuciones por las versiones de las librerías y los componentes aleatorios de los modelos.
- El enlace público que crea Gradio es temporal. Al ejecutar de nuevo la última celda se genera una dirección diferente.
- Los archivos descargados y los artefactos creados en Colab se eliminan cuando finaliza la sesión, salvo que se descarguen o se guarden en Google Drive.

## Tecnologías utilizadas

Python, Google Colab, NLTK, spaCy, scikit-learn, pandas, NumPy, Matplotlib, Seaborn, Transformers, Hugging Face, KaggleHub, Gemini y Gradio.

