# Sistema de Gestión de Notificaciones ( Ejercicio de Polimorfismo)

Este proyecto es una implementación en Java que demuestra los principios de la Programación Orientada a Objetos, específicamente el uso de **Herencia** y **Polimorfismo**, para gestionar diversos tipos de notificaciones universitarias.

##  Características

- **Polimorfismo**: Uso de una clase base abstracta `Notificacion` con implementaciones específicas para Email, SMS y Aplicaciones Móviles.
- **Gestión Centralizada**: Un `GestorNotificaciones` que permite agregar, listar, buscar y filtrar notificaciones de manera eficiente.
- **Tipado Fuerte**: Uso de Enums para definir tipos de notificación (Calificaciones, Pagos, Cancelaciones, etc.) y estados (Pendiente, Enviado, Fallido).
- **Extensibilidad**: Estructura diseñada para agregar fácilmente nuevos canales de notificación.

##  Tecnologías

- **Lenguaje**: Java
- **Conceptos clave**:
  - Clases Abstractas y Métodos Abstractos.
  - Sobrescritura de métodos (`@Override`).
  - Colecciones (`ArrayList`).
  - Enums y Lógica de Filtrado.

##  Ejemplo de Uso

El sistema permite crear diferentes tipos de notificaciones y procesarlas uniformemente:

```java
GestorNotificaciones gestor = new GestorNotificaciones();

// Crear una notificación de Email
NotificacionEmail email = new NotificacionEmail(
    "NOT-001", "Juan Pérez", "Mensaje...", 
    TipoNotificacion.PUBLICACION_CALIFICACIONES, 
    "Asunto", "juan@correo.com", "u@univ.edu", false
);

// Agregar y enviar
gestor.agregarNotificacion(email);
gestor.enviarTodas();
```

