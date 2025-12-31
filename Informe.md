#  Reto 1 –

**Diplomado Gestión de Datos 2025-2026**

##  ¿Qué hice en este reto?

En este reto desarrollé un script en Python llamado `ingestor.py` que simula una **etapa Bronze de un pipeline de datos**.  
La idea principal fue procesar archivos que llegan desde una carpeta de entrada (`landing/`), sabiendo que algunos pueden venir vacíos o dañados, y clasificarlos sin que el proceso se detenga por errores.

El objetivo fue automatizar la limpieza inicial de los datos y dejarlos listos para las siguientes etapas del pipeline.

---

##  ¿Cómo funciona el script?

El script realiza los siguientes pasos:

1. **Recorre la carpeta `landing/`**
   - Utiliza la librería `pathlib` para leer todos los archivos de forma segura.

2. **Valida cada archivo**
   - Si el archivo tiene contenido (más de 0 bytes), se considera válido.
   - Si el archivo está vacío, se considera corrupto o inválido.

3. **Clasifica los archivos**
   - Los archivos válidos se mueven a la carpeta `bronze/`.
   - Los archivos vacíos se mueven a la carpeta `bad_data/`.

4. **Muestra mensajes en consola**
   - Por cada archivo procesado, el script imprime qué archivo se movió y a qué carpeta, lo que permite hacer seguimiento del proceso.

5. **Manejo de errores**
   - Se implementó `try/except` para asegurar que, si ocurre un error con un archivo, el script continúe procesando los demás.

6. **Resultado final**
   - Al finalizar la ejecución, la carpeta `landing/` queda vacía, cumpliendo con el propósito del reto.

---

##  Tecnologías y librerías usadas

- Python 3
- `pathlib` para el manejo de rutas y archivos
- `shutil` para mover archivos entre carpetas
- Manejo de excepciones con `try/except`

---

##  Estructura del proyecto

```text
.
├── ingestor.py
├── landing/
├── bronze/
├── bad_data/
└── README.md
