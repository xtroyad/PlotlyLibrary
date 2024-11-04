# 📚 Material Didáctico para Aprender Plotly
![alt text](img/logo.png)
## 🌟 Introducción

¡Bienvenido a este proyecto de aprendizaje sobre **Plotly**! Este material didáctico está diseñado para ayudarte a comprender y utilizar esta poderosa biblioteca de visualización de datos en Python. A través de una serie de notebooks de Jupyter, aprenderás a crear visualizaciones interactivas y personalizadas, además de explorar diversas funcionalidades que ofrece Plotly.

### 🎯 Objetivos del Proyecto

- Proporcionar una introducción clara y concisa a la biblioteca Plotly.
- Explicar cómo instalar y configurar el entorno de trabajo.
- Presentar ejemplos prácticos y ejercicios para afianzar el aprendizaje.

<img src="img/anima.gif" alt="Descripción de la animación" style="width: 80%; height: auto;">

## 🛠️ a. Guía de Instalación

Para comenzar a trabajar con Plotly, sigue estos pasos para configurar tu entorno:

### 📋 Requisitos Previos

- Asegúrate de tener **Python 3.10** o superior instalado en tu sistema.
- Se recomienda utilizar un entorno virtual (como `venv` o `conda`) para evitar conflictos de dependencias.

### 🔧 Instalación de Dependencias

1. **Crea un entorno virtual** (opcional, pero recomendado):
   ```bash
   python -m venv myenv
   source myenv/bin/activate  # En Linux y Mac
   myenv\Scripts\activate  # En Windows

   
2. **Crea un entorno virtual usando Conda** (opcional 2):
   ```bash
   conda create -n myenv python=3.10
   conda activate myenv
3. **Instalación de dependencias**
    ```bash
    pip install -r requirements.txt
##  🛠️ b. Alternativa. Proyecto con Docker

Esta sección describe cómo configurar y ejecutar el proyecto utilizando una imagen de Docker almacenada en Docker Hub. Esta alternativa permite trabajar en un entorno controlado sin necesidad de configurar manualmente las dependencias en tu sistema.

### 📋 Prerrequisitos

1. Tener Docker y Docker Compose instalados. Si no los tienes, sigue las instrucciones en la [página oficial de Docker](https://docs.docker.com/get-docker/).

### 🚀 Pasos para instalar y ejecutar el proyecto con Docker

1. Verificar el archivo `docker-compose.yml`

    El archivo `docker-compose.yml` en este repositorio está configurado para descargar la imagen desde Docker Hub y ejecutar el contenedor de Jupyter Notebook en el puerto 8888. Asegúrate de que contiene la siguiente configuración:

    ```yaml
    services:
    jupyter:
        image: xtroyad/plotly_lib:latest
        ports:
        - "8888:8888"
        volumes:
        - ./:/app
        environment:
        - JUPYTER_ENABLE_LAB=yes
    ```

2. Ejecutar Docker Compose

    Para iniciar el servicio de Jupyter Notebook, ejecuta el siguiente comando en el directorio raíz del proyecto (donde se encuentra `docker-compose.yml`):
    ```bash
    docker compose up
    ```

3. Acceso a Jupyter Notebook

    Una vez que el contenedor esté ejecutándose, verás una URL en la terminal con un token de autenticación. Abre esa URL en un navegador para acceder a Jupyter Notebook.

    Algo parecido a lo siguiente pero con un token:
    http://127.0.0.1:8888/lab?token=

    Los herrores adicionales que puedan salir ignórelos. Salen al crear por primera vez el contenedor😊.
