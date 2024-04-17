# JUSTIFICACIONES DE DISEÑO

## Patron Strategy
Se decidió el uso del patron Strategy para modelar las distintas estrategias de reacción a un posible incidente, como el enunciado es explicito a la hora de pedir que se deben poder agregar mas poisble estrategias en el futuro. El patron Strategy es excelente para cumplir este requerimiento, ya que permite que un componente utilice polimorficamente distintos algoritmos para realizar una misma tarea y ademas permite que se cambie de algoritmos o de "estrategia" en tiempo de ejecución, es configurable incluso por el usuario.


## Patron Adapter

El enunciado no aclara que podrian haber diferentes formas de calcular la demora ademas de usando la API de google, pero si fuera una posibilidad, aca se puede usar un patron adapter. Caso contrario, se podria poner toda la logica dentro del metodo getTiempoDemora() de la clase Viaje. Pero como no sabemos del todo como funciona la API google es interesante usar un patron adapter para poder modelar los componentes propios acorde al enunciado y luego que el adapter se encargue de manejar la API de google.
