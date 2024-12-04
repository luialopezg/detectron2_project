# Detectron2 Project

Este proyecto utiliza [Detectron2](https://github.com/facebookresearch/detectron2), un framework de visión por computadora de código abierto desarrollado por Meta AI, para realizar la detección y segmentación de impactos en aeronaves. El objetivo principal es desarrollar un modelo que pueda identificar y estimar el área de impacto utilizando imágenes de referencia.

## Propósito del Proyecto

El propósito de este proyecto es implementar y personalizar **Detectron2** para segmentar áreas impactadas en aeronaves. Esto será útil para:
- Automatizar la identificación de daños en imágenes de aeronaves.
- Estimar el área afectada de manera precisa.
- Reducir el tiempo y los costos asociados al análisis manual.

Este proyecto forma parte del trabajo final de máster y está diseñado para ser un repositorio colaborativo con compañeros de estudio.

---

## Configuración del Entorno

### Requisitos Previos

1. **Sistema Operativo**: Se recomienda Linux (probado en Linux Mint).
2. **Python**: Versión 3.8 o superior.
3. **Dependencias principales**:
   - PyTorch
   - Detectron2
   - OpenCV

### Pasos para Configurar

1. Clonar este repositorio:
   ```bash
   git clone https://github.com/tu_usuario/detectron2_project.git
   cd detectron2_project

Crear un entorno virtual de Python:

python3 -m venv detectron2_env
source detectron2_env/bin/activate

Instalar PyTorch (con soporte para CUDA si tienes GPU):

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117

Instalar Detectron2:

pip install 'detectron2@git+https://github.com/facebookresearch/detectron2.git'

Instalar otras dependencias necesarias:

    pip install opencv-python-headless

Cómo Ejecutar el Modelo
1. Inferencia con un modelo preentrenado

El proyecto incluye un script para ejecutar inferencias sobre imágenes utilizando un modelo preentrenado en el dataset COCO. Las imágenes de entrada deben colocarse en la carpeta data/inputs/, y los resultados procesados se generarán en data/outputs/.

Para ejecutar el modelo, usa el siguiente comando:

python3 run_detectron2.py

2. Estructura del Script run_detectron2.py

El script:

    Carga un modelo preentrenado (Mask R-CNN con backbone ResNet-50).
    Procesa todas las imágenes en data/inputs/.
    Genera máscaras y bounding boxes en data/outputs/.

3. Personalización

Si deseas entrenar un modelo con tus propios datos, debes:

    Etiquetar las imágenes utilizando herramientas como LabelMe.
    Convertir las anotaciones al formato COCO.
    Registrar el dataset en Detectron2.

Estructura del Proyecto

detectron2_project/
├── configs/               # Configuraciones del modelo
├── data/                  # Datos de entrada y salida
│   ├── inputs/            # Imágenes de entrada
│   ├── outputs/           # Resultados procesados
├── scripts/               # Scripts adicionales
├── run_detectron2.py      # Script principal para inferencia
└── README.md              # Documentación del proyecto


Colaboración

Este repositorio es colaborativo. Si deseas contribuir:

    Crea una rama para tu trabajo:

git checkout -b nombre_de_rama

Realiza tus cambios y haz un commit:

git add .
git commit -m "Descripción de los cambios"

Sube tu rama:

    git push origin nombre_de_rama

    Crea un pull request en GitHub para que se revise y fusione tu trabajo.

Créditos

Este proyecto utiliza Detectron2, desarrollado por Meta AI. Para más información sobre Detectron2, visita su documentación oficial.


---

### Instrucciones
1. Crea un archivo llamado `README.md` en la raíz del proyecto.
2. Copia y pega el contenido proporcionado.
3. Realiza un commit y súbelo al repositorio:
   ```bash
   git add README.md
   git commit -m "Agregado README.md con documentación inicial"
   git push origin main
