# 🛠️ Cómo agregar Anaconda al PATH manualmente en Windows
Cuando instalas Anaconda, puedes optar por **no agregarlo al PATH del sistema** (opción recomendada por Anaconda). Si no lo hiciste, entonces **no podrás usar `python` ni `conda` desde CMD o PowerShell**. Aquí tienes todos los pasos en un solo bloque para crear un archivo Markdown.

## Paso 1: Verifica si necesitas agregar Anaconda al PATH
Abre CMD o PowerShell y escribe:
```
conda --version
python --version
```
Si ves errores como:
```
'conda' is not recognized as an internal or external command...
```
Entonces **Anaconda no está en el PATH** y debes seguir los pasos siguientes.

## Paso 2: Encuentra la carpeta donde está instalado Anaconda
Por defecto, Anaconda se instala en:
```
C:\Users\TU_USUARIO\anaconda3
```
Vamos a agregar estas tres rutas al PATH:
```
C:\Users\TU_USUARIO\anaconda3
C:\Users\TU_USUARIO\anaconda3\Scripts
C:\Users\TU_USUARIO\anaconda3\Library\bin
```
_Reemplaza `TU_USUARIO` por tu nombre de usuario real (por ejemplo: `fredy`)._

## Paso 3: Agregar esas rutas al PATH del sistema
1. Abre el menú de **Inicio** y busca: `Editar las variables de entorno del sistema`
2. Haz clic en el botón **Variables de entorno**
3. En el panel inferior (**Variables del sistema**), selecciona la variable llamada `Path` y haz clic en **Editar`
4. En la ventana de edición, haz clic en **Nuevo** y agrega **las tres rutas** listadas arriba, una por línea:
   ```
   C:\Users\TU_USUARIO\anaconda3
   C:\Users\TU_USUARIO\anaconda3\Scripts
   C:\Users\TU_USUARIO\anaconda3\Library\bin
   ```
5. Haz clic en **Aceptar** en todas las ventanas abiertas para guardar los cambios

## Paso 4: Verificar que funciona
Cierra y vuelve a abrir CMD o PowerShell. Luego ejecuta:
```
conda --version
python --version
```
✅ Si todo está bien, verás algo como:
```
conda 24.3.0
Python 3.10.13
```

## Tip adicional: Usa Anaconda Prompt
Si no quieres modificar el PATH global, puedes usar la terminal especial que viene con Anaconda:
```
Inicio > Anaconda Prompt
```
Desde ahí puedes ejecutar `conda`, `python`, `jupyter`, etc., sin hacer cambios en tu configuración.

## Conclusión
Agregar Anaconda al PATH te permite usar Python y Conda desde cualquier terminal en Windows. Es útil si trabajas desde VS Code, PowerShell o CMD directamente.
