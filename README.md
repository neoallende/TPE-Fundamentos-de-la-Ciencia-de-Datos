# TPE – Fundamentos de la Ciencia de Datos (2026)

Trabajo Práctico Especial: análisis del conjunto de datos **CKD-NHANES** sobre enfermedad renal crónica (CKD), a partir de datos de la encuesta poblacional de salud y nutrición NHANES de Estados Unidos (ciclo 2021-2023).

## Integrantes (Grupo 33)

- Allende, Neo
- Maiarú, Francisco
- Lara Lambrecht, Manuel

## Contenido del repositorio

```
.
├── README.md                    # Este archivo
├── requirements.txt             # Dependencias de Python (pip)
├── Informe.docx                 # Informe con hallazgos y conclusiones
├── TPE_Ciencia_de_Datos.ipynb   # Notebook de Jupyter con todo el análisis (solo código)
├── dataset.csv                  # Conjunto de datos CKD-NHANES
├── metadata.docx                # Documentación de las variables del conjunto de datos
└── .gitignore
```

## Qué hace el trabajo

La notebook implementa, organizada en secciones, los requerimientos del enunciado:

1. Análisis exploratorio inicial de los datos (origen, atributos, distribuciones, outliers y valores nulos).
2. Limpieza de la base, con la justificación de cada acción.
3. Planteo de tres hipótesis propias (univariada, bivariada y multivariada).
4. Validación de las tres hipótesis propias y de las tres provistas por la cátedra.

El informe sigue la misma estructura que la notebook y referencia explícitamente las secciones en las que se realiza cada cálculo.

## Requisitos previos

- **Python 3.12**.
- `pip` y `venv` (incluidos en las instalaciones estándar de Python).
- Jupyter (se instala con `requirements.txt`).

## Instrucciones de ejecución

### 1. Clonar el repositorio

```bash
git clone https://github.com/neouuuu/TPE-Fundamentos-de-la-Ciencia-de-Datos.git
cd TPE-Fundamentos-de-la-Ciencia-de-Datos
```

### 2. Crear y activar un entorno virtual

Linux / macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows (PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Windows (cmd):

```bat
python -m venv .venv
.venv\Scripts\activate.bat
```

### 3. Instalar las dependencias

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Verificar que el archivo de datos esté en su lugar

El archivo de datos (`dataset.csv`) se incluye en la raíz del repositorio. La notebook lo lee mediante una ruta **relativa**, por lo que debe ejecutarse desde la raíz del repositorio y no hace falta modificar ninguna ruta.

### 5. Abrir y ejecutar la notebook

```bash
jupyter notebook TPE_Ciencia_de_Datos.ipynb
```

(o `jupyter lab TPE_Ciencia_de_Datos.ipynb`). Una vez abierta, ejecutar todas las celdas en orden con **Kernel → Restart & Run All**. La notebook corre de principio a fin sin errores ni intervención manual.

Alternativa por línea de comandos, sin abrir la interfaz:

```bash
jupyter nbconvert --to notebook --execute TPE_Ciencia_de_Datos.ipynb --output TPE_Ciencia_de_Datos_ejecutada.ipynb
```

## Estructura de la notebook

Las secciones de la notebook se corresponden con las del informe (Tabla 1 del informe):

| Sección del informe | Contenido | Sección de la notebook |
| ------------------- | --------- | ---------------------- |
| 2.1 | Exploración inicial y caracterización de atributos | 0 (configuración) y 1.1 a 1.3 |
| 2.2 | Distribución de variables y outliers | 1.4 a 1.6 |
| 2.3 | Limpieza de la base | 2 y 2.1 |
| 3.1 | Hipótesis 1 (univariada): proporción de adultos con ACR elevada | 3.1 |
| 3.2 | Hipótesis 2 (bivariada): BMI según diabetes diagnosticada | 3.2 |
| 3.3 | Hipótesis 3 (multivariada): parámetros bioquímicos y eGFR | 3.3 |
| 3.4 | Hipótesis 4 (cátedra): casos de CKD según grupo étnico | 3.4 |
| 3.5 | Hipótesis 5 (cátedra): presión arterial y presencia de CKD | 3.5 |
| 3.6 | Hipótesis 6 (cátedra): edad, sexo, BMI, presión arterial, diabetes, tabaquismo y nivel socioeconómico con CKD | 3.6 |
