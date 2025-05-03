# Principio de Segregacion de Interfaces (ISP)
El proposito de este principio es que evita las interfaces grandes porque pueden forzar la implementacion de metodos inecesarios, su tipo de principio SOLID es que esta relacionado con la cohesión y desacoplamiento (Específicamente, promueve interfaces bien definidas y separadas según uso). El problema que hay es que las funciones que se necesitan para asignar turnos estan juntas, obligando dependencias inecesarias de estas funciones, el principio, este principio lo soluciona separando las diferentes funciones en sub clases individuales para que puedan funcionar sin la dependencia de las otras funciones

### Motivacion
El problema que hay es que para asignar turnos, se necesitan que el paciente y el profesional se registren, la disponibilidad del profesional y el historial de turnos realizados, pero obliga a que el paciente dependa de estas dos funciones inecesariamente, este principio lo soluciona separando las funciones en 3 diferentes sub clases: IdentificablePaciente, IdentificableProfesional y HistorialDeTurno. Esto quedaria asi: 

![Diagrama ISP](https://github.com/user-attachments/assets/aabe0315-61f4-41db-abbf-40de245cdecb)
