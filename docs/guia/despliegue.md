# 🔄 Flujo de Despliegue Continuo (CI/CD)

El sitio web estático se compila y publica automáticamente en **GitHub Pages**.

## Automatización con GitHub Actions
Cada vez que se realiza un `git push` a la rama `main`, un flujo de trabajo (Workflow) de GitHub ejecuta las siguientes tareas:
1. Levanta un contenedor virtual Ubuntu.
2. Descarga el código fuente del repositorio.
3. Configura el entorno de Python 3.x.
4. Instala el paquete `mkdocs-material`.
5. Ejecuta el comando `mkdocs gh-deploy --force` para subir el HTML estático a la rama `gh-pages`.
