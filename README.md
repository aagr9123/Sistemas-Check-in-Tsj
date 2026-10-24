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

**-Administrador global (admin_global):** dispone de opciones de gestión con alcance multisede.

**-Administrador de sede (admin_sede):** accede a las opciones autorizadas para administrar su propia sede.

**-División Personal (Recursos Humanos):** dispone de un menú más limitado, con acceso a Inicio, Empleados, Asistencias y Check-in de su sede correspondiente.

## Dashboard según el rol de usuario.

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
      <img width="100%" alt="Administrador global" src="https://github.com/user-attachments/assets/77624983-6e6d-4e4c-96d4-1a8f8328988e">
    </td>
    <td align="center">
      <img width="100%" alt="Administrador de sede" src="https://github.com/user-attachments/assets/c2a8d6e4-5b48-454a-8ab2-e1dfb784ca7c">
    </td>
    <td align="center">
      <img width="100%" alt="División Personal" src="https://github.com/user-attachments/assets/5a5fd4aa-992a-46dc-8d75-a6e9f8cbd8c3" />
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
      <img width="100%" alt="Dashboard del administrador global"
      src="https://github.com/user-attachments/assets/1b260727-941b-47fb-82e2-f63c6b7c5ec3" />
    </td>
    <td align="center">
      <img width="100%" alt="Dashboard del administrador de sede"
      src="https://github.com/user-attachments/assets/ab903185-b19c-47a9-8010-16f7ca61044f" />
    </td>
  </tr>
</table>

### Agregar empleados:

<table>
  <tr>
    <td align="center">
      <strong>Datos Personales</strong><br>
      <img src="https://github.com/user-attachments/assets/af91d985-78a0-4aa9-99b3-c4444d8ec7cc" width="100%">
    </td>
    <td align="center">
      <strong>Datos Laborales</strong><br>
      <img src="https://github.com/user-attachments/assets/9c8343c4-f07a-42d4-9c9a-051894ae0d3c" width="100%">
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>Sueldos</strong><br>
      <img src="https://github.com/user-attachments/assets/d1d55dea-4fe7-4418-8ba7-a3472ebd2c28" width="100%">
    </td>
    <td align="center">
      <strong>Foto</strong><br>
      <img src="https://github.com/user-attachments/assets/f3b3fc3c-1481-4216-9ac3-19da76e8fb83" width="100%">
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong> Huella</strong><br>
      <img src="https://github.com/user-attachments/assets/4ccb76de-a5eb-477d-a124-819b294f5f73"  width="100%">
    </td>
    <td></td>
  </tr>
</table>

### Ver/Editar empleados:

Se puede ver y editar en el mismo campo:

<table>
  <tr>
    <td align="center">
      <strong>Modo Vista </strong><br>
      <img src="https://github.com/user-attachments/assets/1ce0a4f2-2a67-4acc-ae3d-d22d2d5f3531" width="100%">
    </td>
    <td align="center">
      <strong>Modo Edición</strong><br>
      <img src="https://github.com/user-attachments/assets/f8a09710-2521-4a4f-bcc6-491e61f115ee" width="100%">
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>Modo Edición</strong><br>
      <img src="https://github.com/user-attachments/assets/8d5cf82b-99a2-400e-9c17-0444434340f0"  width="100%">
    </td>
   
</table>

### 3. Control de asistencia

Consulta de los registros de entrada y salida del personal, fecha y hora, la hora esperada según el horario del cargo, hora de retraso, horas trabajadas, con información organizada para facilitar el seguimiento de las asistencias.

<table>
  <tr>
    <th align="center">Administrador global</th>
    <th align="center">Administrador de sede</th>
  </tr>
  <tr>
    <td align="center">
      <img width="100%" alt="Administrador global"
      src="https://github.com/user-attachments/assets/54a153a3-6d01-43f2-874f-2d71dff41f56" />
    </td>
    <td align="center">
      <img width="100%" alt="Administrador de sede"
      src="https://github.com/user-attachments/assets/adfe8836-4f90-48bb-a28b-677ebeb3a437" />
    </td>
  </tr>
</table>
Admin global cuenta con su filtro de sede para seleccionar el rendimiento de la sede que se desee auditar.

### 4. Check-in biométrico

Módulo destinado al registro de asistencia mediante huella dactilar.

La integración se diseñó utilizando el SDK de Futronic y un puente desarrollado en Java para comunicar el componente biométrico con el backend PHP.

El módulo contempla también una alternativa de registro manual por número de cédula, restringida a los usuarios administradores autorizados, para los casos en que un empleado presente dificultades con su huella.

<table>
  <tr>
    <th align="center">Usuario Promedio</th>
    <th align="center">Administrador de sede y Global</th>
  </tr>
  <tr>
    <td align="center">
      <img width="100%" alt="Usuario Promedio"
      src="https://github.com/user-attachments/assets/8490cc1d-b9a5-4dcb-909f-1bfe35bae135" /> </td>
    <td align="center">
      <img width="100%" alt="Administradores"
      src="https://github.com/user-attachments/assets/79002b6d-cdcf-48b7-b9f4-580d335bc2de"/> </td>
  </tr>
</table>

### 5. Control de puntualidad

El sistema aplica una regla de control de tardanzas con un límite de 3 tardanzas mensuales. Cada vez que se registra una tardanza, el empleado recibe una notificación de advertencia.

