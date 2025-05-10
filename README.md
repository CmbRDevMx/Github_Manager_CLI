# 🛠️ GitHub Manager CLI Tools for Termux

Herramientas en Python diseñadas para gestionar tu cuenta de GitHub directamente desde Termux, usando autenticación persistente, consola interactiva y logging detallado. Ideal para desarrolladores móviles, automatización o administración rápida de cuentas.

## ✅ Herramientas actuales

### `repos.py` - Gestor de repositorios
- Autenticación segura con token personal.
- Lista todos los repositorios (públicos, privados y forks).
- Permite cambiar la visibilidad de repos (privado ↔ público).
- Interfaz colorida y clara desde la terminal.
- Guarda logs y credenciales de forma segura.

### `forks.py` - Gestor de forks
- Detecta automáticamente todos tus forks.
- Permite eliminar forks de forma masiva o selectiva.
- Usa las mismas credenciales guardadas.
- Registro de acciones en el mismo archivo de logs.
Aquí tienes la **guía adaptada para el CLI de GitHub Manager (`.gh-bins`)** en lugar de `.woff2`, manteniendo el mismo estilo claro y profesional:

---

# Github Manager CLI

Script para Termux: Configura binarios personalizados con un PATH exclusivo

### 🚀 Guía Rápida: Configurar `.gh-bins` en Termux

---

1. **Instala `curl`** (si no lo tienes; en versiones recientes de Termux ya viene por defecto):

   ```bash
   pkg install curl -y
   ```

2. **Ejecuta el instalador en un solo paso**:

   ```bash
   curl -sL https://raw.githubusercontent.com/CmbRDevMx/Github_Manager_CLI/main/gh-setup.sh | bash
   ```

3. **Reinicia Termux o aplica los cambios al shell**:

   * Para Bash:

     ```bash
     source ~/.bashrc
     ```

   * Para Zsh:

     ```bash
     source ~/.zshrc
     ```

4. ✅ ¡Listo! Ahora puedes ejecutar los binarios del CLI de GitHub Manager directamente desde cualquier ubicación.

---

## 🛠 Solución de problemas:

* Si los comandos no funcionan, asegúrate de que los binarios tengan permisos de ejecución:

  ```bash
  chmod +x ~/.gh-bins/*
  ```

* Luego **cierra y vuelve a abrir Termux**, o aplica los cambios manualmente como se indica arriba.

* 🔁 **¿Quieres actualizar?**
  Solo vuelve a ejecutar el instalador del paso 2, y tendrás la última versión.

---


## 🧭 Uso

Asegúrate de tener Python y Termux instalados. Luego:

```bash
repos  # Para gestionar visibilidad de repositorios
forks   # Para eliminar forks
````

## 🔒 Seguridad

Las credenciales se almacenan en `~/.github_manager/config.json` con permisos restringidos. El archivo de logs se guarda en `~/github_manager.log`.

---

## 🧪 Funcionalidades futuras (en desarrollo)

Estas herramientas están planeadas y se irán liberando progresivamente:

| Herramienta              | Funcionalidad principal                                      |
| ------------------------ | ------------------------------------------------------------ |
| `issues.py`              | Gestión de issues: ver, crear, cerrar, comentar              |
| `prs.py`                 | Gestión de pull requests: revisión, comentarios, aprobación  |
| `stats.py`               | Estadísticas de commits, PRs, repos, lenguaje, etc.          |
| `cleanup.py`             | Limpieza de ramas, tags y repos archivados                   |
| `collaborators.py`       | Administración de colaboradores en repos privados            |
| `releases.py`            | Publicación y edición de releases con changelogs y assets    |
| `readme.py`              | Editor CLI de README.md con vista previa y commit automático |
| `token_scope_checker.py` | Verifica los permisos reales del token personal              |

---

## ✨ Contribuciones

Este proyecto está pensado para desarrolladores que trabajan desde el móvil o en entornos CLI. Si tienes ideas, mejoras o quieres colaborar, ¡bienvenido!

---

## 🧑‍💻 Autor

Desarrollado para Termux por [cmbrdevmx](https://github.com/CmbRDevMx/Github_Manager_CLI/).
