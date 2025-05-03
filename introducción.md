# Anexo - Introducción al Diseño Orientado a Objetos
El paradigma orientado a objetos (POO) es un enfoque de programación que organiza el software en torno a objetos, los cuales son entidades que agrupan tanto datos como comportamientos. Los datos se representan a través de atributos (propiedades o características), y los comportamientos se modelan a través de métodos (funciones que operan sobre esos datos). El objetivo de la POO es modelar el mundo real de manera más natural y modular. En lugar de centrarse en funciones o procesos, se enfoca en los objetos y sus interacciones. Esto permite una manera más estructurada de desarrollar software, favoreciendo la reutilización, la escalabilidad y la mantenibilidad. Los fundamentos del Paradigma Orientado a Objetos son: 
1. Encapsulación: Es el proceso de ocultar la implementación interna de un objeto y exponer sólo las interfaces públicas. Esto permite que los objetos mantengan suestado interno protegido de accesos no autorizados, promoviendo así lamodularidad y la seguridad del sistema.
2. Abstracción: Consiste en simplificar la complejidad del mundo real modelando solo los aspectos esenciales relevantes para el sistema. Los objetos abstractos representan entidades del dominio de aplicación y sus interacciones, lo que facilita lacomprensión y el diseño del software.
3. Herencia: Es un mecanismo que permite que un objeto herede propiedades y comportamientos de otro objeto. Esto fomenta la reutilización del código y lacreación de jerarquías de clases, donde las clases secundarias pueden extender o modificar el comportamiento de las clases primarias.
4. Polimorfismo: Se refiere a la capacidad de los objetos de una misma jerarquía declases para responder de manera diferente a un mismo mensaje. Esto permite escribir código genérico que puede funcionar con varios tipos de objetos, promoviendo la flexibilidad y la extensibilidad del sistema.

El POO es importante por su modularidad, su reutilización de código, su escalabilidad, su mantenimiento y su facilidad de compresión

## Los cuatro fundamentos del POO

