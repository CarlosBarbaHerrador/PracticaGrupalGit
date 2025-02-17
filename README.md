# PracticaGrupalGit
# Guía para trabajar con Git y GitHub

## 1. Crear una nueva rama para una funcionalidad
Para trabajar en una nueva funcionalidad sin afectar la rama principal, crea una nueva rama con:
```bash
git branch nueva-funcionalidad
git checkout nueva-funcionalidad
```
También puedes hacerlo en un solo paso:
```bash
git checkout -b nueva-funcionalidad
```

## 2. Realizar cambios en la nueva rama y hacer commit
Haz los cambios necesarios en el código y guárdalos en un commit:
```bash
echo "<h1>Hola mundo</h1>" > index.html
git add index.html
git commit -m "Añadir título en index.html"
```

## 3. Subir la rama al repositorio remoto
Para compartir tu rama con el equipo, súbela a GitHub:
```bash
git push origin nueva-funcionalidad
```

## 4. Realizar un Pull Request (PR) en GitHub
Un **Pull Request (PR)** es una solicitud para fusionar los cambios de una rama en otra, generalmente de una rama de desarrollo a `main`. Sirve para revisar y discutir los cambios antes de fusionarlos.

Pasos para crear un PR:
1. Accede al repositorio en GitHub.
2. Ve a la pestaña **"Pull Requests"** y haz clic en **"New Pull Request"**.
3. Selecciona la rama que contiene los cambios y compárala con `main`.
4. Revisa los cambios antes de enviarlos.
5. Escribe una descripción detallada del PR explicando los cambios realizados.
6. Haz clic en **"Create Pull Request"**.
7. Espera revisiones y feedback de los compañeros o del profesor.

## 5. Revisar y fusionar cambios
1. Otro compañero revisa el PR y lo aprueba.
2. Si todo está correcto, se fusiona con la rama `main`.
3. Si hay sugerencias o cambios requeridos, deben realizarse antes de la aprobación.
4. Una vez aprobado, hacer clic en **"Merge Pull Request"** y eliminar la rama si ya no es necesaria.

## 6. Actualizar la rama local con los cambios aprobados
Para mantener tu repositorio local actualizado con la rama principal:
```bash
git checkout main
git pull origin main
```

## 7. Resolución de Conflictos

### 7.1 Generar un conflicto (de forma intencionada)
1. Dos personas editan la misma línea de `index.html` en diferentes ramas y hacen commits.
2. Ambos intentan fusionar sus ramas con `main`.

### 7.2 Resolver el conflicto
1. Git avisará del conflicto.
2. Edita manualmente el archivo afectado, manteniendo los cambios correctos.
3. Una vez resuelto, ejecutar:
```bash
git add index.html
git commit -m "Resolver conflicto en index.html"
git push origin main
```

Con esto, el conflicto quedará solucionado y los cambios podrán fusionarse en `main`.

