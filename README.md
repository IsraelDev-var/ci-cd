# CI/CD para Proyecto TDD

Este repositorio incluye un pipeline basico de CI en GitHub Actions.

## Workflow incluido

Ruta del workflow: `.github/workflows/ci-pipeline.yml`

Eventos que disparan el pipeline:
- push
- pull_request

Pasos automatizados:
- Clonar repositorio
- Configurar entorno
- Compilar proyecto

## Flujo de ramas sugerido

- main
- develop
- feature/nueva-funcionalidad

## Comandos para preparar y subir el repositorio

1. Inicializar Git

```powershell
git init
git branch -M main
git checkout -b develop
```

2. Crear rama de funcionalidad

```powershell
git checkout -b feature/nueva-funcionalidad
```

3. Primer commit

```powershell
git add .
git commit -m "Agregar pipeline CI con GitHub Actions"
```

4. Conectar con GitHub y subir ramas

```powershell
git remote add origin https://github.com/TU_USUARIO/TU_REPOSITORIO.git
git push -u origin main
git push -u origin develop
git push -u origin feature/nueva-funcionalidad
```

5. Crear Pull Request

- En GitHub, abrir un PR desde `feature/nueva-funcionalidad` hacia `develop`.
- Verificar ejecucion en la pestaña Actions.

## Entregable

- Enlace del repositorio en GitHub
- Captura del workflow ejecutado en Actions
