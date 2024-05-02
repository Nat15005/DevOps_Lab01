# DevOps_Lab01

## Managing Project Schedules across Teams with Delivery Plans

### Prerrequisitos

1. Vaya a https://azuredevopsdemogenerator.azurewebsites.net. Este sitio de utilidades automatizará el proceso de creación de un nuevo proyecto de Azure DevOps dentro de la cuenta que se rellena previamente con el contenido (elementos de trabajo, repositorios, etc.) necesario para el laboratorio. Para obtener más información sobre el sitio, consulte https://docs.microsoft.com/en-us/azure/devops/demo-gen.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/4368b6f5-6a6d-4f31-bcd1-879b7df38fe0)


2. Inicie sesión con la cuenta de Microsoft asociada a su suscripción de Azure DevOps.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/a47b56cb-f045-4d0f-8e09-8191ce38bbc3)

3. Acepte las solicitudes de permiso para acceder a su suscripción.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/9ffe87a1-2653-4a5f-81d5-4d065fd071c9)

4. Seleccione la organización de Azure DevOps y escriba el nombre del proyecto "Parts Unlimited". Haga clic en Elegir plantilla.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/909bf95d-da63-4252-94a3-2b6a6727e9ae)

5. Seleccione la plantilla PartsUnlimited y haga clic en Seleccionar plantilla.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/6db7bb14-d1b4-4443-a879-3a389ae339e7)

6. Haga clic en Crear proyecto y espere a que se complete el proceso.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/f51e66d4-a0fd-4ed9-81b2-d9608be2ed31)

7. Verificamos que se haya creado el proyecto en Azure DevOps

   ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/cc6d481b-e03c-4ddf-bf05-6f5f949cca68)


## Ejercicio 1: Administración de planes de entrega con Azure DevOps

### Tarea 1: Creación de un plan de entrega

1. En el menú desplegable Tableros, seleccione Planes de entrega.
   
    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/891e13a1-6237-4fc1-a8a3-bc5dadb01eb7)

2. Haz clic en Nuevo plan.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/3dafdc6c-bd5c-4dd7-bf6b-b8a23f190794)


3. Dado que es posible que desee tener varios planes de entrega para diferentes aspectos del proyecto, proporcione el nombre específico "Entrega web". De forma predeterminada, debería ser el equipo de Parts Unlimited, así que seleccione Características y haga clic en Crear. Tenga en cuenta que también puede organizar sus envíos por Historias si utiliza ese modelo en su lugar. También existe la opción de agregar equipos y criterios adicionales para filtrar historias/características, pero los revisaremos más adelante.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/aa56fc78-f46d-4fbd-86ed-643f7b084d57)

4. Debido a la reconfiguración de la iteración realizada anteriormente, el marcador "Hoy" está justo al comienzo del Sprint 2. Tenemos una serie de historias listadas para su entrega en el sprint anterior, y también podemos ver un Sprint 3 vacío. Tenga en cuenta que algunas de las historias que se muestran están terminadas. Aunque es útil ver el progreso del trabajo, lo usaremos como ejemplo para filtrar los elementos en un momento.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/a8329eb1-1bfc-42e9-81ce-f7077fb9653e)


5. Haga clic en el botón Configuración.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/6290b230-353b-4281-9df0-f5b24a951f19)
  
6. Seleccione la pestaña Criterios de campo y haga clic en Agregar criterios.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/672b9d3f-378b-4f56-a0cf-a50d2713cb76)

7. Establezca los nuevos criterios para filtrar los elementos en los que el estado no es igual a (<>) Hecho.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/85cdcc46-4ca2-4150-97a8-c86fb0d39410)

8. También podemos agregar un marcador personalizado para realizar un seguimiento de las fechas significativas. Seleccione la pestaña Marcadores y haga clic en Agregar marcador.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/a525e8d4-4243-4c8d-8f4c-40d9587f7d68)

9. Selecciona el cuarto viernes a partir de hoy (será el viernes en medio del Sprint 3) y establece la etiqueta en "Equipo fuera del sitio". Seleccione un color y haga clic en Guardar.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/4c075c13-ce06-4454-a868-91b887427fc6)

10. Lo primero que hay que tener en cuenta es que el caso "Cerrado" ya no está visible en el plan de entrega debido a los criterios establecidos en la configuración. Además, ahora hay un marcador magenta en el medio de la iteración 3 que dice "Equipo fuera del sitio" cuando se hace clic en él.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/16337590-78bf-4ae3-a029-adce342a8418)


