# python-clean-architecture-base

Este proyecto es un esqueleto base diseñado para iniciar cualquier desarrollo en Python siguiendo buenas prácticas de código, formateo y pruebas. Incluye una configuración lista para usar con herramientas modernas de calidad y productividad.

## Características principales

- **Estructura modular** para facilitar la escalabilidad y el mantenimiento.
- **Control de calidad** con [Ruff](https://docs.astral.sh/ruff/) para linting y formateo automático.
- **Pruebas unitarias** con [pytest](https://docs.pytest.org/).
- **Chequeo de tipos** con [mypy](https://mypy-lang.org/).
- **Soporte para Dev Containers**: configuración lista para entornos de desarrollo reproducibles en VS Code.

## Estructura del proyecto

```
├── src/                # Código fuente principal
│   └── main.py         # Ejemplo de punto de entrada
├── tests/              # Pruebas unitarias
│   └── test_main.py    # Ejemplo de test
├── requirements.txt    # Dependencias de Python
├── pyproject.toml      # Configuración de herramientas
├── .devcontainer/      # Configuración para Dev Container
│   ├── devcontainer.json
│   ├── Dockerfile
│   └── settings.json
```

## Instalación y uso

### 1. Clona el repositorio
```bash
git clone https://github.com/polroyg/python-clean-architecture-base.git
cd python-clean-architecture-base
```

### 2. Abre en VS Code usando Dev Container
1. Instala la extensión "Dev Containers" en VS Code.
2. Abre la carpeta del proyecto en VS Code.
3. Selecciona "Reabrir en contenedor" cuando se te solicite.

### 3. Instala las dependencias (si no usas devcontainer)
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### 4. Ejecuta los tests
```bash
pytest
```

### 5. Chequea el código
```bash
ruff check src/
mypy src/
```

## Pre-commit

Este proyecto incluye soporte para [pre-commit](https://pre-commit.com/) mediante el archivo `.pre-commit-config.yaml`. Pre-commit permite ejecutar automáticamente comprobaciones de calidad de código (como Ruff, mypy, formateo, etc.) antes de cada commit, ayudando a mantener la calidad y coherencia del código en el repositorio.

### Instalación y uso de pre-commit (si no usas devcontainer)

1. Instala pre-commit si no lo tienes:
	```bash
	pip install pre-commit
	```
2. Instala los hooks definidos en `.pre-commit-config.yaml`:
	```bash
	pre-commit install
	```
3. Ahora, cada vez que realices un commit, se ejecutarán automáticamente los chequeos configurados.

Puedes ejecutar todos los hooks manualmente en todos los archivos con:
```bash
pre-commit run --all-files
```

## Buenas prácticas incluidas
- Linting y formateo automático en cada guardado.
- Organización y limpieza de imports.
- Pruebas unitarias obligatorias para nuevas funcionalidades.
- Tipado estático recomendado en todo el código.

## Personalización
Puedes modificar la configuración de las herramientas en `pyproject.toml` y los settings de VS Code en `.devcontainer/devcontainer.json` en la sección de settings.

## Contribuciones

¡Las contribuciones son bienvenidas!
Si quieres mejorar este esqueleto base, añadir nuevas herramientas o corregir errores, no dudes en abrir un *issue* o enviar un *pull request*.

Por favor, asegúrate de seguir las buenas prácticas de código y pruebas incluidas en este proyecto.

## Licencia

Este proyecto está bajo la licencia MIT.
Puedes usarlo libremente en proyectos personales o comerciales, siempre que mantengas el aviso de copyright.

## Autor
Pol Roy Garcia
