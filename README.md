# Sistemas-Check-in-TSJ
Sistema web de control de asistencia con integración biométrica, gestión de personal, gestión multi-sede, roles de usuario y cálculo automatizado de nómina.
## Sobre el proyecto

Este proyecto fue desarrollado en el contexto de mis pasantías profesionales en el Tribunal Supremo de Justicia (TSJ), como propuesta de modernización del proceso de registro de asistencia.
Durante las pasantías identifiqué la oportunidad de mejorar un proceso que dependía de un sistema de control biométrico antiguo. A partir de esta necesidad, trabajé en el desarrollo de una aplicación web para centralizar la gestión del personal y las asistencias, incorporando control de acceso por roles e integración con un lector de huellas dactilares.

## Objetivos

- Facilitar el registro de entradas y salidas del personal.
- Centralizar la información de asistencia y puntualidad.
- Organizar la administración del personal por sedes.
- Controlar el acceso a las funcionalidades según el rol del usuario.
- Generar reportes que permitan consultar y analizar los registros de asistencia.

## Tecnologías utilizadas

- **PHP:** lógica del servidor y backend.
- **MySQL:** almacenamiento y gestión de datos.
- **Java:** puente de integración con el SDK biométrico.
- **JavaScript:** interactividad de la interfaz.
- **AJAX y JSON:** comunicación e intercambio de datos entre componentes.
- **HTML y CSS:** estructura y presentación de la aplicación.
- **Bootstrap:** diseño de la interfaz adaptable.
- **SDK Futronic:** integración con el lector de huellas dactilares.

## Funcionalidades principales

### 1. Login.
antalla de autenticación para acceder al sistema mediante credenciales de usuario. El acceso a las funcionalidades está sujeto al rol y los permisos asignados a cada cuenta.


<p align="center">
<img width="600"  alt="imagen de login" src="https://github.com/user-attachments/assets/b040ebf7-e3e6-4144-aa6b-2fc062bda2ec" />
</p>


### 1. Panel principal y estadísticas

Dashboard con información de asistencia y gráficos para consultar la puntualidad del personal por períodos diarios, semanales y mensuales. Que permite visualizar información relacionada con el control de asistencia del personal. La interfaz y las opciones disponibles varían según el rol del usuario, de acuerdo con sus responsabilidades y permisos de acceso.

La gestión multisede permite administrar la información de distintas sedes, manteniendo restricciones de acceso según el nivel de autorización de cada usuario:
-Administrador global (admin_global): dispone de opciones de gestión con alcance multisede.

-Administrador de sede (admin_sede): accede a las opciones autorizadas para administrar su propia sede.

-División Personal (Recursos Humanos): dispone de un menú más limitado, con acceso a Inicio, Empleados, Asistencias y Check-in de su sede correspondiente.

## Dashboard según el rol de usuario

El dashboard presenta información y funcionalidades según el rol
y el alcance de acceso de cada usuario.


<table>
  <tr>
    <th align="center">Administrador global</th>
    <th align="center">Administrador de sede</th>
    <th align="center">División Personal</th>
  </tr>
  <tr>
    <td align="center">
      <img width="600" alt="Administrador global" src="https://github.com/user-attachments/assets/77624983-6e6d-4e4c-96d4-1a8f8328988e">
    </td>
    <td align="center">
      <img width="600" alt="Administrador de sede" src="https://github.com/user-attachments/assets/c2a8d6e4-5b48-454a-8ab2-e1dfb784ca7c">
    </td>
    <td align="center">
      <img width="280" alt="División Personal" src="https://github.com/user-attachments/assets/5a5fd4aa-992a-46dc-8d75-a6e9f8cbd8c3" />
    </td>
  </tr>
  <tr>
    <td align="center">Vista de alcance multisede.</td>
    <td align="center">Información correspondiente a su sede.</td>
    <td align="center">Panel con las funcionalidades autorizadas para su rol.</td>
  </tr>
</table>



### 2. Gestión de empleados

Módulo para consultar y administrar la información del personal, con opciones de registro y edición.


