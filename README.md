# Repositorio de Código Asociado a la Tesis de Magíster

Código de la tesis de magíster sobre modelos de difusión.

## Estructura

```
.
├── src/        # Paquete principal con el código fuente
├── scripts/    # Scripts ejecutables
├── configs/    # Archivos de configuración
├── data/       # Datasets (no versionado)
├── outputs/    # Checkpoints, muestras y logs (no versionado)
└── tests/      # Tests
```

## Configuración del entorno (conda)

1. Crear el entorno a partir de `environment.yml`:

   ```bash
   conda env create -f environment.yml
   ```

2. Activar el entorno:

   ```bash
   conda activate diffusion-models
   ```

3. Instalar los hooks de pre-commit (solo una vez):

   ```bash
   pre-commit install
   ```

Para actualizar el entorno si cambian las dependencias:

```bash
conda env update -f environment.yml --prune
```

## Formato automático en cada commit

El repositorio usa [pre-commit](https://pre-commit.com/) con [ruff](https://docs.astral.sh/ruff/) para formatear y lintear el código automáticamente antes de cada commit. La configuración está en `.pre-commit-config.yaml`.

Para correr los hooks manualmente sobre todos los archivos:

```bash
pre-commit run --all-files
```
