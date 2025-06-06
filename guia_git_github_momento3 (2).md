# 🧭 Tercer Momento – Conectando Git con GitHub

## 🎯 Objetivo
Poner en práctica un flujo completo de versionamiento con Git y GitHub, trabajando con un repositorio remoto.

---

## ✅ PASO 1: Crear cuenta en GitHub

1. Ir a [https://github.com/](https://github.com/)
2. Registrarse con nombre, correo y contraseña
3. Confirmar correo electrónico
4. (Opcional) Agregar una foto y bio en el perfil

---

## ✅ PASO 2: Crear un repositorio nuevo en GitHub

1. Clic en el botón verde **"New"** o ir a: [https://github.com/new](https://github.com/new)
2. Nombre sugerido: `mi-primer-repo`
3. Opciones:
   - NO seleccionar "Initialize with README"
   - Visibilidad: Pública o Privada
4. Clic en **“Create repository”**

---

## ✅ PASO 3: Clonar el repositorio en tu computador

1. Copia la URL HTTPS del repositorio, por ejemplo:  
   `https://github.com/usuario/mi-primer-repo.git`
2. Abre tu terminal y ubícate en la carpeta donde quieres clonar el proyecto
3. Ejecuta:

```bash
git clone https://github.com/usuario/mi-primer-repo.git
cd mi-primer-repo
```

---

## ✅ PASO 4: Crear archivos y hacer seguimiento

```bash
echo "# Bienvenidos a mi repositorio" > README.md
git status
git add README.md
git commit -m "Agrego archivo README.md"
```

---

## ✅ PASO 5: Subir cambios a GitHub

```bash
git push origin main
```

> Si es tu primer push, Git puede pedir autenticación. Usa tu usuario y token de GitHub.

---

## ✅ PASO 6: Verifica en GitHub

- Ingresa a tu repositorio desde el navegador
- Verifica que el archivo `README.md` aparezca

---

## 🌿 Bonus: Crear una nueva rama y subirla

```bash
git checkout -b mejora-readme
echo "Mi nombre es..." >> README.md
git add README.md
git commit -m "Agrego presentación personal"
git push origin mejora-readme
```

Puedes hacer una Pull Request desde GitHub para unir esta rama a `main`.

---

¡Ahora sí! Ya sabes trabajar con Git y GitHub en conjunto. 🚀


---

## 📌 Resumen de comandos más utilizados en Git + GitHub

| Comando                                  | Qué hace                                                      |
|------------------------------------------|---------------------------------------------------------------|
| `git init`                               | Inicializa un repositorio Git local                           |
| `git clone URL`                          | Clona un repositorio remoto en tu máquina                     |
| `git status`                             | Muestra el estado actual de los archivos                      |
| `git add archivo`                        | Agrega archivo(s) al área de preparación (staging)            |
| `git commit -m "mensaje"`                | Crea un commit con los cambios registrados                    |
| `git log`                                | Muestra el historial de commits                               |
| `git diff`                               | Muestra diferencias entre archivos modificados                |
| `git branch`                             | Lista las ramas existentes                                    |
| `git branch nombre-rama`                 | Crea una nueva rama                                           |
| `git checkout nombre-rama`              | Cambia a otra rama                                            |
| `git merge nombre-rama`                  | Fusiona una rama con la rama actual                          |
| `git push origin rama`                   | Envía los cambios locales al repositorio remoto               |
| `git pull origin rama`                   | Trae los últimos cambios del repositorio remoto               |
| `git remote -v`                           | Muestra las URLs del repositorio remoto                       |
| `git config --global user.name`          | Configura el nombre de usuario global                         |
| `git config --global user.email`         | Configura el correo de usuario global                         |

---

✅ Con estos comandos ya puedes trabajar con Git y GitHub como un profesional.



---

## 🤝 Trabajo colaborativo: Pull Requests y cambios en equipo

### 🎯 Objetivo
Aprender cómo colaborar en un repositorio de otra persona (por ejemplo, el de tu instructora), proponer cambios y que estos sean revisados antes de integrarse.

---

## ✅ PASO ADICIONAL: Contribuir a un repositorio existente

1. Ve al repositorio compartido por tu tutora (por ejemplo: `https://github.com/gbuvoli/mi_repo_test.git`)
2. Haz clic en **"Fork"** (arriba a la derecha) para crear una copia en tu cuenta
3. Clona tu fork en tu computador:

```bash
git clone https://github.com/tu_usuario/repo-ejemplo.git
cd repo-ejemplo
```

4. Crea una rama para tu aporte:

```bash
git checkout -b mi-contribucion
```

5. Realiza cambios, por ejemplo:

```bash
echo "estudiante: Tu Nombre" >> estudiantes.md
git add estudiantes.md
git commit -m "Agrego mi nombre a la lista de estudiantes"
git push origin mi-contribucion
```

6. Ve a tu repositorio en GitHub y haz clic en **"Compare & Pull Request"**
7. Escribe un mensaje claro explicando tu cambio
8. Haz clic en **"Create pull request"**

---

✅ Tu instructora podrá revisar el cambio y aceptarlo (mergearlo) si todo está bien. Así funciona el trabajo colaborativo en proyectos reales de código abierto.

