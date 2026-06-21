# Práctica 1: Mundo del Wumpus

**Asignatura:** Sistemas Inteligentes (Curso 2024-2025)  
**Docente:** Pedro Latorre Carmona  
**Autor:** Arkaitz Díez González  

Este repositorio contiene la implementación del clásico problema del "Mundo del Wumpus", desarrollado como parte de la asignatura de Sistemas Inteligentes. El proyecto está programado en Python y estructurado a través de un cuaderno interactivo de Jupyter (Jupyter Notebook).

La principal característica de esta versión es la integración del algoritmo **Minimax con poda alfa-beta**. En esta simulación, la lógica se divide en dos enfoques: el agente (actuando como jugador MAX) evalúa los estados del tablero para sobrevivir y obtener el oro, mientras que el entorno (actuando como jugador MIN) incrementa la complejidad desplazando las cuevas de forma aleatoria.

## Ejecución interactiva en la nube

Para facilitar la evaluación y prueba del código sin necesidad de descargar el repositorio ni configurar un entorno local, el proyecto ha sido desplegado utilizando Binder. 

Puedes interactuar con el entorno completo y ejecutar las celdas directamente desde el navegador a través del siguiente enlace:

👉 **[Ejecutar simulación en Binder](https://mybinder.org/v2/gh/arkadigo04/Wumpus/main?urlpath=%2Fdoc%2Ftree%2Fpractica1Arkaitz.ipynb)**

*Aviso: Durante el primer inicio, el servidor de Binder puede demorar unos minutos mientras construye la imagen virtual e instala las dependencias (`requirements.txt`). Una vez cargado, el rendimiento será el habitual.*

## Estructura Técnica y Herramientas

El desarrollo se apoya en los siguientes pilares técnicos:

* **Motor Lógico**: Implementación del motor del juego para la validación de movimientos, detección de percepciones (brisa, hedor) y resolución de estados finales.
* **Toma de Decisiones**: Uso de Minimax (con poda alfa-beta para evitar la explosión combinatoria) evaluando el riesgo de las casillas contiguas. Se incluye una heurística de disparo aleatorio como último recurso en situaciones de bloqueo.
* **Interfaz Visual**: Sustitución de la clásica salida por consola de texto mediante un entorno gráfico generado con `matplotlib`, `numpy` y procesamiento de imágenes con `Pillow`.

## Despliegue en entorno local

Si prefieres realizar la ejecución en tu propia máquina en lugar de utilizar el entorno en la nube, sigue estos pasos:

1. Asegúrate de tener instalado Python y Jupyter Notebook.
2. Clona el repositorio en tu entorno local:

```bash
git clone [https://github.com/arkadigo04/Wumpus.git](https://github.com/arkadigo04/Wumpus.git)
cd Wumpus

```

3. Verifica que la carpeta de recursos gráficos (`casillas_imagenes`) se encuentre en el mismo directorio raíz que el archivo `practica1Arkaitz.ipynb`. Sin esta carpeta, la renderización visual del tablero fallará.
4. Inicia el cuaderno:

```bash
jupyter notebook practica1Arkaitz.ipynb

```
