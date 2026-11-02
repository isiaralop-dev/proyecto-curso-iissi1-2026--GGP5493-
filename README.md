# Título Proyecto

## Miembros del grupo LX-XXX-X (sustituir)

1. Martín Gómez, Alejandro
1. Rodríguez Galán, Sergio
1. Aragón López, Isidro
1. Apellidos, Nombre

## 1. Introducción al problema

1.1. Contexto y descripción del problema
En la actualidad, la práctica regular de ejercicio físico y entrenamiento de fuerza o muscular se ha consolidado como un pilar fundamental para la salud y el bienestar. Sin embargo, un gran número de deportistas (tanto principiantes como intermedios) se enfrentan a problemas recurrentes que afectan su constancia y progreso:

-   Falta de motivación y seguimiento estructurado: Registrar los entrenamientos en papel o notas desorganizadas impide medir de forma objetiva la progresión en cargas, series y repeticiones.
-   Ausencia de un componente social y competitivo sano: Mantener la disciplina en el gimnasio o en la rutina diaria resulta más complejo cuando no existe una comunidad o un mecanismo para comparar el rendimiento con amigos o atletas cercanos geográfica o socialmente.
-   Desbalance muscular no controlado: Es habitual trabajar más ciertos grupos musculares (ej. Pecho o Brazo) y descuidar otros (ej. Pierna o Espalda), sin contar con una representación clara del nivel real alcanzado en cada zona del cuerpo.

1.2. Situación actual y oportunidad
Muchas aplicaciones de fitness existentes son excesivamente complejas, cobran suscripciones elevadas o carecen de una gamificación basada en un sistema claro de puntos y colores por nivel de progreso muscular.
Existe una oportunidad clara de mercado para desarrollar una aplicación móvil centrada en:

-   Registrar entrenamientos diarios de forma sencilla (series, repeticiones, peso utilizado).
-   Otorgar puntuaciones diarias limitadas (evitando el sobreentrenamiento y promoviendo la competencia justa).
-   Mostrar un mapa/indicador de Progreso Muscular por rangos de color (Gris, Verde, Azul, Morado, Dorado).
-   Generar Clasificaciones (Rankings) locales y sociales (entre amigos o personas cercanas) ordenadas por puntos totales.

1.3. Clientes y Usuarios
Clientes / Stakeholders: Entidades, entrenadores o promotores del proyecto enfocados en promover un estilo de vida saludable e incentivar el deporte gamificado.

Usuarios Finales:

-   Atletas / Usuarios Deportistas: Personas de entre 15 y 70 años que realizan actividad física regular y buscan registrar sus progresos, ganar puntos y comparar su rendimiento.
-   Amigos y Comunidad: Usuarios que interactúan mediante la comparación de sus métricas y clasificaciones por puntuación.

## 2. Glosario de términos

- Términos específicos del dominio del problema, ordenados alfabéticamente. Se valorará la presencia de información multimedia.

## 3. Visión general del sistema

### 3.1. Requisitos generales
El sistema debe cumplir con las siguientes capacidades generales:

-   R.G.01. Gestión de Usuarios: Módulo encargado de gestionar la información de las cuentas e identidades de los usuarios del sistema (Clientes y Administradores), sus perfiles y los puntos acumulados.   

-   R.G.02. Gestión de Entrenamientos: Módulo encargado del registro y seguimiento diario de las sesiones de entrenamiento realizadas por los clientes.   

-   R.G.03. Gestión de Ejercicios: Módulo para administrar el catálogo de ejercicios clasificados según su grupo muscular.   

-   R.G.04. Gestión de Series de Ejercicio: Módulo para registrar las repeticiones, cargas (peso en kg) y el cálculo de puntos asociados a cada serie dentro de una sesión.   

-   R.G.05. Gestión de Clasificaciones: Módulo encargado de generar y consultar las tablas de clasificación (rankings) de usuarios según su puntuación total.   

