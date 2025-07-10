# Guía de práctica CLI: Primeros pasos en la línea de comandos

## 🎯 Objetivo
Aprender a navegar por carpetas, crear archivos, visualizar su contenido y manipularlos usando comandos de terminal.

---

## 🧩 ¿Cómo abrir las terminales?

### 🪟 Windows
- **PowerShell:** Presiona `Win + X` y selecciona Terminal
- **CMD:** Presiona `Win + R`, escribe `cmd` y presiona Enter

  
> **Activar subsistema LINUX**: Ingresa a alguna de las terminales y escribe `wsl`


### 🍎 macOS
- Presiona `Cmd + Espacio`, escribe `Terminal` y presiona Enter

### 🐧 Linux
- Presiona `Ctrl + Alt + T` o busca "Terminal" en el menú

---

## 🛠️ Actividad guiada

### 1️⃣ Ver en qué carpeta estás

```bash

pwd # En Windows / Mac/Linux

```

### 2️⃣ Listar archivos y carpetas

```bash
# En Windows
dir
ls

# En Mac/Linux
ls
```

### 3️⃣ Crear una carpeta

```bash
mkdir practica-cli
```

### 4️⃣ Entrar a una carpeta

```bash
cd practica-cli
```

### 5️⃣ Moverse a un directorio usando ruta completa

```bash
cd C:/Users/TuUsuario/Documentos/proyecto
```

### 6️⃣ Limpiar la pantalla de la terminal

```bash

cls # En Windows
clear # En Mac/Linux /Windows
```

---

## 🧪 Comandos para trabajar con archivos

### 🆕 Crear un archivo vacío

```bash
# En windows
"" > nuevo.txt
```

### 📝 Crear archivo con contenido y salto de línea

```bash
echo "Línea 1\nLínea 2" > multilinea.txt
```

### 📄 Ver contenido del archivo

```bash
type archivo.txt        # Windows
cat archivo.txt         # Linux/Mac/Windows
```

### ➕ Agregar texto a un archivo existente

```bash
echo "Nueva línea" >> archivo.txt
```
> Cuidado con reemplazar el archivo existente! Utilizar `>` es diferente a `>>`
---

## ✏️ Copiar, mover y renombrar archivos

### 📂 Copiar archivo

```bash
# Copiar archivo.txt a copia.txt
copy archivo.txt copia.txt        # Windows
cp archivo.txt copia.txt          # Linux/Mac
```

## 🧭 Detalle: ¿Cómo funciona `move` / `mv` para mover y renombrar?

### 📦 Sintaxis general

```bash
move origen destino     # En Windows
mv origen destino       # En Linux/Mac
```

---

### ✅ Para mover un archivo a otra carpeta (sin cambiar el nombre)

```bash
move archivo.txt carpeta/         # Windows
mv archivo.txt carpeta/           # Linux/Mac
```
Esto mueve `archivo.txt` a la carpeta `carpeta`.

---

### ✅ Para renombrar un archivo (sin moverlo)

```bash
move archivo.txt nuevo_nombre.txt   # Windows
mv archivo.txt nuevo_nombre.txt     # Linux/Mac
```
Esto renombra `archivo.txt` como `nuevo_nombre.txt` en la misma ubicación.

---

### ✅ Para mover y renombrar al mismo tiempo

```bash
move archivo.txt carpeta/nuevo.txt    # Windows
mv archivo.txt carpeta/nuevo.txt      # Linux/Mac
```
Esto mueve el archivo a una carpeta y al mismo tiempo le cambia el nombre.


---

## 🧠 Trucos útiles

### ⬆️ Repetir comandos anteriores

- Usa la **flecha hacia arriba** (`↑`) para navegar por tu historial de comandos.
- Usa la flecha hacia abajo (`↓`) para ir hacia comandos más recientes.

### 🔁 Autocompletado

- Escribe parte del nombre y presiona **Tab** para autocompletar nombres de carpetas o archivos.
- Si hay varias coincidencias, presiona **Tab** dos veces para ver las opciones disponibles.

---

¡Explora, equivócate y aprende usando solo la terminal! 💻✨

---

## 📌 Resumen de comandos y su uso

| Comando                            | Uso                                                                 |
|-----------------------------------|----------------------------------------------------------------------|
| `cd`                              | Cambiar de directorio                                               |
| `pwd`                             | Mostrar la ruta actual (Mac/Linux)                                  |
| `dir`                             | Listar archivos y carpetas (Windows)                                |
| `ls`                              | Listar archivos y carpetas (Mac/Linux)                              |
| `mkdir nombre`                    | Crear una carpeta nueva                                             |
| `echo "texto" > archivo.txt`      | Crear archivo con contenido                                         |
| `echo "texto" >> archivo.txt`     | Agregar contenido a un archivo existente                            |
| `echo -e "L1\nL2" > archivo.txt` | Escribir múltiples líneas con salto de línea (Linux/Mac)            |
| `type archivo.txt`                | Ver contenido de archivo (Windows)                                  |
| `cat archivo.txt`                | Ver contenido de archivo (Linux/Mac)                                |
| `copy archivo.txt copia.txt`     | Copiar archivo (Windows)                                            |
| `cp archivo.txt copia.txt`       | Copiar archivo (Linux/Mac)                                          |
| `move archivo.txt nuevo.txt`     | Mover o renombrar archivo (Windows)                                 |
| `mv archivo.txt nuevo.txt`       | Mover o renombrar archivo (Linux/Mac)                               |
| `cls`                             | Limpiar pantalla (Windows)                                          |
| `clear`                           | Limpiar pantalla (Linux/Mac)                                        |
| `↑ / ↓`                           | Repetir comandos anteriores con flechas del teclado                 |
| `Tab`                             | Autocompletar nombres de archivos o carpetas                        |



