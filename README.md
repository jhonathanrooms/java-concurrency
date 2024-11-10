# Java Concurrency
La concurrencia en Java abarca una serie de conceptos y técnicas para permitir la ejecución de múltiples tareas al mismo tiempo, optimizando el uso de los recursos del sistema. 
## Hilos (Threads)
Son la unidad básica de ejecución concurrente. Java proporciona la clase **Thread** y la interfaz **Runnable** para crear y manejar hilos. Cada hilo tiene su propio contexto de ejecución dentro de un programa.
## Sincronización
Garantiza que solo un hilo pueda acceder a una sección crítica de código a la vez. Esto se maneja a través de la palabra clave **synchronized**, que se puede aplicar a métodos o bloques de código para evitar condiciones de carrera (race conditions).
## Bloques y Métodos Synchronized
Permiten que solo un hilo acceda a un bloque de código o método específico a la vez. Esto es útil para proteger datos compartidos.
## Locks y ReentrantLock
**Lock** es una interfaz en el paquete **java.util.concurrent.locks** que proporciona mayor control sobre la sincronización que **synchronized**. **ReentrantLock** es una implementación de esta interfaz que permite bloquear el recurso y desbloquearlo explícitamente.
## Volatile
Asegura que las lecturas y escrituras en una variable sean directamente visibles para todos los hilos. Esto garantiza la visibilidad de cambios en variables compartidas entre hilos.
## Executor Framework
Disponible en **java.util.concurrent**, proporciona una forma de manejar y controlar grupos de hilos. Las interfaces **Executor**, **ExecutorService**, clases como **ThreadPoolExecutos** y **ScheduledThreadPoolExecutor** permiten manejar la concurrencia con mayor flexibilidad.
## Callable y Future
Similar a **Runnable** pero permite que el hilo devuelva un resultado o lance una excepción. **Future** representa el resultado de una tarea asincrónica y permite verificar si la tarea está completa, cancelar la tarea y obtener el resultado.
## Fork/Join Framework
Ayuda a dividir tareas grandes en subtareas más pequeñas y ejecutarlas en paralelo, lo que es útil para operaciones de procesamiento de datos masivos. Se utiliza principalmente con **ForkJoinPool**, **RecursiveTask** o **RecursiveAction**.
## Atomic Variables
**AtomicInteger** y **AtomicRefence** ofrecen operaciones atómica en variables sin necesidad de usar sincronización explícita, estas clases están en **java.util.concurrent.atomic**.
## BockingQueue
Es una interfaz que permite el manejo seguro de colas en entornos concurrentes. Implementaciones como **ArrayBlockingQueue**, **LinkedBlockingQueue** y **PriorityBlockingQueue** facilitan la transferencia de datos entre hilos con control de concurrencia.
## CountDownLatch y CyclicBarrier
Son clases de sincronización avanzadas en **java.util.concurrent**. **CountDownLatch** permite que un hilo espere a un conjunto de operaciones en otros hilos se complete, mientras que **CyclicBarrier** permite que un grupo de hilos espere entre sí para alcanzar un punto común de ejecución.
## Phaser
Similar a **CyclicBarries**, es una herramienta de sincronización más flexible para tareas que implican múltiples fases. útil cuando el número de hilos activos puede cambiar dinámicamente.
## CompletableFuture y Programación Asincrónica
Permite la creación de tareas asincrónicas y la combinación de varias tareas asíncronas. Facilita la programación funcional en Java y el trabajo con promesas(promises) para resultados futuros.
## ThreadLocal
Proporciona variables que son locales al hilo. Esto significa que cada hilo tiene su propia instancia de una variable, lo que evita problemas de concurrencia.