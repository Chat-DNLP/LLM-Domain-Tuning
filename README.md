# Ajuste Fino de Modelos de Lenguaje para Aplicaciones Específicas

Este repositorio contiene un Jupyter Notebook para realizar el ajuste fino de modelos de lenguaje de gran tamaño (LLMs) y adaptarlos a casos de uso específicos. El notebook demuestra un enfoque para el ajuste fino utilizando conjuntos de datos con pares de instrucciones y respuestas, empleando técnicas como LoRA y SFT para mayor eficiencia. Se pretende que el modelo se ajuste para realizar la suma de números enteros.

## Características
- **Ajuste Fino con Datos de tipo 'instruct':** Adapta modelos para seguir instrucciones del usuario de manera efectiva utilizando conjuntos de datos emparejados.
- **Adaptación de Bajo Rango (LoRA):** Optimiza el entrenamiento del modelo con menores requisitos computacionales.
- **Evaluación y Personalización:** Incluye pasos para generar y probar conjuntos de datos para medir el desempeño del modelo en tareas personalizadas.

## Estructura del Notebook
### Paso 1: Ajuste Fino con Conjuntos de Datos 'instruct'
- Importación del modelo pre-entrenado y el tokenizador (`unsloth/mistral-7b-instruct-v0.2-bnb-4bit`).
- Preparación de un conjunto de datos de entrenamiento con pares de instrucciones y respuestas de números múltiplos de 3.
- Configuración de LoRA y SFT para un ajuste fino eficiente.
- Guardado del modelo ajustado para su uso posterior.

### Paso 2: Ajuste Fino Personalizado para Casos de Uso Específicos
- Generación de nuevos conjuntos de datos para tareas especializadas, como garantizar que los números generados no sean múltiplos de tres.
- Aplicación de técnicas de ajuste fino para adaptar aún más el modelo.

### Paso 3: Evaluación del Modelo
- Generación de datos de evaluación para probar la precisión del modelo en tareas específicas.
- Medición de métricas de desempeño y guardado de los resultados de evaluación.

## Bibliotecas
- **Hugging Face Transformers:** Carga del modelo y el tokenizador, utilidades de entrenamiento.
- **LoRA (Low-Rank Adaptation):** Ajuste eficiente de parámetros para el ajuste fino.
- **Datasets:** Manejo y tokenización de conjuntos de datos de entrada.
- **Weights & Biases (WandB):** Seguimiento y monitorización de experimentos.

## Requisitos Previos
- Python 3.8+
- Entorno con soporte GPU para entrenamiento eficiente
- Dependencias (instalar con pip):
  ```bash
  pip install bitsandbytes==0.44.1 datasets==3.1.0 peft==0.13.2 wandb==0.18.7 trl==0.12.1
  ```

## Cómo Usar
1. Clona este repositorio:
   ```bash
   git clone <url-del-repositorio>
   cd <carpeta-del-repositorio>
   ```
2. Abre el notebook en Jupyter o Google Colab.
3. Sigue las instrucciones en cada sección para preparar los conjuntos de datos, ajustar el modelo y evaluar su desempeño.

## Resultados
- Modelos ajustados guardados localmente o en la nube (por ejemplo, Google Drive).
- Resultados de evaluación en formato JSON que detallan la precisión del modelo y los errores.

## Participantes

- [Susana Suárez](https://github.com/susanasrez).
- [Mara Pareja](https://github.com/marapareja17).


