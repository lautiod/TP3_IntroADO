# TP3 – Introducción a Azure DevOps

Este repositorio documenta el Trabajo Práctico 3 de la materia **ISW3**, donde aplicamos los conceptos básicos de **Azure DevOps**: organización, gestión ágil, control de versiones y pipelines.

---

## Acceso al proyecto de Azure DevOps
El proyecto fue creado dentro de la organización de Azure DevOps:

- **Organización:** `SantiagoTricherri`
- **Proyecto:** `TP3_4 Tricherri y Ojeda`  
- **Metodología elegida:** Scrum  
- **Equipos configurados:** Backend y Frontend  

[Acceder al proyecto en Azure DevOps] https://dev.azure.com/santiagotricherri/TP3_4%20Tricherri%20Y%20Ojeda

> **Importante:** Para poder clonar el repositorio y visualizar/ejecutar los pipelines en Azure DevOps, es necesario tener acceso a la **organización** y al **proyecto**.  
> Solo los usuarios agregados como miembros podrán interactuar con el repositorio y los pipelines.

---

## Repositorio
Se creó un repositorio Git dentro de Azure DevOps:

- **Nombre del repo:** `PruebaEj3`
- **Rama principal:** `main`
- **Branches de feature creadas:**
  - `feature/login`
  - `feature/carrito`

### Clonado del repositorio
 ```
bash
git clone https://dev.azure.com/santiagotricherri/TP3_4%20Tricherri%20Y%20Ojeda/_git/PruebaEj3
cd PruebaEj3

```

## Políticas de branch

Se configuraron las siguientes políticas para la rama `main`:

- Cambios solo vía **Pull Request**.  
- Al menos **1 revisor obligatorio**.  
- Bloqueo de **push directo** a `main`.  

---

## Pipelines

El proyecto cuenta con un pipeline de CI/CD básico en Azure Pipelines:

- **Ubicación:** sección **Pipelines** de Azure DevOps.  
- **Archivo de definición:** `azure-pipelines.yml` en la raíz del repositorio.  

### Ejecución:
- Cada **push** a una rama `feature/*` dispara la ejecución del pipeline.  
- Los cambios integrados a `main` vuelven a ejecutar el pipeline para validar la build.  

Para correr el pipeline manualmente:  
Ingresar a **Pipelines** → seleccionar el pipeline → botón **Run pipeline**.  

---

## Estructura del proyecto

- **Decisiones.md** → Documentación de las decisiones tomadas (metodología, justificación, organización del trabajo).  
- **README.md** → Este archivo con las instrucciones.  
- **azure-pipelines.yml** → Definición del pipeline CI/CD.  
- **Código fuente** → Dentro del repositorio `PruebaEj3`, editable desde las ramas `feature/*`.  


Código fuente → Dentro del repositorio PruebaEj3, editable desde las ramas feature/*.