### 3.2. Usuarios del sistema
1. Usuario Cliente:

    Usuario registrado que realiza actividad física y hace un uso activo de la aplicación. Posee los siguientes permisos y acciones principales:
    -   Registrar, editar y consultar sus entrenamientos diarios.
    -   Añadir series, repeticiones y peso por ejercicio.
    -   Visualizar su progreso muscular (puntos y color por grupo muscular).
    -   Consultar clasificaciones sociales (amigos / gente cercana).

2. Usuario No Registrado (Visitante):

    Persona que descarga la aplicación por primera vez. Posee los siguientes permisos:
    -   Crear una cuenta nueva en el sistema.
    -   Iniciar sesión con sus credenciales.

3. Administrador:

    Usuario responsable de la supervisión global de la plataforma. Posee los siguientes permisos:
    -   Gestionar el catálogo general de ejercicios y sus grupos musculares.
    -   Administrar y supervisar las cuentas de los usuarios del sistema.

4. Sistema (Proceso Automatizado):

    Componente automático que gestiona las reglas del negocio y cálculos. Posee los siguientes permisos:
    -   Validar restricciones de registro y registro de entrenamientos.
    -   Recalcular puntos obtenidos, puntos totales y el nivel de color muscular.
    -   Actualizar el ordenamiento de las clasificaciones.

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales
#### R.F.01. Consultar usuarios
Como Administrador

quiero consultar la lista de usuarios registrados

para consultar sus datos de perfil y comprobar sus puntos totales acumulados.

Prueba de aceptación:

-   Comprobar que el sistema muestra el email, nombre y los /Puntos-totales acumulados por cada usuario.   
-   Comprobar que solo los usuarios con rol Administrador tienen acceso a este listado. 

#### R.F.02. Registrar usuario
Como Usuario No Registrado

quiero crear una cuenta en la aplicación

para poder acceder al sistema y llevar el registro de mis entrenamientos.

Prueba de aceptación:

-   Comprobar que al introducir la información del registro se validen los datos requeridos (email, contraseña, nombre y fecha de nacimiento).   
-   Se debe aplicar la regla de negocio R.N.01.   
-   Se debe aplicar la regla de negocio R.N.02. 

#### R.F.03. Consultar entrenamientos
Como Cliente

quiero consultar el historial de mis entrenamientos

para visualizar el seguimiento de las sesiones realizadas.

Prueba de aceptación:

-   Comprobar que el sistema devuelve el listado de entrenamientos del cliente mostrando fecha, nombre, ubicación, duración y /PuntosTotales.   
-   Comprobar que las sesiones aparecen ordenadas cronológicamente.  

#### R.F.04. Registrar entrenamiento
Como Cliente

quiero dar de alta un nuevo entrenamiento

para registrar la actividad física de mi jornada.

Prueba de aceptación:

-   Comprobar que se guardan correctamente el nombre, fecha, ubicación y duración del entrenamiento.   
-   Se debe aplicar la regla de negocio R.N.03.   
-   Se debe aplicar la regla de negocio R.N.04.  

#### R.F.05. Consultar ejercicios
Como Cliente

quiero consultar el catálogo de ejercicios disponibles

para seleccionar los ejercicios que incluiré en mis series de entrenamiento.

Prueba de aceptación:

-   Comprobar que el sistema lista los ejercicios del catálogo mostrando su nombre y grupo muscular asociado.   
-   Comprobar que es posible filtrar la consulta por grupo muscular (Pecho, Brazo, Pierna, Espalda).  

#### R.F.06. Consultar series de ejercicio
Como Cliente

quiero consultar el desglose de series de un entrenamiento especifico

para revisar el detalle de repeticiones, cargas y puntos conseguidos en cada ejercicio.

Prueba de aceptación:

-   Comprobar que se muestran las repeticiones, el peso (kg) y los /PuntosObtenidos calculados para cada serie del entrenamiento seleccionado.

#### R.F.07. Registrar serie de ejercicio
Como Cliente

quiero añadir una serie de un ejercicio a mi entrenamiento

para contabilizar el esfuerzo técnico y la puntuación obtenida.

