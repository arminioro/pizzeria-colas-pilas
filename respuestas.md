❓ Preguntas de Comprensión (Obligatorias en el PR)
1- ¿Por qué un sistema de delivery usa Queue para los pedidos pero Stack para la bitácora? ¿Qué problema surgiría si invertimos las estructuras?
2- ¿Por qué es obligatorio verificar Count == 0 antes de Dequeue() o Pop()? ¿Qué ocurre en ejecución si se omite?
3- En el método Deshacer, ¿por qué es necesario analizar el texto con .StartsWith() antes de revertir? ¿Qué error lógico evitaría    esto?
4- ¿Qué ventaja tiene entregar mediante Fork + Pull Request en lugar de un archivo comprimido? ¿Cómo facilita la la retroalimentación?

Respuestas.
1- Porque el Queue permite hacer una cola donde cada pedido se hace por orden de llegada, es decir, el primero que llega es el primero que recibe su pedido, mientras Stack permite llevar un registro limpio ya que el ultimo elemento ingresado es el primero que se va. Si se invierte podria generar un problema de logistica, ya que si los Pedidos son Stack, el primer pedido que se ingrese no se entregaría de primero, sino que se entragaría de último y viceversa con bitácora == Stack.

2- Es obligatorio porque si no se verifica si hay o no elementos en la pila o la cola puede dar un error, ya que estarias deshaciendo vacio, o entregando vacio (dependiendo del tipo de acción).

3- Es necesario para revertir el elemento pedido, es decir, si se busca revertir un pedido, usamos .StartsWith("PEDIDO:") para que el sistema sepa que va a revertir el elemento que este en la pila llamado "PEDIDO:", esto evitaria que ocurriera un error, ya que el sistema podría revertir cualquier elemento o directamente se forzaria a cerrar.

4- Además de ser un aprendizaje, actualmente en las empresas se usa GitHub para todo, y es un requisito saber usarlo. Fuera de eso, facilita el tener que comprimir y compartir manualmente el archivo por correo o drive, ademas que con un fork y el pull request puedes directamente modificar el repositorio original siempre y cuando la persona que lo maneja acepte el pull request.