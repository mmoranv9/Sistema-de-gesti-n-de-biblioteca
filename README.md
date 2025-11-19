# Informe Técnico - Sistema de Gestión de Biblioteca

##  Descripción del Caso
El sistema de gestión bibliotecaria es una aplicación web diseñada para facilitar el registro, préstamo y devolución de libros en una biblioteca pequeña o mediana.  
Su propósito principal es optimizar el control del inventario bibliográfico, mejorar la experiencia del usuario y reducir errores en los procesos administrativos.  
Se identificaron problemas como préstamos duplicados y fallos en la actualización del estado de los libros, lo que afecta la confiabilidad del sistema.

---

##  Objetivos
- Analizar problemas técnicos reales en el sistema bibliotecario.  
- Aplicar tipos de mantenimiento de software: correctivo, adaptativo, perfectivo y preventivo.  
- Proponer mejoras funcionales que aumenten la seguridad y confiabilidad del sistema.  
- Validar los cambios mediante pruebas unitarias y de integración.  

---

##  Requerimientos

### Funcionales
| Código | Descripción |
|--------|-------------|
| RF1    | Registrar nuevos libros con título, autor, año y código único. |
| RF2    | Registrar préstamos de libros a usuarios con fecha de inicio y devolución. |
| RF3    | Registrar devoluciones y actualizar el estado del libro. |
| RF4    | Mostrar listado de libros prestados y su estado actual. |
| RF5    | Consultar historial de préstamos por usuario. |

### No Funcionales
| Código | Descripción |
|--------|-------------|
| RNF1   | Autenticación mediante usuario y contraseña para funciones administrativas. |
| RNF2   | Validación automática de campos obligatorios antes de registrar información. |
| RNF3   | Copias de seguridad diarias de la base de datos. |
| RNF4   | Consultas con respuesta menor a 3 segundos. |
| RNF5   | Compatibilidad con múltiples dispositivos y sistemas operativos. |

---

##  Tabla de Pruebas

### Pruebas Unitarias
| Id     | Módulo       | Caso de prueba                     | Entrada                         | Resultado esperado            | Estado     |
|--------|--------------|------------------------------------|---------------------------------|-------------------------------|------------|
| UT-01  | Mantenimiento| Registrar mantenimiento preventivo | Tipo: Preventivo, Fecha: 04/11/2025 | Registro guardado en BD       | Realizado  |
| UT-02  | Notificación | Envío de correo al programar       | Técnico: "Admin1"               | Correo enviado correctamente  | Realizado  |
| UT-03  | Base de datos| Consulta de historial              | SELECT * FROM mantenimiento     | Lista completa mostrada       | Realizado  |
| UT-04  | Seguridad    | Acceso restringido a administradores | Usuario: lector                | Acceso denegado               | Realizado  |

### Pruebas de Validación
| Id   | Requerimiento | Escenario de prueba                  | Resultado esperado               | Evidencia              |
|------|---------------|--------------------------------------|----------------------------------|------------------------|
| V-01 | RF-07         | Registro de mantenimiento            | "Registro exitoso"               | Captura del formulario |
| V-02 | RF-08         | Consulta de historial                | Mantenimientos previos visibles | Captura del historial  |
| V-03 | RF-09         | Notificación al responsable          | Notificación generada            | Captura de correo      |
| V-04 | RF-10         | Acceso con usuario lector            | Acceso bloqueado                 | Captura de error       |

---

##  Tipos de Mantenimiento Propuesto
| Tipo         | Aplicación en el sistema | Justificación técnica |
|--------------|--------------------------|------------------------|
| Correctivo   | Corrección de errores como préstamos duplicados o fallos en devoluciones. | Soluciona defectos que afectan la lógica del sistema y la experiencia del usuario. |
| Adaptativo   | Ajustes para compatibilidad con navegadores modernos y dispositivos móviles. | Permite que el sistema se mantenga funcional ante cambios tecnológicos externos. |
| Perfectivo   | Mejora de la interfaz y optimización de tiempos de respuesta. | Incrementa la eficiencia y usabilidad del sistema sin alterar su funcionalidad principal. |
| Preventivo   | Refactorización del código y copias de seguridad automáticas. | Reduce la probabilidad de fallos futuros mediante acciones proactivas. |

---

##  Reflexión sobre el Control de Versiones
El uso de control de versiones (Git y GitHub) fue esencial para documentar los cambios realizados, facilitar la colaboración entre integrantes y mantener un historial claro de modificaciones.  
Permite revertir errores, validar mejoras y asegurar la trazabilidad del mantenimiento aplicado.  
Además, fortalece la calidad del desarrollo al integrar pruebas, documentación y propuestas funcionales en un entorno controlado y accesible.
