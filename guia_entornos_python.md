# Guía Práctica - Entornos de desarrollo

## 🌟 Objetivo general
Guiar a los estudiantes en la exploración del entorno de programación Python usando Anaconda y Visual Studio Code, comprendiendo qué es un intérprete, cómo se ejecuta un script, y cómo se crean módulos y ambientes virtuales.

---

## Parte 1: Sistemas

### 🔹 Paso 1: Abrir Anaconda PowerShell Prompt

> Para realizar esta guía, se requiere tener instalada la distribución Anaconda y VS Code

En la barra de búsqueda de windows, escribe Anaconda Powershell Prompt y accede a el

> Anaconda instala una versión de Python + muchas librerías científicas.

### Paso 2: Verificar instalación de Python

```
python --version
```

Resultado esperado:

```
Python 3.9.x
```

Si da error, verificar si Anaconda está bien instalado o usar `where python` para buscar la ubicación.

---

## 🔹 Parte 2: Explorar el intérprete de Python

### ¿Qué es el intérprete?
> Programa que ejecuta código línea por línea. Es útil para hacer pruebas rápidas y entender el comportamiento de Python.

### Ingresar al intérprete:
```bash
python
```

### Probar comandos simples:
```python
print("Hola mundo")
2 + 3
nombre = "Sofía"
nombre.upper()
import math
math.sqrt(25)
```

### Salir del intérprete:
```python
exit()
```

---

## 🔹 Parte 3: Crear carpeta del proyecto desde Anaconda PowerShell

### ✅ Crear directorio:
```bash
mkdir sprint7B
cd sprint7B
```

### Abrir VS Code desde la carpeta actual:
```bash
code .
```

---

## 🔹 Parte 4: Abrir el proyecto en VS Code

### ✅ ¿Qué es VS Code?
> Un editor de código muy usado por programadores, liviano y flexible.


### ▶️ Crear archivo `hola.py`:

```python
print("¡Mi primer script en Python desde VS Code!")
```

### ▶️ Ejecutar desde terminal integrada en VS Code:
```bash
python hola.py
```

---

## 🔹 Parte 5: Crear un módulo propio

### ▶️ Crear archivo `operaciones.py`:
```python
def saludar(nombre):
    return f"Hola, {nombre}, bienvenido a Python"
```

### ▶️ Crear archivo `main.py`:
```python
from operaciones import saludar

nombre = input("¿Cómo te llamas? ")
print(saludar(nombre))
```

### ▶️ Ejecutar:
```bash
python main.py
```

---

## 🔹 Parte 6: Crear un ambiente virtual con Conda

### ▶️ Crear y activar entorno:
```bash
conda create --name entorno_clase python=3.11
conda activate entorno_clase
```

### ▶️ Verificar instalación:
```bash
python --version
```

---

## 🔹 Parte 7: Instalar y probar un paquete

### ▶️ Instalar `streamlit` y `plotly`:
```bash
conda install plotly
conda install streamlit
```

### ▶️ Crear archivo `app.py`:
```python
import plotly.express as px
import streamlit as st

# Título de la app
st.title("Visualización simple con Plotly")

# Datos de ejemplo
data = {
    "Frutas": ["Manzana", "Banana", "Naranja", "Fresa"],
    "Cantidad": [10, 15, 7, 12]
}

# Crear gráfico de barras
fig = px.bar(data, x="Frutas", y="Cantidad", title="Consumo de frutas")

# Mostrar gráfico en Streamlit
st.plotly_chart(fig)
```

### Ejecutar:
```bash
streamlit run app.py
```

---

## 🔹 Parte 8: Abrir Jupyter Notebook desde comandos

### ▶️ Desde un entorno activo:
```bash
conda activate entorno_clase
jupyter notebook
```

Esto abrirá Jupyter en el navegador. Puedes crear un nuevo notebook desde allí.

➡️ Para cerrar el servidor, regresa a la terminal y presiona `Ctrl + C`.

---

## 🚪 Cierre de clase

### 🧰 Reflexión:
- ¿Qué aprendiste sobre el intérprete?
- ¿Qué diferencia hay entre un script y un módulo?
- ¿Qué ventajas tiene usar un entorno virtual?
- ¿Te resultó intuitivo usar VS Code y Jupyter?

---