Prueba de aceptación:

-   Comprobar que el sistema calcula automáticamente los /PuntosObtenidos multiplicando las repeticiones por el peso (rep × peso).   
-   Se debe aplicar la regla de negocio R.N.05.   
-   Se debe aplicar la regla de negocio R.N.06.

#### R.F.08. Consultar clasificación
Como Cliente

quiero consultar la tabla de clasificación

para comparar mi rendimiento global de puntos con otros usuarios o amigos.

Prueba de aceptación:

-   Comprobar que se muestra la lista de usuarios pertenecientes al ranking o grupo seleccionado.   
-   Se debe aplicar la regla de negocio R.N.07. 

#### 4.1.1. Requisitos de información
##### R.I.01. Información de usuario
Como Administrador

quiero almacenar la información de las cuentas de los usuarios

para gestionar sus datos personales y llevar el control de su puntuación global acumulada.

Prueba de aceptación:

-   Comprobar que de cada usuario se registran los atributos: email, contraseña, nombre, fecha de nacimiento (fecha-nac) y puntos totales acumulados (/Puntos-totales).   
-   Comprobar que se mantiene la relación entre un usuario Cliente y sus múltiples ENTRENAMIENTOS.   
-   Comprobar que se mantiene la relación entre un usuario Cliente y su seguimiento de PROGRESO MUSCULAR por grupo muscular.

##### R.I.02. Información de entrenamiento
Como Administrador

quiero almacenar la información de las sesiones de entrenamiento

para mantener el registro diario de actividad de cada usuario.

Prueba de aceptación:

-   Comprobar que de cada entrenamiento se almacenan los atributos: nombre del entrenamiento, fecha, ubicación, duración y los puntos totales de la sesión (/PuntosTotales).   
-   Comprobar que cada entrenamiento pertenece obligatoriamente a un único USUARIO (Cliente).   
-   Comprobar que cada entrenamiento contiene una o varias SERIES DE EJERCICIO.   

##### R.I.03. Información de ejercicio
Como Administrador

quiero almacenar la información del catálogo de ejercicios

para clasificarlos y utilizarlos en la confección de las series de los entrenamientos.

Prueba de aceptación:

-   Comprobar que de cada ejercicio se almacenan los atributos: nombre del ejercicio y grupo muscular (GrupoMuscular: Pecho, Brazo, Pierna, Espalda).   
-   Comprobar que un ejercicio puede estar referenciado en múltiples SERIES DE EJERCICIO.   

##### R.I.04. Información de serie de ejercicio
Como Administrador

quiero almacenar la información de las series de ejercicios realizadas

para registrar la carga física y calcular la puntuación otorgada.

Prueba de aceptación:

-   Comprobar que de cada serie de ejercicio se guardan los atributos: repeticiones, peso (en kg) y los puntos calculados de la serie (/PuntosObtenidos = rep × peso).   
-   Comprobar que cada serie está asociada a un único ENTRENAMIENTO y a un único EJERCICIO.  

##### R.I.05. Información de clasificación
Como Administrador

quiero almacenar la información de las tablas de clasificación

para permitir la comparación social de puntuaciones entre usuarios.

Prueba de aceptación:

-   Comprobar que de cada clasificación se registra su nombre (ej. "Ranking General", "Amigos").   
-   Comprobar que cada clasificación incluye a un conjunto de USUARIOS ordenados según sus puntos totales acumulados.

#### 4.1.2. Reglas de negocio
##### R.N.01. Edad permitida de registro
La edad del usuario, calculada a partir de su fecha de nacimiento (fecha-nac), debe estar comprendida estrictamente entre 15 y 70 años (15 <= Edad <= 70).

##### R.N.02. Longitud mínima de contraseña
La contraseña definida por el usuario durante el registro debe contener una longitud estrictamente mayor a 8 caracteres (> 8 caracteres).

##### R.N.03. Límite diario de puntos
Un usuario de tipo cliente no puede sumar o ganar más de 20.000 puntos en un mismo día (<= 20.000 puntos/día).