<table>
  <tr>
    <th align="center">Administrador global</th>
    <th align="center">Administrador de sede</th>
  </tr>
  <tr>
    <td align="center">
      <img width="420" alt="Dashboard del administrador global"
      src="https://github.com/user-attachments/assets/1b260727-941b-47fb-82e2-f63c6b7c5ec3" />
    </td>
    <td align="center">
      <img width="420" alt="Dashboard del administrador de sede"
      src="https://github.com/user-attachments/assets/ab903185-b19c-47a9-8010-16f7ca61044f" />
    </td>
  </tr>
</table>


### 3. Control de asistencia

Consulta de los registros de entrada y salida del personal, con información organizada para facilitar el seguimiento de las asistencias.

<!-- Agregar captura real de asistencias -->
![Registro de asistencias](docs/screenshots/asistencias.png)

### 4. Check-in biométrico

Módulo destinado al registro de asistencia mediante huella dactilar.

La integración se diseñó utilizando el SDK de Futronic y un puente desarrollado en Java para comunicar el componente biométrico con el backend PHP.

El módulo contempla también una alternativa de registro manual por número de cédula, restringida a los usuarios administradores autorizados, para los casos en que un empleado presente dificultades con su huella.

<!-- Agregar captura real del módulo de check-in -->
![Módulo de check-in](docs/screenshots/checkin.png)

### 5. Control de puntualidad

El sistema contempla una regla de control de tardanzas mensuales. Al alcanzar el límite configurado, el usuario puede quedar bloqueado y debe acudir a Recursos Humanos para justificar su impuntualidad.

### 6. Gestión de cargos

Administración de los cargos asociados a la organización del personal.

<!-- Agregar captura real de cargos -->
![Gestión de cargos](docs/screenshots/cargos.png)

### 7. Gestión de áreas y ubicaciones

Módulo para administrar áreas y ubicaciones, con herramientas de búsqueda y opciones de exportación de información a Excel o PDF, según las funcionalidades disponibles.

<!-- Agregar captura real de áreas -->
![Gestión de áreas y ubicaciones](docs/screenshots/areas.png)

### 8. Gestión de usuarios y permisos

Administración de las cuentas de acceso y aplicación de restricciones según el rol y la sede correspondiente.

El sistema contempla tres perfiles principales:

| Rol | Alcance |
|---|---|
| Administrador global | Acceso administrativo a la información de todas las sedes. |
| Administrador de sede | Acceso a las funciones e información autorizadas de su sede. |
| División de Personal | Acceso a las funciones de personal autorizadas para su sede. |

La interfaz y las opciones disponibles varían según los permisos asignados a cada perfil.

<!-- Agregar captura real de usuarios y roles -->
![Gestión de usuarios](docs/screenshots/usuarios.png)

### 9. Reportes

Módulo de consulta de información de asistencia, orientado al seguimiento de registros y puntualidad, con información limitada según los permisos del usuario.

<!-- Agregar captura real de reportes -->
![Reportes de asistencia](docs/screenshots/reportes.png)

## Arquitectura general

El sistema utiliza una aplicación web desarrollada en PHP y una base de datos MySQL. Para la integración biométrica, se contempla un componente Java que comunica el backend con el SDK de Futronic.

Flujo general de la integración:

1. La interfaz web solicita una operación de registro o identificación.
2. El componente de integración se comunica con el lector biométrico.
3. El resultado de la operación se procesa mediante la lógica de la aplicación.
4. Los registros correspondientes se gestionan en la base de datos.

*
Proyecto desarrollado en el contexto de pasantías profesionales. La disponibilidad de algunas funciones, especialmente la integración con el lector biométrico, depende del hardware y del entorno de ejecución.

Las capturas utilizadas como maquetas o demostraciones visuales deben distinguirse de las pruebas funcionales realizadas con el dispositivo real.

## Aprendizajes

Este proyecto me permitió trabajar con:

- Desarrollo de aplicaciones web con PHP y MySQL.
- Integración entre tecnologías de software y hardware biométrico.
- Diseño de funcionalidades de administración por roles y sedes.
- Gestión de información de empleados y registros de asistencia.
- Análisis de procesos existentes y diseño de una solución tecnológica.
