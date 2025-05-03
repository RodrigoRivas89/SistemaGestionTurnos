# Principio de Inversion de Dependencias (DIP)
El proposito de este principio es que los modulos de alto nivel no deben depender de los de bajo nivel, sino que ambos deben depender de anstracciones, su tipo de principio SOLID es el desacoplamiento entre niveles del sistema (alto ↔ bajo nivel), el problema que hay es que para registrar a un profesional dependemos del repositorio en concreto, cualquier modificacion desecha este codigo, este principio lo soluciona creando una abstraccion para que dependa de esa abstraccion y no del repositorio

### Motivacion
El problema es que si cambiamos el repositorio de cualquier manera, nuestro codigo para registrar los datos del profesional de salud, este principio lo soluciona creando una interfaz que acople la informacion dada, asi cuando se cambie el repositorio, los datos se puedan guardar en esa interfaz, este es el ejemplo: 

![Diagrama DIP](https://github.com/user-attachments/assets/04617fd7-3e6f-4787-8baa-8145478c6067)
