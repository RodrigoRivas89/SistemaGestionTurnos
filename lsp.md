# Principio de Sustitucion de Liskov (LSP)
El proposito de este principio es que los objetos de una subclase deban poder remplazar a los objetos de su superclase sin alterar el programa, su tipo de principio solid es que que esta relacionado con la herencia, el polimorfismo y el reemplazo seguro de clases. El problema que hay es el enviar un recordatorio al paciente unicamente por email, pero el paciente solo tiene sms, este principio lo soluciona creando dos subclases de recordatorio para asi poder enviar los recordatorios sin problemas

### Motivacion
El problema que hay es que el recordatorio de turnos se envia unicamente a los emails de los pacientes, pero hay un paciente que no tiene email, por lo que no le va a llegar el recordatorio, pero si tiene sms, este principio lo soluciona creando dos subclases de la clase RecordatorioDeTurnos, denominados RecordatorioEmail y RecordatorioSMS respectivamente, logrando que tanto los que tengan emails y sms reciban los recordatorios, la implementacion de esto seria asi:

![Diagrama LSP](https://github.com/user-attachments/assets/6aff76f3-9829-4875-ba7c-64649188e095)