### Tarea 2: Agregar un equipo externo al proyecto

1. Nuestro plan de entrega ha sido bastante simple hasta ahora porque solo tenemos un equipo. Sin embargo, el verdadero poder de la planificación de la entrega entra en juego cuando se orquestan varios equipos autónomos en sus esfuerzos. Abra la página de configuración mediante la navegación Configuración del proyecto ubicada en la parte inferior izquierda de la página

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/dd6f36bd-ac5d-44fd-b9d8-02c5c1c21dd3)

2. En la pestaña Equipos, haga clic en Nuevo equipo.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/6d14e101-ad61-4866-9160-6315bebd1df9)


3. Este nuevo equipo será responsable de los esfuerzos que implican la integración con servicios externos, como los servicios de terceros para cosas como pronósticos meteorológicos y procesamiento de pagos. Establezca el nombre del equipo en "Equipo de integración externo" y haga clic en Crear equipo.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/d91c0e25-9f26-4d66-9dcf-ca4fb98fb904)

4. Seleccione la pestaña Configuración del proyecto en Tableros.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/4cbdcefb-b88c-4958-8859-d90cc8665f35)

5. Tenga en cuenta las fechas del Sprint 2 y el Sprint 3, que variarán para su cuenta en función de cuándo generó los datos del proyecto. Vamos a agregar dos nuevas iteraciones para el equipo de servicios externos que no se alinean exactamente con la programación del equipo principal.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/2aed01bd-826a-41ed-b183-b9f758b8b02b)

6. Con la selección del nodo raíz PartsUnlimited, haga clic en Nuevo elemento secundario.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/8e04bb1c-885d-4a79-aebe-0c9145ee5050)

7. Establezca el nombre de la iteración en "Iteración 50". Use hoy como fecha de inicio y establezca la fecha de finalización en tres viernes a partir de hoy. Este también será el día del equipo fuera de la oficina. Haga clic en Guardar y cerrar.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/515ca2ad-bf1e-4654-a5f5-8a24df99d817)

8. Use el mismo proceso para agregar una iteración 51 que comience el lunes después de que finalice la iteración 50 y tenga una fecha de finalización tres viernes después.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/2cb4eb34-19bf-4d92-8cbf-f637592642df)

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/100adcba-443b-47e1-8a6e-1eb4f143fdd3)


9. Ahora tenemos que configurar el nuevo equipo para que use esos nuevos sprints de proyecto como sus iteraciones. Seleccione la pestaña Equipos y haga clic en Equipo de integración externo.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/46ea3a4d-3fff-40e7-b434-29356de0149b)

10. Haga clic en Iteraciones y rutas de área

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/d8f9f075-2c15-4207-b44b-f2777dc034cd)

11. Seleccione la pestaña Iteraciones.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/1c2716fe-3adb-4979-9a32-478feb36f085)

12. Haga clic en Seleccionar iteraciones y use el botón + Iteración para seleccionar la Iteración 50 y la Iteración 51. Haga clic en Guardar y cerrar.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/df906a25-1c4c-4728-b3e0-fa3fb34488ef)


### Tarea 3: Toma de decisiones de entrega

1. En el menú desplegable Tableros, seleccione Planes de entrega.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/ddff4479-af6d-4b5e-a0ae-8ea5f6b99588)

2. Seleccione el plan de entrega web.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/51868efb-c51d-4a71-8227-9757025e0f33)

3. Haga clic en el botón Configuración.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/310d93c5-5f89-4af0-9e50-2f25b28358be)

4. Seleccione la pestaña Equipos y haga clic en Agregar equipo.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/7abc8597-9684-4437-9417-25f87f9de9a3)

5. Seleccione el equipo de integración externa y Características. Haga clic en Guardar.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/6b015751-d4d0-4bc0-b29f-f88e8705a831)

6. Utilice el alejamiento para ajustar el ancho de la iteración 50 y la iteración 51.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/ff01c18c-613b-4011-966b-575c3c0e66ed)

7. El nuevo equipo aún no tiene ninguna historia agregada. Afortunadamente, puede agregarlos directamente a su equipo e iteración mediante la funcionalidad en línea. Seleccione la iteración 50. Haga clic en el botón Nuevo elemento que aparece.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/f379b744-259e-4b6b-95c1-4683a03281dd)

