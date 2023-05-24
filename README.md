@staticmethod
def get_instance():
    if Singleton._instance is None:
        Singleton._instance = Singleton()
    return Singleton._instance

def __init__(self):
    if Singleton._instance is not None:
        raise Exception("Esta clase es un Singleton. Utilice el método 'get_instance()' para obtener una instancia.")
        
        Supongamos que tenemos un proyecto de gestión de tareas en el que los usuarios pueden crear, actualizar y eliminar tareas. Una funcionalidad adicional que deseamos implementar es la capacidad de enviar notificaciones a los usuarios cuando se les asigne una nueva tarea. En este caso, podríamos aplicar el patrón de comportamiento "Observer" para implementar esta funcionalidad de notificación.
        
        El patrón Observer permite que los objetos observadores sean notificados automáticamente cuando se produce un cambio en el objeto observado. En este caso, el objeto observado sería la lista de tareas y los objetos observadores serían los usuarios interesados en recibir notificaciones de nuevas tareas asignadas.
        
        El refactoring para aplicar este patrón podría involucrar los siguientes pasos:

Identificar las clases involucradas: En este caso, identificaríamos la clase que representa la lista de tareas y la clase que representa a los usuarios.

Crear una interfaz o clase base de observadores: Definir una interfaz o clase base que establezca los métodos que los observadores implementarán, como por ejemplo, un método "notificar()" que será llamado cuando se produzca un cambio en la lista de tareas.

Implementar la interfaz o heredar de la clase base: En la clase que representa a los usuarios, implementar la interfaz o heredar de la clase base de observadores.

Registrar observadores: En la clase de la lista de tareas, proporcionar un método para registrar observadores. Esto permitirá que los usuarios se registren como observadores de la lista de tareas y reciban notificaciones.

Notificar a los observadores: Cuando se cree una nueva tarea, se actualizará la lista de tareas y se llamará al método "notificar()" en cada observador registrado. Cada usuario recibirá una notificación de la nueva tarea asignada
