# Reconocimiento-de-caracteres-y-digitos

implementa un sistema de **reconocimiento de dígitos escritos a mano** usando **Deep Learning** y permite predecir números en **tiempo real con la cámara**.


## Objetivo del código

El programa entrena una **red neuronal convolucional (CNN)** para reconocer dígitos del **0 al 9** usando el dataset **MNIST**, y luego usa la cámara del computador para detectar y predecir números dibujados o escritos frente al lente.

En pocas palabras:
✔ Aprende a reconocer números
✔ Evalúa su precisión
✔ Predice números en vivo con la cámara

---


### Librerías y configuración

Se importan librerías necesarias:

* **PyTorch** → construir y entrenar la red neuronal
* **OpenCV** → capturar video de la cámara
* NumPy y Matplotlib → procesamiento y visualización

También se configura si se usará CPU o GPU.

---

### Carga del dataset MNIST

Se descarga y prepara el dataset MNIST:

* Imágenes de dígitos en escala de grises (28×28 px)
* Normalización de datos
* Creación de **DataLoaders** para entrenamiento y validación

Esto permite alimentar los datos al modelo.

---

### Definición del modelo CNN

Se crea una red neuronal convolucional:

**Arquitectura:**

* Capa convolucional (detecta bordes y formas)
* ReLU (activación)
* MaxPooling (reduce dimensiones)
* Segunda convolución
* Dropout (evita sobreajuste)
* Capas densas (clasificación final)

El modelo aprende patrones de los números.

---

### Configuración de entrenamiento

Se define:

* Función de pérdida: `CrossEntropyLoss`
* Optimizador: Adam
* Scheduler (ajusta el learning rate)
* Early stopping (detiene entrenamiento si no mejora)

Esto optimiza el aprendizaje.

---

### Entrenamiento y validación

El modelo se entrena por varias épocas:

* Calcula pérdida (loss)
* Calcula precisión (accuracy)
* Guarda el mejor modelo

Aquí el sistema aprende a reconocer los dígitos.

---

### Evaluación del modelo

Se prueba el modelo con datos de test:

* Métricas de rendimiento
* Matriz de confusión
* Visualización de resultados

Permite ver qué tan bien reconoce los números.

---

### Preprocesamiento para la cámara

Se prepara la imagen capturada:

1. Conversión a escala de grises
2. Filtrado y umbralización
3. Inversión de colores
4. Redimensionamiento a 28×28
5. Normalización

Convierte la imagen real al formato que el modelo entiende.

---

### Predicción en tiempo real con cámara

Usando OpenCV:

* Se abre la cámara
* Se muestra un recuadro (ROI)
* Al presionar una tecla se captura el dígito
* El modelo predice el número

Puedes escribir un número en papel y el sistema lo reconoce.

---

## ¿Para qué sirve este código?

- Aprender visión por computadora
- Comprender redes convolucionales (CNN)
- Reconocimiento de dígitos escritos a mano
- Proyectos de IA en tiempo real
- Base para OCR (reconocimiento óptico de caracteres)

<img width="980" height="701" alt="image" src="https://github.com/user-attachments/assets/6672d526-5783-4bee-a87b-dbc8770deea5" />


