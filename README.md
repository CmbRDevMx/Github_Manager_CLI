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

## 🧭 Uso

Asegúrate de tener Python y Termux instalados. Luego:

```bash
./repos.py   # Para gestionar visibilidad de repositorios
./forks.py   # Para eliminar forks
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
