# Guía básica: Git en tu máquina local (sin GitHub)

## 🎯 Objetivo
Familiarizarte con Git como herramienta de control de versiones **local**, sin necesidad de conexión a GitHub.

---

## 🛠️ Paso 1: Instalar Git

### 🪟 En Windows (CMD o PowerShell)

```bash
winget install --id Git.Git -e --source winget
```

Si no tienes `winget`, descárgalo desde: https://git-scm.com

### 🍎 En MacOS (Terminal)

```bash
brew install git
```

### 🐧 En Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install git
```

### ✅ Verificar versión instalada

```bash
git --version
```

Esto debe devolver algo como: `git version 2.40.1`

---

## 🔧 Paso 2: Configurar Git

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tucorreo@example.com"
```

Verifica configuración:

```bash
git config --list
```

*Nota:* También puedes hacer esta configuración solo para un repositorio si no deseas que se aplique globalmente.

---

## 📂 Paso 3: Crear un repositorio local

```bash
mkdir proyecto-git
cd proyecto-git
git init
```

Esto inicializa Git en esa carpeta. Ahora es un repositorio.

---

## 📄 Paso 4: Crear archivos y hacer seguimiento

```bash
echo "print('Hola mundo')" > script.py
git status
```

Agregar archivo al "staging area":

```bash
git add script.py
```

Hacer un commit:

```bash
git commit -m "Primer commit: se agrega script.py"
```

---

## 🌱 Ramas en Git

### Crear una nueva rama:

```bash
git branch nueva-funcionalidad
```

### Cambiar de rama:

```bash
git checkout nueva-funcionalidad
```

Haz un cambio (por ejemplo, agrega un archivo):

```bash
echo "print('rama nueva')" > otro.py
git add otro.py
git commit -m "Se agrega otro.py en rama nueva"
```

### Volver a `main` y hacer merge:

```bash
git checkout main
git merge nueva-funcionalidad
```

---

## 🔁 Comandos comunes de Git local

| Comando                             | Qué hace                                               |
|-------------------------------------|--------------------------------------------------------|
| `git status`                        | Ver qué ha cambiado y qué está listo para commit       |
| `git add archivo`                   | Agrega archivo al staging                             |
| `git commit -m "mensaje"`           | Guarda los cambios con un mensaje                     |
| `git log`                           | Ver el historial de commits                           |
| `git diff`                          | Ver qué ha cambiado antes del commit                  |
| `git reset archivo`                 | Quita un archivo del staging                          |
| `git rm archivo`                    | Borra un archivo y lo registra en el commit           |
| `git mv archivo nuevo_nombre`       | Renombra y lo registra con Git                        |
| `git checkout nombre-rama`          | Cambia de rama                                        |
| `git branch nombre-rama`            | Crea una nueva rama                                   |
| `git merge nombre-rama`             | Fusiona una rama con la actual                        |

---

## 🧪 Buenas prácticas

- Haz commits con mensajes claros
- Usa `git status` frecuentemente
- No mezcles muchas cosas diferentes en un solo commit
- Usa ramas para experimentar o probar cambios

---

## 🧹 Eliminar un repositorio local (deshacer `git init`)

```bash
rm -rf .git        # Linux/Mac
rmdir /s /q .git   # Windows
```

Esto **borra el repositorio Git** (no tus archivos).

---

## 🔁 ¿Cómo volver a una versión anterior en Git?

Git guarda un historial completo de todos los cambios (commits), por lo tanto puedes volver a una versión anterior del proyecto en cualquier momento.

---

### ✅ Ver el historial de versiones

```bash
git log
```

Muestra todos los commits con su código (hash), autor y mensaje.

---

> ### 🧬 ¿Qué es el hash de un commit?

>Cada vez que haces un `git commit`, Git genera un **hash (ID único)** para identificar ese cambio.  
Este hash es una cadena de letras y números que puedes usar para referenciar esa versión exacta del proyecto.

---

> Verás algo como:

```
commit 3f2c4a8b9e0e1e58739c835a1ff14c18a5aeb9a1
Author: Estudiante <correo@ejemplo.com>
Date:   Tue Jun 6 10:45:00 2025 -0500

    Agrego archivo README.md
```

- El código que aparece después de `commit` es el **hash del commit**.
- Puedes usar solo los primeros 7-10 caracteres para referenciarlo:

```bash
git checkout 3f2c4a8
```

### 🔙 Volver temporalmente a una versión anterior

```bash
git checkout <hash-del-commit>
```

Esto te lleva a una versión anterior en modo solo lectura (detached HEAD).  
Ideal para revisar, **pero no trabajes ni hagas commits aquí directamente.**

---

### 🧹 Deshacer el último commit (manteniendo los cambios)

```bash
git reset --soft HEAD~1
```

Te permite editar y rehacer el último commit sin perder tus archivos.

---

### 🔥 Restaurar completamente a una versión anterior

```bash
git reset --hard <hash-del-commit>
```

⚠️ Esto elimina los commits posteriores al seleccionado.  
**No lo uses si no estás seguro.**

---

### 🧯 Recuperar un archivo de una versión pasada

```bash
git checkout <hash> -- archivo.py
```

Trae una versión antigua de un archivo sin afectar el resto del proyecto.

---

💡 **Recomendación:** para principiantes, usa `git log` y `git checkout <hash>` solo para explorar. Usa `reset` con precaución.


---

## 🧬 ¿Qué es el hash de un commit?

Cada vez que haces un `git commit`, Git genera un **hash (ID único)** para identificar ese cambio.  
Este hash es una cadena de letras y números que puedes usar para referenciar esa versión exacta del proyecto.

---

### 🔍 ¿Dónde se ve?

Usa:

```bash
git log
```

Verás algo como:

```
commit 3f2c4a8b9e0e1e58739c835a1ff14c18a5aeb9a1
Author: Estudiante <correo@ejemplo.com>
Date:   Tue Jun 6 10:45:00 2025 -0500

    Agrego archivo README.md
```

- El código que aparece después de `commit` es el **hash del commit**.
- Puedes usar solo los primeros 7-10 caracteres para referenciarlo:

```bash
git checkout 3f2c4a8
```

---

### ✅ ¿Para qué sirve?

- **Explorar** una versión anterior sin afectar tu trabajo actual.
- **Volver** todo el proyecto a ese estado con `reset`.
- **Recuperar** un archivo como estaba en ese momento:

```bash
git checkout 3f2c4a8 -- archivo.txt
```

---

💡 Git utiliza estos hashes para que puedas navegar en el tiempo de forma precisa y confiable.
