# Detector de objetos personalizado para retail con YOLOV8 y DeepSort

**Universidad Nacional de Colombia**

**Realizado por:** Juan Andres Bueno

**Dirigido por:** Jorge Sofrony


Se entrena un modelo personalizado para la detección de un set de productos seleccionados, se usa YOLOV8, posteriormente se adapta un codigo para el empleado para el conteo de autos para nuestra aplicación especifica.

![Detecciones y conteo con el modelo entrenado](https://github.com/Juan-Good/Hatsu_YOLOv8/blob/main/images/hatsu.gif)

## Descripción

Se busca realizar un modelo de detección personalizada para entornos retail, para ello se capturan y generan distintos datasets para el entrenamiento de un modelo de detección de objetos. Se desea que el sistema sea capaz de identificar los objetos en un espacio definido y llevar el registro de los objetos entrando y saliendo de este espacio para asi automatizar el proceso de compra y mejorar la experiencia global del usuario, para tal fin se emplea Supervisión para el conteo de entradas y salidas definiendo una linea en la imagen  como frontera, asi mismo se usa DeepSort como rastreador.

## Características

- Detector de objetos personalizado utilizando YOLOV8.
- Uso de DeepSort para el rastreo de productos.
- Uso de LineCounter con modificaciones propias para el conteo de productos.

## Requisitos del Sistema

En esta sección, puedes listar los requisitos necesarios para ejecutar el proyecto. Esto puede incluir software, bibliotecas o hardware específicos. Por ejemplo:

- Python 3.9
- Anaconda Navigator
- YOLOV7
- Bytetrack
- Supervision
- Visual StudioCode

Sobre Software recomendado
- Procesador: 12th Gen Intel(R) Core(TM) i7-12700H   2.70 GHz.
- Ram: 16.0 GB.
- Tarjeta Gráfica NVIDIA GeForce RTX 3070 Ti GPU
- Memoria disponible 100 GB
- Webcam: 1920 x 1080 Pixeles FULL HD

## Instalación

En general se recomienda visitar: https://github.com/MuhammadMoinFaisal/YOLOv8-DeepSORT-Object-Tracking

## Uso

En el archivo comandosY8.txt encontrara los diferentes comandos para entrenamiento y uso, tienen el siguiente estilo

```
#Entrenamiento

python train.py workers=1 device=0 model=yolov8n.yaml data=Y8hatsu.yaml epochs=200 imgsz=640 name=Y8_Hatsu2
#Uso
python predict_count.py model=Y8hatsu1.pt source="control.mp4" show=True save=false name=prueba_control
```

Se recomienda fuertemente revisar la guia pertinente al trabajo realizado con YOLOV7, alli se abordan coceptos como el cambio en diferentes entradas de video y la creación de datasets

## Contacto

jbuenoh@unal.edu.co

## Créditos
Para mayor información se invita a revisar:

- Muhammad Moin (2023) Real-Time Object Tracking using YOLOv8 and DeepSORT | Vehicles Counting (Vehicles Entering & Leaving) Disponible en: https://www.youtube.com/watch?v=9jRRZ-WL698




