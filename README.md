# Laboratorio 4 – Minería de datos (ISW 911)

```
Laboratorio4_MineriaDatos/
├── lab4_IC2025.ipynb    ← TODO el laboratorio (este es el que se entrega)
├── datos/
│   └── recursos_contratacion_2022_2024.csv   ← dataset original (subir a GitHub)
├── data_process.csv     ← dataset final (lo genera el notebook al final)
└── README.md
```

---

## ¿Qué es un archivo `.ipynb`?

`.ipynb` significa **I**nteractive **Py**thon **N**ote**b**ook: es un **notebook de Jupyter**.
Es como un cuaderno que mezcla, en un solo archivo:

- **Texto explicativo** (títulos, párrafos, tablas)
- **Código Python** que se puede ejecutar
- **Los resultados** de ese código: tablas, números y **gráficos**

Por eso se usa tanto en ciencia de datos: el profesor ve en un mismo lugar *qué hiciste*,
*el código* y *el resultado*, sin tener que ejecutar nada.

### Está hecho de "celdas"

El notebook es una lista de bloques llamados **celdas**. Hay dos tipos:

| Tipo | Para qué sirve | Cómo se ve |
|------|----------------|------------|
| **Markdown** | Texto: títulos (`#`), negritas (`**texto**`), listas, tablas | Texto con formato |
| **Code** (código) | Código Python | Un recuadro con `[n]` a la izquierda y su resultado debajo |

El número `[n]` a la izquierda de una celda de código indica **en qué orden se ejecutó**.

### El "kernel"

El **kernel** es el programa de Python que ejecuta las celdas. Todas las celdas comparten la
misma memoria: si en una celda haces `df = pd.read_csv(...)`, la siguiente ya puede usar `df`.
Por eso **el orden importa**: hay que ejecutar las celdas de arriba hacia abajo.

### Por dentro es un JSON

Si abres el `.ipynb` con el Bloc de notas vas a ver texto en formato **JSON**: una lista de celdas,
cada una con su tipo, su código y sus salidas (los gráficos se guardan como imágenes dentro del
mismo archivo). **No se edita así**: se abre con un programa que lo muestra como cuaderno.

---

## Cómo abrirlo y ejecutarlo

**Opción A: VS Code** (ya lo tienes instalado)
1. Abre `lab4_IC2025.ipynb`. Si te lo pide, instala la extensión **Jupyter**.
2. Arriba a la derecha → **Select Kernel** → **Python 3.13**.
3. **Run All** ejecuta todo de arriba a abajo; o ejecuta una celda con **Shift + Enter**.
4. Para agregar una celda: botones **+ Code** o **+ Markdown**.

**Opción B: Google Colab** (en el navegador, sin instalar nada)
1. Entra a colab.research.google.com → **Subir** → elige `lab4_IC2025.ipynb`.
2. **Entorno de ejecución → Ejecutar todas**.
3. Como Colab lee el dataset desde GitHub, ahí primero tienes que poner la URL real (ver abajo).

**Opción C: Jupyter en la computadora**
```powershell
python -m pip install --user notebook
```
```powershell
python -m notebook
```
Se abre el navegador; entra a la carpeta y haz clic en el archivo.

---

## Cómo está organizado el laboratorio dentro del notebook

Cada sección empieza con una celda de texto que explica qué se hace y por qué, luego el código,
y al final una celda con los **hallazgos**.

| Sección | Punto del enunciado |
|---------|---------------------|
| Encabezado (integrantes, dataset) | 15 |
| 1. Librerías | 1 |
| 2. Lectura desde GitHub | 2‑3 |
| 3. Funciones básicas | 4 |
| 4. Columnas en español | 5 |
| 5. Valores nulos + gráficos | 6 |
| 6. Valores atípicos + gráficos | 7 |
| 7. Funciones de imputación | 8 |
| 8. Conversión de tipos | 9 |
| 9. Categóricas a numéricas | 10 |
| 10. Estandarización | 11 |
| 11. Correlación + gráficos | 12 |
| 12. Variable dependiente y modelo | 13 |
| 13. Guardar `data_process.csv` | 14 |

---

## Pendiente antes de entregar

1. Crear un repositorio **público** en GitHub y subir `datos/recursos_contratacion_2022_2024.csv`.
2. En GitHub, abrir el archivo → botón **Raw** → copiar la URL.
3. En el notebook, sección 2, pegar esa URL en `URL_GITHUB`
   (mientras no la pongas, el notebook usa la copia de la carpeta `datos/`).
4. En la primera celda, cambiar `[Nombre completo] – [Carné]` por tus datos
   (doble clic en la celda para editarla, Shift + Enter para terminar).
5. **Run All**, guardar (Ctrl + S) y subir `lab4_IC2025.ipynb` al campus virtual.
