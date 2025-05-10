![github_token](https://github.com/user-attachments/assets/4b6f4646-4581-4212-be85-47297ea5a508)# 🛠️ GitHub Manager CLI Tools for Termux

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

## Creando token 
Para usar correctamente el programa con el CLI de GitHub, deberás crear un **token de acceso personal** siguiendo estos pasos:

1. Visita el enlace: [https://github.com/settings/tokens](https://github.com/settings/tokens).
2. Haz clic en "Generate new token" (puede decir "Classic token").
3. Asigna un nombre al token y elige una expiración (recomendado: "No expiration" solo si es seguro).
4. Marca los permisos necesarios, **mínimo activa el permiso `repo` y `admin`** para permitir la gestión de la visibilidad de los repositorios y la eliminación de los mismos a gestionar.
5. Genera el token y **cópialo inmediatamente** (no podrás volver a verlo).
6. Ejecuta el programa y cuando se te solicite, ingresa tu **nombre de usuario de GitHub** y **pega el token generado** cuando se te pida el "Token de GitHub".

![Uploa<?xml version="1.0" encoding="UTF-8"?>
<svg viewBox="0 0 800 500" xmlns="http://www.w3.org/2000/svg">
  <!-- Fondo con gradiente moderno -->
  <defs>
    <linearGradient id="bgGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1a1a2e" />
      <stop offset="100%" stop-color="#16213e" />
    </linearGradient>
    
    <!-- Sombras para efecto 3D -->
    <filter id="shadow1" x="-20%" y="-20%" width="140%" height="140%">
      <feDropShadow dx="4" dy="4" stdDeviation="6" flood-color="#000" flood-opacity="0.3"/>
    </filter>
    
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="5" result="blur"/>
      <feFlood flood-color="#4f8ff7" flood-opacity="0.5" result="color"/>
      <feComposite in="color" in2="blur" operator="in" result="glow"/>
      <feMerge>
        <feMergeNode in="glow"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <!-- Fondo -->
  <rect width="800" height="500" fill="url(#bgGradient)" rx="15" ry="15"/>
  
  <!-- Logo GitHub estilizado -->
  <g transform="translate(80, 80) scale(0.8)" filter="url(#shadow1)">
    <circle cx="100" cy="100" r="90" fill="#2a2a72" stroke="#4f8ff7" stroke-width="5"/>
    <path d="M100,35 C64,35 35,64 35,100 C35,129 53,153 79,161 C84,162 86,159 86,156 C86,153 86,148 86,142 C67,146 63,132 63,132 C60,124 55,122 55,122 C48,117 56,117 56,117 C64,118 67,124 67,124 C74,136 86,133 87,130 C88,126 90,122 93,120 C77,118 61,112 61,85 C61,77 64,70 67,65 C66,63 64,55 68,46 C68,46 75,44 86,52 C90,50 96,49 100,49 C104,49 110,50 114,52 C125,44 132,46 132,46 C136,55 134,63 133,65 C137,70 139,77 139,85 C139,112 123,118 107,120 C110,123 113,129 113,137 C113,149 113,153 113,156 C113,159 115,162 120,161 C146,153 165,129 165,100 C165,64 136,35 100,35 Z" fill="#ffffff"/>
  </g>
  
  <!-- Tarjeta de token -->
  <g transform="translate(250, 70)">
    <rect width="480" height="320" rx="15" fill="#24292e" filter="url(#shadow1)"/>
    
    <!-- Header de la tarjeta -->
    <rect width="480" height="60" rx="15" fill="#2ea44f"/>
    <text x="20" y="38" font-family="Arial, sans-serif" font-size="24" font-weight="bold" fill="white">Personal Access Token</text>
    
    <!-- Contenido de la tarjeta -->
    <g transform="translate(30, 80)">
      <!-- Permisos -->
      <g>
        <rect x="0" y="0" width="100" height="100" rx="10" fill="#6f42c1" filter="url(#glow)"/>
        <text x="50" y="40" font-family="Arial, sans-serif" font-size="16" font-weight="bold" fill="white" text-anchor="middle">admin:org</text>
        <text x="50" y="65" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">Administrar</text>
        <text x="50" y="85" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">organizaciones</text>
      </g>
      
      <g transform="translate(120, 0)">
        <rect x="0" y="0" width="100" height="100" rx="10" fill="#f97316" filter="url(#glow)"/>
        <text x="50" y="40" font-family="Arial, sans-serif" font-size="16" font-weight="bold" fill="white" text-anchor="middle">repo</text>
        <text x="50" y="65" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">Acceso</text>
        <text x="50" y="85" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">repositorios</text>
      </g>
      
      <g transform="translate(240, 0)">
        <rect x="0" y="0" width="100" height="100" rx="10" fill="#0ea5e9" filter="url(#glow)"/>
        <text x="50" y="40" font-family="Arial, sans-serif" font-size="16" font-weight="bold" fill="white" text-anchor="middle">user</text>
        <text x="50" y="65" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">Control de</text>
        <text x="50" y="85" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">usuario</text>
      </g>
      
      <g transform="translate(120, 120)">
        <rect x="0" y="0" width="100" height="100" rx="10" fill="#ef4444" filter="url(#glow)"/>
        <text x="50" y="40" font-family="Arial, sans-serif" font-size="16" font-weight="bold" fill="white" text-anchor="middle">delete_repo</text>
        <text x="50" y="65" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">Eliminar</text>
        <text x="50" y="85" font-family="Arial, sans-serif" font-size="12" fill="#d1d5db" text-anchor="middle">repositorios</text>
      </g>
    </g>
  </g>
  
  <!-- Etiqueta explicativa -->
  <g transform="translate(400, 410)">
    <rect width="300" height="60" rx="30" fill="#4338ca" filter="url(#shadow1)"/>
    <text x="150" y="35" font-family="Arial, sans-serif" font-size="18" font-weight="bold" fill="white" text-anchor="middle">Token para CLI de GitHub</text>
  </g>
</svg>
ding github_token.svg…]()


<p align="center">
  <img src="https://github.com/user-attachments/assets/55b37353-1497-40c6-9d21-df7724859027" alt="image termux github CLI API" width="50%">
</p>


## ✨ Contribuciones

Este proyecto está pensado para desarrolladores que trabajan desde el móvil o en entornos CLI. Si tienes ideas, mejoras o quieres colaborar, ¡bienvenido!

---

## 🧑‍💻 Autor

Desarrollado para Termux por [cmbrdevmx](https://github.com/CmbRDevMx/Github_Manager_CLI/).