![Los cuatro fundamentos del POO](https://github.com/user-attachments/assets/bed48079-9c5d-4f7c-96bd-fca0a2b2dce0)


## Requisitos iniciales del sistema
Para que el sistema funcione se necesitará minimamente de estos 5 requisitos:
1. Registro y gestión de pacientes

El sistema debe permitir el registro de pacientes con sus datos básicos (nombre, edad, sexo, contacto, historial médico, etc.). Debe contar con la capacidad de actualizar los datos del paciente y vincularlos a los turnos programados. La gestión de pacientes debe ser eficiente para que el personal de recepción pueda acceder rápidamente a la información y a su historial médico.

2. Programación y asignación de turnos
 
 El sistema debe permitir a los usuarios (personal administrativo) asignar turnos de manera eficiente según la disponibilidad de médicos y otros profesionales de salud. Debe manejar la asignación de turnos para diferentes especialidades y tipos de consulta (consulta general, urgencias, procedimientos, etc.). Los turnos deben ser programados con horarios precisos y permitir la opción de reprogramar o cancelar turnos en caso de necesidad.
 
3. Gestión de disponibilidad de médicos y personal de salud

El sistema debe permitir ingresar y actualizar la disponibilidad de los médicos y otros profesionales de la salud (como enfermeros, psicólogos, etc.), para asignar turnos de manera adecuada. Debe permitir que los médicos puedan tener días y horarios específicos de disponibilidad, y que los turnos sean gestionados en función de esa disponibilidad.

4. Notificación y recordatorio de turnos

El sistema debe enviar notificaciones automáticas a los pacientes para recordarles los turnos programados (por ejemplo, vía SMS, correo electrónico o a través de una app). Además, debe permitir enviar notificaciones en caso de cancelaciones o cambios en los horarios.

5. Informes y estadísticas

El sistema debe generar informes detallados sobre la ocupación de turnos, la cantidad de pacientes atendidos por especialidad, tiempos de espera, etc. Debe permitir la generación de estadísticas para ayudar a los administradores del centro de salud a tomar decisiones basadas en la demanda de servicios, la eficiencia del personal y el tiempo de atención.

## Casos de uso
A continuación se mencionaran los casos de uso de los requisitos mencionados

### 1. Caso de uso: Registrar paciente

Nombre del caso de uso: Registrar paciente

Actor(es) involucrado(s): Administrador, Recepcionista

Descripción breve: Permite registrar la información básica de un nuevo paciente en el sistema.

Flujo principal de eventos:
+ El recepcionista ingresa al sistema de gestión de turnos.
+ El recepcionista selecciona la opción "Registrar paciente".
+ El sistema solicita los datos básicos del paciente (nombre, apellido, edad, sexo, número de contacto, etc.).
+ El recepcionista ingresa la información solicitada.
+ El sistema guarda la información en la base de datos y genera un identificador único para el paciente.
+ El sistema confirma que el registro se ha realizado correctamente.

Precondiciones: El recepcionista debe estar autenticado en el sistema.

Postcondiciones: El paciente queda registrado en el sistema con un identificador único, y sus datos están disponibles para la programación de turnos.

### 2. Caso de uso: Asignar turno a paciente

Nombre del caso de uso: Asignar turno a paciente

Actor(es) involucrado(s): Recepcionista, Paciente, Médico

Descripción breve: El recepcionista asigna un turno al paciente para una consulta con un médico específico.

Flujo principal de eventos:
+ El recepcionista accede al sistema de gestión de turnos.
+ El recepcionista selecciona la opción "Asignar turno".
+ El sistema muestra la lista de médicos disponibles y sus horarios.
+ El recepcionista selecciona el médico y el horario deseado.
+ El sistema muestra los turnos disponibles en ese horario y pregunta si el paciente es nuevo o ya está registrado.
+ Si el paciente es nuevo, el recepcionista registra al paciente antes de asignar el turno.
+ El recepcionista confirma la asignación del turno.
+ El sistema guarda el turno en la base de datos y envía una notificación de confirmación al paciente.

Precondiciones: El paciente debe estar registrado en el sistema, y el médico debe tener disponibilidad en el horario seleccionado.

Postcondiciones: El turno se asigna y se guarda en la base de datos, y el paciente recibe la confirmación del turno.

### 3. Caso de uso: Notificar recordatorio de turno

Nombre del caso de uso: Notificar recordatorio de turno

Actor(es) involucrado(s): Sistema, Paciente

Descripción breve: El sistema envía un recordatorio de turno al paciente para que no olvide la cita médica.

Flujo principal de eventos:
+ El sistema revisa los turnos programados para el día.
+ El sistema identifica los turnos próximos a realizarse.
+ El sistema envía una notificación por correo electrónico o SMS al paciente recordándole la cita.
+ El sistema confirma que el recordatorio ha sido enviado correctamente.

Precondiciones: El paciente debe tener un turno programado y la información de contacto debe estar correctamente registrada en el sistema.

Postcondiciones: El paciente recibe la notificación de recordatorio del turno.

### 4. Caso de uso: Cancelar turno

Nombre del caso de uso: Cancelar turno

Actor(es) involucrado(s): Paciente, Recepcionista, Sistema

Descripción breve: Permite al paciente cancelar un turno previamente asignado.

Flujo principal de eventos:
+ El paciente se comunica con el centro de salud para cancelar su turno.
+ El recepcionista accede al sistema y busca el turno del paciente.
+ El recepcionista selecciona la opción "Cancelar turno".
+ El sistema verifica que el turno existe y está dentro del rango de cancelación.
+ El sistema cancela el turno y lo elimina de la agenda del médico.
+ El sistema envía una notificación al paciente confirmando la cancelación.

Precondiciones: El paciente debe tener un turno programado y el turno debe ser cancelable (por ejemplo, no en las últimas horas previas).

Postcondiciones: El turno se cancela y se libera el espacio para otros pacientes.

### 5. Caso de uso: Generar reporte de turnos atendidos

Nombre del caso de uso: Generar reporte de turnos atendidos

Actor(es) involucrado(s): Administrador

Descripción breve: El administrador genera un informe sobre los turnos atendidos en un periodo específico.

Flujo principal de eventos:
+ El administrador ingresa al sistema de gestión de turnos.
+ El administrador selecciona la opción "Generar reporte de turnos atendidos".
+ El sistema solicita el rango de fechas para el reporte.
+ El administrador ingresa las fechas deseadas.
+ El sistema genera un reporte con la cantidad de turnos atendidos por especialidad, médico, y otros detalles.
+ El administrador descarga o visualiza el reporte generado.

Precondiciones: El administrador debe estar autenticado y tener permisos para acceder a los informes.

Postcondiciones: El reporte es generado y puesto a disposición del administrador, quien puede analizarlo para tomar decisiones

## Boceto inicial del diseño de clases

![Boceto inicial del diseño de clases](https://github.com/user-attachments/assets/5443c894-0d80-47fd-a8c4-cf86dd5ef113)
