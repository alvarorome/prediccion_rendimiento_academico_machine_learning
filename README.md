
# Proyecto Final - Aprendizaje Automático 2024/2025

Este repositorio contiene el código y los archivos necesarios para reproducir los resultados del proyecto final del curso de Aprendizaje Automático.

## Estructura del repositorio

- `proyecto_final.ipynb`: Notebook principal con todo el análisis y los modelos.
- `informe_proyecto_final.tex`: Informe del proyecto en formato LaTeX (estilo NeurIPS).
- `predicciones_finales.csv`: Archivo generado con las predicciones de los dos modelos.
- `README.md`: Este archivo con las instrucciones para ejecución.
- `requirements.txt`: Este archivo contiene todas las librerías usadas junto con sus versiones.

## Instrucciones de ejecución

1. Instalación de las librerías necesarias

Las principales librerías utilizadas son:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy

Para ejecutar este proyecto, primero debes instalar las dependencias necesarias, que se encuentran listadas en el archivo requirements.txt con versiones específicas para garantizar la compatibilidad y la correcta reproducción de los resultados. Se recomienda crear y activar un entorno virtual antes de instalar las dependencias, para evitar conflictos con otras instalaciones que puedas tener en tu equipo. En Windows, puedes crear el entorno virtual con python -m venv venv y activarlo con venv\Scripts\activate. Si usas Linux o macOS, puedes crearlo con el mismo comando y activarlo con source venv/bin/activate.

Una vez activado el entorno virtual, simplemente instala las dependencias ejecutando pip install -r requirements.txt desde la carpeta del proyecto. Este comando instalará las versiones exactas de las librerías requeridas: matplotlib 3.10.0, numpy 2.2.2, pandas 2.2.3, scikit-learn 1.6.1, scipy 1.15.1 y seaborn 0.13.2. Es recomendable asegurarse de tener pip actualizado antes de realizar la instalación, lo cual puedes hacer con el comando pip install --upgrade pip. Si surge algún problema de compatibilidad, verifica que la versión de Python instalada en tu sistema sea compatible con las versiones de las librerías que se van a instalar.

2. Abre el notebook `proyecto_final.ipynb` y ejecútalo en orden. El código incluye:

- Análisis exploratorio de los datos.
- Entrenamiento de los modelos (i) y (ii).
- Optimización de hiperparámetros para el modelo final.
- Evaluación de resultados y visualizaciones.
- Predicción sobre conjunto de test.

3. Para generar el archivo `predicciones_finales.csv`, asegúrate de tener dos arrays con las predicciones de los modelos:

Este es el código base empleado

```python
import pandas as pd

submission = pd.DataFrame({
    'Modelo_i': predicciones_modelo1,
    'Modelo_ii': predicciones_modelo2
})

submission.to_csv('predicciones_finales.csv', index=False)
```

El archivo generado debe tener este formato:

| Modelo_i | Modelo_ii |
|----------|-----------|
| 15.3     | 13.1      |
| 17.0     | 14.8      |
| ...      | ...       |