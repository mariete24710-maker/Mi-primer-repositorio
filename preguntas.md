# Entrega de la Práctica 0

1. **¿Qué diferencia hay entre preparar un archivo y confirmarlo?**
   Preparar (`stage`, el `+` en VS Code) es elegir qué cambios de los archivos modificados quieres meter en el siguiente guardado, como dejar lo que vas a subir listo en el banquillo. Confirmar (`commit`) es guardar esa foto de los cambios preparados en el historial local de Git con un mensaje que explica lo que has hecho.

2. **¿Cuándo puedes usar Descartar cambios y qué riesgo tiene?**
   Se usa cuando has tocado un archivo en el directorio de trabajo pero todavía no lo has confirmado (o cuando deshaces el último commit y quieres tirar ese cambio). El riesgo es que borra esos cambios y no se pueden recuperar desde Git, así que hay que mirar bien la diferencia antes de darle.

3. **¿Qué pasa con tu trabajo cuando cambias de una rama a otra?**
   El editor y los archivos cambian al estado que tiene la rama a la que pasas. Lo que tenías confirmado en otra rama no se borra, simplemente queda guardado en su rama hasta que vuelvas a ella o la fusiones.

4. **¿Por qué no hubo conflicto al fusionar rama-a pero sí al fusionar rama-b?**
   Al fusionar `rama-a`, `main` no había modificado esa misma línea del `<h1>`, así que Git pudo aplicar el cambio sin problema. Al fusionar `rama-b`, tanto `main` (con lo que venía de `rama-a`) como `rama-b` habían cambiado la misma línea de forma distinta, y Git no sabe cuál elegir sin que lo decidas tú.

5. **¿Para qué sirve crear una rama de experimento, aunque luego se borre?**
   Sirve para probar cambios o ideas (como cambiar el color de fondo) sin tocar `main` ni arriesgar el proyecto principal. Si el experimento sale mal, borras la rama y `main` sigue intacta.

6. **Si descubres hoy un error cometido hace cinco commits, ¿qué haces para arreglarlo?**
   No sirve deshacer solo el último commit. Miro el historial en la Cronología del archivo afectado, busco una versión anterior donde estuviera bien, copio ese contenido (o recupero el estado anterior) y hago un nuevo commit corrigiéndolo para que quede registrado en el historial.