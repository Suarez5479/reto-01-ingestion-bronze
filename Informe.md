#  Reto 1

**Diplomado Gestión de Datos 2026**

---

##  Contexto

En este reto se simula una etapa de ingestión de datos dentro de un pipeline.  
Se cuenta con una carpeta llamada `landing/` donde llegan archivos desde diferentes fuentes, pero debido a problemas en la transmisión algunos de estos archivos pueden llegar vacíos o corruptos.

El objetivo es procesar estos archivos automáticamente, separar los datos útiles de los inválidos y evitar que el proceso se detenga por errores individuales.

---

##  Objetivo del Reto

Desarrollar un script en Python que:

- Recorra todos los archivos dentro de la carpeta `landing/`
- Clasifique los archivos según su contenido
- Mueva los archivos válidos a `bronze/`
- Mueva los archivos vacíos a `bad_data/`
- Registre en consola qué ocurrió con cada archivo
- No se detenga si ocurre un error con algún archivo

---

##  Tecnologías utilizadas

- Python 3
- `pathlib` para el manejo de rutas
- `shutil` para mover archivos dentro del sistema

---

##  Estructura del proyecto

```text
reto-01-ingestion-bronze/
├── ingestor.py
├── bronze/
├── bad_data/
├── landing/
└── README.md

