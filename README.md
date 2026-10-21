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

1. Gestión de Cuentas e Identidad:

    -   Permitir el registro de usuarios verificando los criterios de edad permitida (entre 15 y 70 años) y requisitos de seguridad en contraseñas.
    -   Mantener el perfil del usuario actualizado con su puntuación global acumulada.

2. Registro y Control de Entrenamientos:

    -   Registrar cada entrenamiento diario capturando fecha, ubicación y duración.
    -   Controlar que los entrenamientos cumplan con las restricciones de negocio (ej. límites en la duración de la sesión y tope de puntos diarios otorgados para evitar trampas o sobreentrenamiento).
    -   Permitir desglosar el entrenamiento en ejercicios específicos con sus correspondientes series, repeticiones y peso (en kg).

3.  Gamificación y Nivel de Progreso Muscular:

    -   Calcular de forma automatizada los puntos acumulados por grupo muscular (Pecho, Brazo, Espalda, Pierna).
    -   Asignar dinámicamente un nivel de color basado en los puntos alcanzados en cada grupo muscular:
        Gris: 0 – 99 puntos
        Verde: 100 – 299 puntos
        Azul: 300 – 599 puntos
        Morado: 600 – 999 puntos
        Dorado: +1000 puntos

4.  Clasificación Social y Comparación:

    -   Generar tablas de clasificación (rankings) compuestas por grupos de usuarios (amigos o usuarios cercanos por ubicación).
    -   Ordenar automáticamente las clasificaciones en función de los puntos totales acumulados de mayor a menor.

### 3.2. Usuarios del sistema
1. Usuario Deportista (Atleta):

    Usuario registrado que realiza actividad física y hace uso activo de la aplicación. Posee los siguientes permisos:
    -   Registrar, editar y consultar sus entrenamientos diarios.
    -   Añadir series, repeticiones y peso por ejercicio.
    -   Visualizar su progreso muscular (puntos y color por grupo muscular).
    -   Consultar clasificaciones sociales (amigos / gente cercana).

2. Usuario No Registrado (Visitante):

    Persona que descarga la aplicación por primera vez. Posee los siguientes permisos:
    -   Crear una cuenta nueva en el sistema.
    -   Iniciar sesión con sus credenciales.

3. Sistema (Proceso Automatizado):

    Componente automático que gestiona las reglas del negocio y cálculos. Posee los siguientes permisos:
    -   Validar restricciones de registro y registro de entrenamientos.
    -   Recalcular puntos obtenidos, puntos totales y el nivel de color muscular.
    -   Actualizar el ordenamiento de las clasificaciones.

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

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