##### R.N.04. Límite diario de entrenamientos
Un usuario de tipo cliente solo puede registrar como máximo 1 entrenamiento al día (<= 1 entrenamiento/día).

##### R.N.05. Frecuencia de registro de series
No se puede registrar más de una serie de un mismo ejercicio realizada en los últimos 3 días.   

##### R.N.06. Límite de incremento de peso
El peso introducido en una serie no puede superar el doble del peso máximo registrado por el usuario para ese mismo ejercicio en el último mes.

##### R.N.07. Criterio de ordenación de clasificaciones
Las clasificaciones de usuarios deben mostrarse y mantenerse ordenadas en todo momento por el valor de sus puntos totales acumulados (/PuntosTotales) de mayor a menor (orden descendente).

### 4.2. Mapa de historias de usuario (opcional)
El mapa de historias organiza las funciones de la aplicación según el camino que hace el usuario al usarla (pasos de izquierda a derecha) y las prioridades de programación (de más urgente a menos urgente):

1. Pasos de la aplicación (Eje de actividades)
#### Actividad 1: Cuenta y Perfil
-   Crear una cuenta nueva en la app (R.F.02).

-   Iniciar sesión y ver mis datos de perfil (R.F.01).

-   Validar que el usuario tenga entre 15 y 70 años (R.N.01) y la contraseña más de 8 caracteres (R.N.02).

#### Actividad 2: Registro de Entrenamientos

-   Crear un nuevo entrenamiento diario (R.F.04).

-   Ver el historial con los entrenamientos pasados (R.F.03).

-   Controlar que solo se pueda hacer 1 entreno al día (R.N.04) y un máximo de 20.000 puntos al día (R.N.03).

#### Actividad 3: Registro de Series

-   Añadir una serie con repeticiones y peso (R.F.07).

-   Ver el detalle de las series realizadas (R.F.06).

-   Calcular los puntos automáticos multiplicando repeticiones por peso.

-   Comprobar que han pasado 3 días antes de repetir el mismo ejercicio (R.N.05) y que no se ponga el doble del peso máximo del mes (R.N.06).

#### Actividad 4: Catálogo y Progreso Muscular

-   Ver el catálogo de ejercicios (R.F.05).

-   Filtrar ejercicios por grupo muscular (Pecho, Brazo, Pierna, Espalda).

-   Ver la evolución del usuario con el nivel de color según los puntos conseguidos.

#### Actividad 5: Ranking y Competición Social

-   Ver la tabla de clasificación con amigos o gente cercana (R.F.08).

-   Comprobar que la lista esté ordenada siempre de mayor a menor puntuación (R.N.07).

### ¿Cómo se organizan las entregas de la app?
#### Lo básico que tiene que funcionar ya (Fase 1):
Que el usuario se pueda registrar, iniciar sesión, crear un entrenamiento, meter las series con sus repeticiones y peso (para que calcule los puntos) y poder ver la tabla del ranking con sus amigos.   

#### Controlar que no hagan trampas (Fase 2):
Poner las reglas para que la app controle sola que nadie haga más de 1 entreno al día, que no pasen de 20.000 puntos en un día, que descansen 3 días por ejercicio y que nadie ponga el doble de peso de golpe. 

#### Ver la evolución y colores (Fase 3):
Poder buscar ejercicios por grupo muscular (Pecho, Brazo, Pierna, Espalda) y que el cuerpo del usuario cambie de color según los puntos que lleve acumulados.   

### 4.3. Requisitos no funcionales (opcional)
#### R.N.F. 01. Rendimiento en consultas de clasificación
Como Cliente

quiero que la tabla de clasificación cargue en menos de 1 segundo

para comparar mis puntos con otros usuarios sin demoras ni interrupciones.

#### R.N.F. 02. Disponibilidad del servicio
Como Cliente

quiero que la aplicación esté disponible el 99.9% del tiempo

para poder registrar mis entrenamientos en el gimnasio a cualquier hora del día.
-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


