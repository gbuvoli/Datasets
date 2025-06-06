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

¡Con esto ya puedes versionar y organizar tus proyectos localmente como un/a pro! 🎯
