# Principio de Abierto/Cerrado (OCP)
El proposito de esta clase es que debe de estar abierta a la extension, pero cerrada a la modificacion, su tipo de principio SOLID es que esta relacionado con la extensibilidad y la estabilidad del código. El problema que hay es que la clase GestorDeTurnos solo registra a un paciente, pero quiero que tambien registre al doctor que va a atender al paciente, este principio lo soluciona integrando ambas funciones sin modificar su uso principal

### Motivacion
El problema que hay es que la clase de GestorDeTurnos solo hace una funcionalidad, y esa es la de registrar a un paciente, pero yo quiero añadirle que tambien registre el doctor que va a atender el paciente asi hay una mejor interaccion entre los dos, pero no quiero modificar tanto el codigo para no estropiarlo, el OCP lo soluciona extendiendo la clase de GestorDeTurnos, teniendo tanto la funcionalidad de registrar la paciente como la de registrar al doctor que va a atender al paciente, esto quedaria asi:

![Diagrama OCP](https://github.com/user-attachments/assets/158021cf-3410-40f2-8886-53435bdd6273)
