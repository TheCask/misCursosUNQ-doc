![Logo](https://github.com/TheCask/misCursosUNQ-doc/blob/master/logoApp.png)
# misCursosUNQ Documentation repository
---
---
[**Repositories**](https://github.com/TheCask)
| Link | Travis | JaCoCo | Codacy | Licence |
| ------ | ------ | ------ | ------ | ------ |
| [Backend](https://github.com/TheCask/misCursosUNQ-back.git) | [![Build Status](https://travis-ci.org/TheCask/misCursosUNQ-back.svg?branch=master)](https://travis-ci.org/TheCask/misCursosUNQ-back) | [![Codacy Badge](https://app.codacy.com/project/badge/Coverage/5f7776931f374604b1b9ea41243ceb0f)](https://www.codacy.com/manual/TheCask/misCursosUNQ-back?utm_source=github.com&utm_medium=referral&utm_content=TheCask/misCursosUNQ-back&utm_campaign=Badge_Coverage) | [![Codacy Badge](https://app.codacy.com/project/badge/Grade/5f7776931f374604b1b9ea41243ceb0f)](https://www.codacy.com/manual/TheCask/misCursosUNQ-back?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=TheCask/misCursosUNQ-back&amp;utm_campaign=Badge_Grade) | [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) |
| [Frontend](https://github.com/TheCask/misCursosUNQ-front.git) | | | | [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) |
| [Docs](https://github.com/TheCask/misCursosUNQ-doc.git) | | | | [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) |
---
[**Backlog**](https://trello.com/invite/b/tBtNOQyX/079461fa54dd03f45fec964b3543d726/miscursosunq)

[**Wiki**](https://github.com/TheCask/misCursosUNQ-doc/wiki)

---
- **Group**: 14
- **Members**: Elías Filipponi y Eugenio Cálcena
- **General Goal**: Se plantea construir un sistema de gestión de cursos y evaluaciones para el ciclo introductorio de ciencia y tecnología (CI-CYT) de la Universidad Nacional de Quilmes (UNQ).
- **License**: GNU GPL 3
- **Development process**: Iterativo (MVP mínimo y suma de funcionalidades)
---
## Architecture
- **Type**: Web client - server.
- **Technologies**: MySQL - Hibernate - Java - Spring - ReactJS
![Architecture](https://github.com/TheCask/misCursosUNQ-doc/blob/master/Architecture.png)
Se plantea una arquitectura de tipo cliente servidor. Del lado del Frontend se utilizará REACT dividiendo el proyecto en componentes que manejan lógica y renderizan una parte de pequeña de cada pantalla. Estos se conectaran entre si y a su vez delegaran la comunicación con el backend a servicios API para envío y recepción de información. Del lado del Backend se utilizarán controllers que manejan request y reponses REST, delegando en services especiales la lógica previa y posterior a la comunicación con los repos para la persistencia de la información. Los repos son manejados por Hibernate mediante configuraciones en el dominio mediante anotations, evitando el acceso directo a la base de datos mysql. El dominio escrito en JAVA contempla la lógica de negocio y encapsulamiento apropiado de la información.
---
## Milestones Github
| Fecha | Backend | Frontend | Documents |
| ------ | ------ | ------ | ------ |
| 25/04/2020 | [Prueba de Concepto](https://github.com/TheCask/misCursosUNQ-back/milestone/2) | [Prueba de Concepto](https://github.com/TheCask/misCursosUNQ-front/milestone/1) | [Prueba de Concepto](https://github.com/TheCask/misCursosUNQ-doc/milestone/5) |
| 09/05/2020 | [Entrega 1](https://github.com/TheCask/misCursosUNQ-back/milestone/3) | [Entrega 1](https://github.com/TheCask/misCursosUNQ-front/milestone/2) |[Entrega 1](https://github.com/TheCask/misCursosUNQ-doc/milestone/1)|
| 23/05/2020 | [Entrega 2](https://github.com/TheCask/misCursosUNQ-back/milestone/4) | [Entrega 2](https://github.com/TheCask/misCursosUNQ-front/milestone/3) | [Entrega 2](https://github.com/TheCask/misCursosUNQ-doc/milestone/2) |
| 13/06/2020 | [Entrega 3](https://github.com/TheCask/misCursosUNQ-back/milestone/5) | [Entrega 3](https://github.com/TheCask/misCursosUNQ-front/milestone/4) |[Entrega 3](https://github.com/TheCask/misCursosUNQ-doc/milestone/3)|
| 04/07/2020 | [Entrega 4](https://github.com/TheCask/misCursosUNQ-back/milestone/6) | [Entrega 4](https://github.com/TheCask/misCursosUNQ-front/milestone/5) | [Entrega 4](https://github.com/TheCask/misCursosUNQ-doc/milestone/4)|
| TBD | [Presentación final](https://github.com/TheCask/misCursosUNQ-back/milestone/7) | [Presentación final](https://github.com/TheCask/misCursosUNQ-front/milestone/6) | [Presentación final](https://github.com/TheCask/misCursosUNQ-doc/milestone/6) |
---
## Sobre el Producto
### Usuarios
Serán docentes y coordinadores/as del CI-CYT. Se puede plantear a futuro el uso por parte de estudiantes para acceder a información sobre sus cursadas (módulo no planteado en MVP).
### Objetivo
El objetivo principal es centralizar la información sobre los cursos del CI - CYT de forma que lxs docentes puedan gestionar diferentes aspectos de estos. Al mismo tiempo se pretende que lxs distintos coordinadores/as de asignaturas y general del CI-CYT pueden utilizar esta información para gestionar aspectos relevantes a la toma de decisiones académicas y administrativas relativas al CI-CYT.
### Módulos
En una primer etapa se pretende la implementación de los siguientes módulos:
- Carga y consulta de información sobre estudiantes.
- Carga y consulta de información sobre asignaturas y cursadas.
- Carga y consulta de información sobre docentes y coordinadores.

Se plantean como posibles módulos a futuro:
- Carga y consulta de información sobre evaluaciones.
- Importación de datos a partir de formatos de marcado (CSV).
### Proceso
El proceso general contempla la creación de lxs usuarixs del sistema, en este caso docentes y coordinadores/as, para que luego ellxs puedan crear y cargar los datos de las distintas cursadas (asignatura, lista de estudiantes, etc.). Se plantea que ambos procesos puedan realizarse de forma manual a través de una interfaz web tipo formulario.
El ingreso al sistema debe contemplar distintos roles con distintos permisos de acceso, cada docente solo podrá ver/editar información sobre los cursos a su cargo, mientras que coordinadores podrán análogamente ver información de todos los cursos de una misma asignatura, mientras que la coordinación general tendrá acceso a todas las cursadas.
Se contempla la posibilidad de logueo al sistema mediante autenticación con cuentas de google.
### Modelo de dominio
![UML](https://github.com/TheCask/misCursosUNQ-doc/blob/master/misCursosUNQ%20Domain.png)
### Objetos Pricipales
![Objects](https://github.com/TheCask/misCursosUNQ-doc/blob/master/Pricipal%20Objects.png)

El objeto central del modelo es la cursada, que corresponde a el dictado de una asignatura en un determinado cuatrimestre, estará compuesta por estudiantes que la cursan y docente/s que la dicta/n. Además se contará con la figura de coordinador de asignatura, que podrá gestionar todas las cursadas de una misma asignatura y coordinador/a de ciclo que se con alcance análogo para todo el CI-CYT. 
El coordinador de ciclo estará a cargo de gestionar la creación de asignaturas y el agregado de lxs coordinadores/as, as su vez estxs gestionarán la creación de cursos y el agregado de docentes. Lxs docentes gestionarán la alta de estudiantes en sus cursos.
### Casos de uso
Lineamientos generales de los casos de uso:
- Un administrador crea materia y coordinadores, y los asocian según corresponda. Reúne todos los permisos que un coordinador o un docente para todas las asignaturas.
- Los coordinadores crean cursadas y docentes, y los asocian según corresponda. Reúne todos los permisos de los docentes a su cargo.
- Los docentes crean alumnos en las cursadas a su cargo, crean clases y registran asistencia para sus cursadas, y crean instancias evaluatorias y registran las calificaciones de sus alumnos para cada instancia. 

![Use Cases](https://github.com/TheCask/misCursosUNQ-doc/blob/master/Use%20Cases/Diagrama%20de%20caso%20de%20uso_Entrega3.png)
