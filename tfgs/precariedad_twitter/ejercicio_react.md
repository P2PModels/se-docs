# Ejercicio React

## Introducción

React es un framework de desarrollo para el lenguaje JavaScript. En React el código que se escribe se asemeja a las etiquetas HTML pero directamente en JavaScript. Estas etiquetas son luego pre-procesadas por herramientas como [webpack](https://webpack.js.org/) para que puedan ser ejecutadas en un navegador. 

Además de etiquetas similares a las HTML, React incorpora patrones de desarrollo y elementos conceptuales, como los fragmentos, los estados, los componentes, las propiedades, y los hooks, cuyos objetivos son organizar y estructurar la arquitectura del sofware así como también facilitar la implementación de interfaces de usuario web altamente sofisticadas.

Para más información sobre el framework React se puede consulta la [documentación técnica](https://reactjs.org/) oficial y/o el libro [Learning React: Modern Patterns for Developing React Apps](https://github.com/MoonHighway/learning-react).

## Ejercicio práctico

Para comenzar a experimentar con el framework se propone la construcción de una aplicación [single page](https://en.wikipedia.org/wiki/Single-page_application) para la gestión de listas de tareas pendientes. La aplicación debe permitir al usuario crear, modificar, y eliminar listas de tareas pendientes así como también crear, modificar, buscar, y eliminar tareas. 

### Lista de tareas

El usuario debe poder crear, modificar, y eliminar listas de tareas. Para la creación de una lista el usuario debe ingresar el nombre de la misma y además debe tener la opción de agregar una descripción. También, el usuario debe tener la posibilidad de modificar el nombre y la descripción de la lista. La eliminación de una lista debe estar precedida por una confirmación por parte del usuario.

### Tareas

El usuario debe poder crear, modificar, y eliminar tareas. Para la creación de una tarea el usuario debe ingresar el nombre, deadline (fecha y hora) de la tarea, así como también la prioridad que tiene la misma, esto es alta, media, baja. Además, al momento de la creación el usuario debe indicar la lista de tareas a la que corresponde la tarea. El usuario debe poder modificar el nombre, deadline, prioridad, y lista de una tarea. Al igual que en el caso de las listas de tareas, la eliminación de una tarea debe estar precedida de una confirmación.

### Búsqueda de tareas

Además de poder crear listas y tareas, el usuario debe tener la posibilidad de buscar una tarea ya sea por palabra clave, por fecha, o por prioridad.