Al alcanzar el límite establecido, el usuario queda bloqueado y debe acudir a Recursos Humanos para justificar su impuntualidad. En ese momento, se habilita el botón Desbloquear, que permite restablecer el contador de tardanzas para iniciar un nuevo seguimiento.
<table>
  <tr>
    <th align="center">Contador de Tardanzas</th>
    <th align="center">Notificación de advertencia: límite alcanzado</th>
    <th align="center">Boton de Desbloqueo</th>
  </tr>
  <tr>
    <td align="center">
      <img width="100%" alt="Contador de Tardanzas" src="https://github.com/user-attachments/assets/ee159d54-525a-4147-b932-5c9e8f8be947">
    </td>
    <td align="center">
      <img width="100%" alt="Notificacion de Advertencia" src="https://github.com/user-attachments/assets/3e56a472-8166-471d-96bd-4219e894e0e2" />
    </td>
    <td align="center">
      <img width="600" alt="Boton de Desbloqueo" src="https://github.com/user-attachments/assets/1d0806bc-5d9b-4eb7-bf43-8b9d03889e73" />
    </td>
  </tr>

</table>


### 6. Gestión de cargos

Administración de los cargos asociados a la organización del personal, junto con su su horario.
<table>
  <tr>
    <th align="center">Vista previa</th>
    <th align="center">Agregar</th>
    <th align="center">Editar</th>
  </tr>
  <tr>
    <td align="center" valign="top">
      <img width="100%" alt="Vista previa"
      src="https://github.com/user-attachments/assets/31e7c46f-a28a-4747-b472-e16364bc9278">
    </td>
    <td align="center" valign="top">
      <img width="100%" alt="Agregar"
      src="https://github.com/user-attachments/assets/b6629ad3-5d3e-4086-9306-334bab1da253"/>
   </td>
    <td align="center" valign="top">
      <img width="100%" alt="Editar"
     src="https://github.com/user-attachments/assets/68d01daf-b107-430e-8b08-da4ae5da3304" />
    </td>
  </tr>
</table>

### 7. Gestión de áreas y ubicaciones.

Módulo para administrar áreas (Sedes) y ubicaciones (Administraciones y Fisicas), con herramientas de búsqueda y opciones de exportación de información a Excel o PDF, según las funcionalidades disponibles.
<table>
  <tr>
    <th align="center">Administrador global</th>
    <th align="center">Administrador de sede</th>
  </tr>
  <tr>
    <td align="center">
      <img width="100%" alt="Administrador global"
   src="https://github.com/user-attachments/assets/f649069e-50fd-4cf5-aa1c-41faa62a0fd6" />
    </td>
    <td align="center">
      <img width="100%" alt="Administrador de sede" 
        src="https://github.com/user-attachments/assets/bcb5f40c-eabd-42b6-9367-3d6c81b7fcef" />
    </td>
  </tr>
</table>

### 8. Gestión de usuarios y permisos

Administración de las cuentas de acceso y aplicación de restricciones según el rol y la sede correspondiente.

El sistema contempla tres perfiles principales:

| Rol | Alcance |
|---|---|
| Administrador global | Acceso administrativo a la información de todas las sedes. |
| Administrador de sede | Acceso a las funciones e información autorizadas de su sede. |
| División de Personal | Acceso a las funciones de personal autorizadas para su sede. |

La interfaz y las opciones disponibles varían según los permisos asignados a cada perfil.
<table>
  <tr>
    <th align="center">Administrador global</th>
    <th align="center">Administrador de sede</th>
  </tr>
  <tr>
    <td align="center">
      <img width="100%" alt="Administrador global"
   src="https://github.com/user-attachments/assets/1f1e4361-6d22-4c02-aa41-cfb9f0faf7b4" />
    </td>
    <td align="center">
      <img width="100%" alt="Administrador de sede" 
       alt="imagen" src="https://github.com/user-attachments/assets/c4b09f1d-80c1-4702-b1cb-0e5d32282747" />
    </td>
  </tr>
</table>

### 9. Reportes
Permite consultar el historial de acciones realizadas por los usuarios dentro del sistema, como el registro, la edición y la eliminación de información. Los datos que puede visualizar cada usuario dependen de su rol y de los permisos asignados.
<table>
  <tr>
    <th align="center">Administrador global</th>
    <th align="center">Administrador de sede</th>
  </tr>
  <tr>
    <td align="center">
      <img width="100%" alt="Administrador global"
 src="https://github.com/user-attachments/assets/e2035ba7-6e0c-4686-a3e6-46744ed279ab" />
    </td>
    <td align="center">
      <img width="100%" alt="Administrador de sede" 
        src="https://github.com/user-attachments/assets/750ae4ec-ec7c-4f44-826d-70d9eac06938" />
    </td>
  </tr>
</table>

## Arquitectura general

El sistema utiliza una aplicación web desarrollada en PHP y una base de datos MySQL. Para la integración biométrica, se contempla un componente Java que comunica el backend con el SDK de Futronic.
Flujo general de la integración:
1. La interfaz web solicita una operación de registro o identificación.
2. El componente de integración se comunica con el lector biométrico.
3. El resultado de la operación se procesa mediante la lógica de la aplicación.
4. Los registros correspondientes se gestionan en la base de datos.

Proyecto desarrollado en el contexto de pasantías profesionales. La disponibilidad de algunas funciones, especialmente la integración con el lector biométrico, depende del hardware y del entorno de ejecución.
## Aprendizajes
Este proyecto me permitió trabajar con:
- Desarrollo de aplicaciones web con PHP y MySQL.
- Integración entre tecnologías de software y hardware biométrico.
- Diseño de funcionalidades de administración por roles y sedes.
- Gestión de información de empleados y registros de asistencia.
- Análisis de procesos existentes y diseño de una solución tecnológica.