8. Ingrese "Integrar con el servicio meteorológico" y presione Enter. Ese elemento se encuentra ahora en el trabajo pendiente con su área e iteración configuradas.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/e45c4d27-ba9e-42bd-9f97-09709ee2b4d8)

9. Siga el mismo proceso para agregar un elemento para integrarlo con activos de marca corporativa a la iteración 51.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/4041bfe4-fdd3-4bf3-837c-58380a8cce3c)

10. Ahora podemos dar un paso atrás para ver cómo estos dos equipos están trabajando hacia nuestros objetivos comunes. Tras un examen más detallado, parece que el equipo principal está planeando reutilizar algunos activos de marca corporativa durante el sprint actual que no estarán disponibles hasta mucho después de que termine. Es bueno que tengamos esta visión para detectar este tipo de problemas potenciales desde el principio.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/d0a4d35e-9f01-4129-86c6-f1cb6f19b9c1)

11. Lo primero que debemos hacer es trasladar el trabajo de integración de marca a una iteración anterior. Arrastre y suelte la historia de marca corporativa en la iteración 50. Para liberar el ancho de banda, arrastre la historia del servicio meteorológico a la iteración 51.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/dcfdf061-4142-45dc-a9cc-57d0f2ce5dfb)

12. A continuación, arrastre el elemento de trabajo de personalización de marca del Sprint 1 al Sprint 3 para que exista la posibilidad de que las dependencias estén disponibles a tiempo para que se desbloquee este equipo.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/7a989d3c-1f86-49b8-b2a1-ff0c309f5084)

13. Ahora podemos volver a revisar el plan de entrega. Debería ser más factible ahora.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/fa6d8a6a-4fde-4fda-837c-489007407f60)

14. Hay muchas maneras de personalizar rápidamente la vista del plan de entrega. Por ejemplo, puede contraer todos los equipos (o equipos específicos) usando los botones de alternancia junto a sus nombres.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/71500c3b-8870-46da-a28e-b4fb2328a93a)


### Tarea 4: Realizar un seguimiento de las dependencias mediante planes de entrega
Con los planes de entrega, puede realizar un seguimiento de las dependencias que se han agregado a los elementos de trabajo. El seguimiento de dependencias admite el tipo de vínculo predecesor/sucesor entre los elementos de trabajo.

1. Vaya a Plan de entrega web.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/7364cb28-fe1e-464a-98e7-d76221159cb1)

2. Mover la función de marca a Sprint 1

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/17f0a219-ddd2-432d-9fca-26e764eec642)

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/60b9b778-5b00-4e1c-9cd7-b3d696c32acf)


3. Y haga clic en la pestaña Enlaces y agregue las funciones Integrar con el servicio meteorológico e Integrar con activos de marca corporativa como Sucesores y Guardar y cerrar

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/2a8157bf-b12a-4e1b-a525-f548f2b34aa7)

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/65df1b92-ab48-46f1-89cd-4aaa33bfc181)

4. Ahora su plan de entrega se ve como se muestra a continuación. Haga clic en donde está señalado para ver el resumen de dependencias

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/cb02a511-a567-495a-b0a8-3efd78182dcb)

5. Puede ver la vista detallada Dependencias. Esto indica que el elemento de trabajo tiene dos sucesores y no hay problemas con las fechas de entrega.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/5b2b0423-166b-4b88-87d0-a049eb1ffb81)

6. Ahora mueva la función de marca al sprint 2 y actualice la página.
    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/5e39cb79-12c5-4b73-855b-c478530b95d7)

7. Ahora puede ver el icono señalado en la función. Haga clic para ver los detalles. Aquí podemos ver que una función tiene un problema de entrega. Con esta información podemos planificar la entrega de la característica dependiente.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/9defe30f-6a26-4525-9685-86d56029819a)

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/e13d135f-7b51-4e95-a378-f4c0c7d5a817)

8. Haga clic en el icono Mostrar todas las dependencias. Las líneas de dependencia que no tienen problemas se muestran como líneas negras. Las líneas de dependencia que tienen problemas se muestran con líneas rojas. Para ver el problema o los detalles, puede hacer clic en esas líneas.

    ![image](https://github.com/Nat15005/DevOps_Lab01/assets/111907712/74de5691-154e-426b-bf1d-b9bb2e9954ef)

   



