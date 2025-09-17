# **TRABAJO PRÁCTICO 3**


## **1. Configuración inicial del proyecto**

- Crear una organización en Azure DevOps
Para crear la organización fuimos a la pantalla principal de Azure DevOps, y usando el botón Create organization creamos nuestra organización, a la cual llamamos SantiagoTricherri.

- Crear un proyecto con la metodología ágil que consideremos apropiada
Una vez dentro de nuestra organización, creamos un nuevo proyecto usando el botón New Project. Lo nombramos TP3_4 Tricherri y Ojeda, lo configuramos como privado y con la metodología ágil Scrum.

- Configurar los equipos y áreas del proyecto
Para esto, primero fuimos a Project settings → Teams, y allí creamos dos equipos de trabajo: Backend y Frontend.
Por otro lado, para crear las áreas fuimos a Project settings → Project configuration y desde allí creamos dos sprints con su respectiva fecha, de modo que el segundo empiece cuando termine el primero.


## **2. Gestión del trabajo con Azure Boards**

- Crear un Epic que represente una funcionalidad completa

Fuimos a la sección Boards → Work items y allí creamos un nuevo work item de tipo Epic. Lo nombramos Gestión de Pedidos Online, que representa la funcionalidad general de permitir a los clientes registrarse, armar un carrito y realizar un pedido en la aplicación.

- Crear 3 User Stories relacionadas con el Epic

Dentro del Epic, en la parte de Related Work, usamos la opción Add link → Child → Product Backlog Item, y así fuimos creando tres PBIs como hijos del Epic. Los llamamos:
1. **Registro de usuarios**
2. **Carrito de compras**
3. **Pago en línea**

- Crear 2 Tasks por cada User Story

Abrimos cada PBI creado y desde Related Work, con la opción Add link → Child → Task, agregamos dos tareas.
Por ejemplo, en “Registro de usuarios” creamos las tareas Diseñar UI registro e Implementar validación y almacenamiento.
Hicimos lo mismo para los otros dos PBIs, cada uno con dos tareas correspondientes.

- Crear 2 Bugs de ejemplo

En la misma sección Boards, Work items, creamos dos nuevos work items de tipo Bug. Los nombramos **Validación de contraseña no bloquea envío** y **Carrito no actualiza el total al quitar producto**, simulando errores que podrían encontrarse en el desarrollo.

- Configurar un Sprint de 2 semanas

Para configurar el Sprint fuimos a Project Settings → Project Configuration → Iterations y allí creamos una nueva iteración llamada **Sprint 1**, con una duración de dos semanas.

- Asignar los work items al Sprint

Finalmente, editamos algunos PBI, Task y Bug creado, y en el campo Iteration seleccionamos **Sprint 1**, de modo que todos quedaran dentro del primer Sprint y pudieran visualizarse desde Boards.


## **3. Control de versiones con Azure Repos**

- Importar o crear un repositorio con código de una aplicación

Para esto entramos en la sección **Repos** dentro de mi proyecto. Allí utilizamos la opción **New repository** y creamos un nuevo respositorio git llamado PruebaEj3.

- Configurar políticas de branch para la rama principal

Dentro de **Repos, Branches**, seleccionamos la rama **main** y abrimos el menú de **Branch policies**.  
Desde allí configuramos las siguientes políticas:  
1. **Requerir Pull Request**: habilitamos la opción que impide pushear cambios directos a la rama main.  
2. **Mínimo 1 reviewer**: configuramos que cada Pull Request necesite al menos una revisión/aprobación antes de poder hacer merge.

- Crear al menos 2 branches de feature

Desde **Repos, Branches** usamos la opción **New branch**. Creamos dos ramas nuevas a partir de main, con los nombres:  
- `feature/login`  
- `feature/carrito`

- Realizar cambios y crear Pull Requests

Nos cambiamos a cada rama desde la interfaz web de Azure DevOps,  En `feature/login` editamos un archivo de ejemplo (README.md) para simular un cambio, y lo guardamos en esa rama.  
Luego fuimos a **Repos, Pull requests**, y con el botón **New Pull Request** abrimos un PR desde `feature/login` hacia `main`. El sistema aplicó la política configurada y nos pidió al menos 1 revisor. Lo mismo pasaría con la rama `feature/carrito`.  
De esta manera se validó el flujo de trabajo: desarrollo en ramas de feature, revisión obligatoria y posterior integración a main mediante Pull Request.


## Uso de IA

Para este TP utilizamos la IA (ChatGPT) como apoyo: nos propuso una estructura de épicas, historias de usuario y tareas para simular un caso real. Por otro lado,  nos ayudó a entender algunos conceptos sobre los que se nos generaban dudas. 
