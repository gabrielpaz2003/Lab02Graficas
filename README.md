# LAB02GRAFICAS

Este proyecto es una implementación de un renderizador de gráficos simple en Python utilizando PyGame para la visualización. El proyecto incluye varios módulos para manejar modelos 3D, shaders y operaciones matemáticas necesarias para las transformaciones y la representación de los objetos.

## Contenido del Proyecto

- `gl.py`: Contiene funciones y clases para el renderizado de gráficos, como la clase `Renderer` y funciones auxiliares para manejar datos binarios.
- `lab2.py`: El script principal que inicializa la ventana de PyGame, carga el modelo 3D y ejecuta el bucle principal de renderizado.
- `mathlib.py`: Contiene funciones para operaciones matemáticas necesarias, como productos de matrices y vectores, y matrices de transformación.
- `modelo.py`: Define la clase `Model` para manejar los modelos 3D, incluyendo sus vértices y caras.
- `obj.py`: Define la clase `Obj` para leer y parsear archivos .obj.
- `output.bmp`: Archivo de salida de ejemplo generado por el renderizador.
- `README.md`: Este archivo, proporciona una descripción general del proyecto y cómo utilizarlo.
- `shaders.py`: Archivo donde se pueden definir los shaders para la manipulación de vértices.



LAB02GRAFICAS/
│
├── gl.py
│   ├── char(c)
│   ├── word(w)
│   ├── dword(d)
│   ├── Renderer
│   │   ├── __init__(self, screen)
│   │   ├── glColor(self, r, g, b)
│   │   ├── glClearColor(self, r, g, b)
│   │   ├── glClear(self)
│   │   ├── glPoint(self, x, y, color=None)
│   │   ├── glLine(self, v0, v1, color=None)
│   │   ├── glPoligono(self, listadoPuntos)
│   │   ├── glFill(self, points)
│   │   ├── glGenerateFrameBuffer(self, filename)
│   │   ├── glRender(self)
│   │   └── glDrawPrimitives(self, buffer)
│
├── lab2.py
│   ├── Inicializa PyGame
│   ├── Crea una instancia de Renderer
│   ├── Carga un modelo 3D (Model)
│   ├── Bucle principal de renderizado y manejo de eventos
│
├── mathlib.py
│   ├── MatrixProduct(A, B)
│   ├── MatrixVectorProduct(A, v)
│   ├── TranslationMatrix(x, y, z)
│   ├── ScaleMatrix(x, y, z)
│   └── RotateMatrix(pitch, yaw, roll)
│
├── modelo.py
│   ├── Model
│   │   ├── __init__(self, filename)
│   │   ├── GetModelMatrix(self)
│
├── obj.py
│   ├── Obj
│   │   ├── __init__(self, filename)
│   │   ├── vertices
│   │   ├── texcoords
│   │   ├── normals
│   │   └── faces
│
├── shaders.py
│   └── Archivo para definir shaders (vacio en el ejemplo)
│
├── output.bmp
│   └── Archivo de salida generado por el renderizador
│
└── README.md
    └── Descripción general del proyecto y guía de uso


## Requisitos

- Python 3.x
- PyGame

## Instalación

1. Clona el repositorio:

git clone https://github.com/gabrielpaz2003/Lab02Graficas.git
cd LAB02GRAFICAS

2. Crea un entorno virtual (opcional pero recomendado):
python -m venv .venv
source .venv/bin/activate  # En Windows: .venv\Scripts\activate

3. Instala las dependencias:
pip install pygame


## Uso

python lab2.py

## Controles

ESC: Salir del programa.
Flecha Derecha: Rotar el modelo hacia la derecha.
Flecha Izquierda: Rotar el modelo hacia la izquierda.
1: Cambiar el modo de renderizado a puntos.
2: Cambiar el modo de renderizado a líneas.

## Autor

Gabriel Alberto Paz Gonzalez - 221087



