<div align="center">
  <img src="https://user-images.githubusercontent.com/35271042/79503741-8c396a00-7fe6-11ea-97e5-8fd1b3059eb8.png">
</div>

# **¿CÓMO USAR GITHUB PULL REQUESTS? Una breve guía de inicio rápido 🔄**
## **Introducción a GitHub Pull requests** 🔄

Los **Pull Requests (PRs)** 🔄 en **GitHub** son una herramienta esencial para la colaboración en proyectos de desarrollo. Permiten a los equipos trabajar en código de forma ordenada, proponer cambios y revisarlos antes de integrarlos en la rama principal.

Un **Pull Request**  🔄 es una solicitud para que los cambios realizados en una rama sean revisados y, eventualmente, integrados en otra rama del repositorio. Es especialmente útil en proyectos donde múltiples desarrolladores trabajan en paralelo.
Cuando alguien propone cambios, los miembros del equipo pueden:
- Revisar el código,
- Comentar sugerencias y correcciones,
- Probar la funcionalidad,
- Aprobar o rechazar la incorporación del código a la rama principal.

---

## **Explicación del flujo de trabajo en GitHub** 🔄

El uso de GitHub sigue un flujo de trabajo estructurado para garantizar que los cambios en el código sean organizados y revisados adecuadamente. En esta guía vamos a proporcionar los comandos que deben ser utilizados desde Git Bash.

🔹 1. Creación de una rama: Antes de modificar el código, se recomienda crear una nueva rama en el repositorio. Esto permite trabajar sin afectar la rama principal.

<div align="center">
  <img src="nueva_rama.png">
</div>

🔹 2. Realización de cambios y confirmación (````commit````): Después de modificar archivos, se registran los cambios en Git con ````git commit````.

<div align="center">
  <img src="commit.png">
</div>

🔹 3. Envío de la rama al repositorio remoto: Para compartir los cambios en GitHub, se sube la rama con ````git push````.

<div align="center">
  <img src="push.png">
</div>

🔹 4. Revisión del código y colaboración: Una vez los cambios están en el repositorio remoto, los miembros del equipo pueden revisar el código, hacer comentarios y sugerir ajustes para mejorar la calidad del código antes de integrarlo en la rama principal.

🔹 5. Resolución de observaciones y ajustes: Si se detectan mejoras o errores en el código, se pueden realizar correcciones dentro de la misma rama y volver a subir los cambios con ````git commit```` y ````git push````.

🔹 6. Aprobación de los cambios: Antes de fusionar los cambios en la rama principal, es fundamental asegurarse de que han sido revisados y aprobados por el equipo.

---

## **Comandos básicos de Git relacionados** 🔄
Para trabajar con Git y gestionar cambios en un repositorio, es importante dominar algunos comandos esenciales. Aquí tienes una lista de los más relevantes:

📌 Configuración Inicial: Antes de empezar a usar Git, puedes configurar tu usuario y correo...

<div align="center">
  <pre>git config --global user.name "Tu Nombre"</pre></div>

<div align="center">
  <pre>git config --global user.email "tu@email.com"</pre></div>

🔹 Creación y Gestión de Repositorios:
- Inicializar un repositorio Git:

<div align="center">
  <pre>git init</pre></div>
- Clonar un repositorio remoto:
<div align="center">
  <pre>git clone URL-del-repositorio</pre></div>

🔹 Manejo de Ramas:
- Listar ramas en el repositorio:

<div align="center">
  <pre>git branch</pre></div>
- Crear una nueva rama:

<div align="center">
  <pre>git checkout -b nombre-de-la-rama</pre></div>
- Cambiar a otra rama:

<div align="center">
  <pre>git checkout nombre-de-la-rama</pre></div>
- Eliminar una rama local:

<div align="center">
  <pre>git branch -d nombre-de-la-rama</pre></div>

🔹 Realización de Cambios:
- Ver el estado de los archivos modificados:

<div align="center">
  <pre>git status</pre></div>
- Añadir archivos al área de preparación:

<div align="center">
  <pre>git add nombre-de-archivo</pre></div>
- O para añadir todos los archivos modificados:

<div align="center">
  <pre>git add .</pre></div>
- Guardar los cambios con un mensaje:

<div align="center">
  <pre>git commit -m "Mensaje describiendo los cambios"</pre></div>
- Ver historial de commits:

<div align="center">
  <pre>git log</pre></div>

🔹 Trabajo con Repositorios Remotos:
- Conectar el repositorio local con uno remoto:

<div align="center">
  <pre>git remote add origin URL-del-repositorio</pre></div>
- Subir los cambios al repositorio remoto:

<div align="center">
  <pre>git push origin nombre-de-la-rama</pre></div>
- Actualizar el repositorio con cambios remotos:

<div align="center">
  <pre>
git pull origin nombre-de-la-rama</pre></div>

---

## **Crea el Pull Request** 🛠️

Una vez que tu rama ha sido subida a GitHub, es momento de abrir el Pull Request (PR):

1. Dirígete al repositorio en GitHub.
2. Verás un botón que dice **"Compare & pull request"** — haz clic.
<div align="center">
  <img src="pullrequest.png">
</div>

3. Completa los siguientes campos:
- ✍️ **Título**: claro y directo sobre el cambio.
- 📄 **Descripción**: explica qué hiciste, por qué y cómo afecta el proyecto.
- 🔗 **Referencia a Issues (opcional)**: si tu PR soluciona un Issue, escríbelo así:  
     `Closes #23` → esto cerrará automáticamente el issue #23 al hacer merge.
---

## **Espera revisión y responde feedback** 🔧 

Cuando se abre el Pull Request, el equipo podrá:

- 👀 Leer el código.
- 💬 Comentar sugerencias o correcciones.
- ✅ Aprobarlo o solicitar cambios.

Si se te solicita hacer ajustes, puedes realizarlos desde el local y subir los cambios (como se mencionó anteriormente)

```bash
git add .
git commit -m "Aplicar correcciones sugeridas"
git push
```
---

## **Aprobar y fusionar el Pull Request** ✅

Una vez revisado y aprobado por al menos un miembro del equipo (según configuración del repositorio), puedes hacer merge del PR. Hay tres formas comunes:

- 🔀 Merge commit: crea un commit adicional que une las ramas.

- 🧼 Squash and merge: combina todos los commits en uno solo.

- 🔁 Rebase and merge: reescribe el historial a la rama base para mantenerlo lineal.

Haz clic en "Merge pull request" para finalizar el proceso.
<div align="center">
  <img src="mergelu.png">
</div>

---

## **Buenas prácticas al trabajar con Pull Requests** 📌

✍️ Usa títulos y descripciones claros.

👥 Asigna revisores (@usuario) **si es necesario.**

📎 Relaciona los PR con Issues existentes.

🧪 Asegúrate de probar el código antes de abrir el PR.

📂 Borra la rama luego de fusionar si ya no se necesita.

---



