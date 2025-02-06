# <center><u> Proyecto Final DAMV 2º</center></u>

## Wakkey ⏰
<img src="durmiendo.png" with="100" height="100">

## Table of Contents 📄
1. [Información General](#información-general-ℹ️)
2. [Cracterísticas](#características-✨)
3. [Tecnologías](#tecnologías-🖥️)
4. [Instalación](#instalación-🔧)
5. [Uso](#uso-📱)
6. [Preguntas Frecuentes](#preguntas-frecuentes-❓)



## <span style="color:blue;">1. Información General ℹ️</span>
Wakkey es una aplicación móvil pensada para personas a la que les cuesta despertarse con una simple alarma. 
Debes completar el mini-juego que te aparecerá en pantalla para descativar la alarma, ¡si no lo consigues seguirá sonando!
Wakkey incluye cronómetro y un temporizador.
Configura tu alarma y al despertar completa el mini-juego que más te llame la atención.
<center>¡Descárgalo ya!</center>
<br>
> "El sueño es un arte poético involuntario." 
Friedrich Nietzsche 

## 2. Cracterísticas ✨

✅ *Configura múltiples alarmas con sonidos personalizados.*

✅ *Mini juegos para desactivar la alarma.* 

✅ *Interfaz intuitiva y fácil de usar.*

✅ *Modo oscuro y claro.*


| Nombre   | Descripción                                | Estado  |
|----------|------------------------------------------|---------|
| Wakkey   | Aplicación de alarma con juego          | En desarrollo |
| Plataforma | Android                              | Planeado |
| Método de apagado | Resolver un juego o desafío   | Implementado |
| Notificaciones | Recordatorios y alertas           | Pendiente |
| Personalización | Sonidos y niveles de dificultad  | En progreso |


### <u>Ejemplos de juegos 🎮</u>

[Ejemplo de juego](https://www.youtube.com/watch?v=9hOJH7IflFo&pp=ygUqYW5kcm9pZCBzdHVkaW8ga290bGluIGNyZWFjaW9uIGRlIHVuIGp1ZWdv "Tic Tac Toe")
[![Ver en YouTube](https://img.youtube.com/vi/LBRrW08_P8c/maxresdefault.jpg)](https://www.youtube.com/watch?v=LBRrW08_P8c&list=PLhcYacorV7U6HHVsfXnWodwEPI0E38BXD&ab_channel=DinoCode-Tutoriales)


## 3. Tecnologías 🖥️
Las tecnologías usadas para este programa han sido:
- **Kotlin**: Lenguaje principal de la aplicación.
- **SQLite**: Almacenamiento de datos y configuraciones, ya que esta aplicación no requiere un almacenamiento de gran volumen.
 
## 4. Instalación 🔧
Para instalar la aplicación, sigue estos pasos:
1. Clona el repositorio: ```git clone https://github.com/Leczzz/Wakkey.git```
![GitHub followers](https://img.shields.io/github/followers/Leczzz?style=social)
2. Abre el proyecto en Android Studio.
3. Compila y ejecuta la aplicación en un emulador o dispositivo físico.

## 5. Uso 📱
1. Abre la aplicación.
2. Configura tu alarma junto con el mini-juego que quieras completar una vez llegue a sonar.
3. Al sonar la alarma, completa el mini-juego para desactivarla.
4. Utiliza el cronómetro y el temporizador según tus necesidades.

## 6. Preguntas Frecuentes ❓
***¿Cómo configuro una alarma?***

- Abre la aplicación, selecciona la opción de configurar alarma, elige la hora y el mini-juego a completar y guarda la configuración.

***¿Qué pasa si no completo el mini-juego?***
- La alarma seguirá sonando hasta que completes el mini-juego.

***¿Puedo usar mi propia música como alarma?***
- Actualmente, esta funcionalidad no está disponible, pero estamos trabajando en ello para futuras versiones, pero puedes escoger alguna de nuestra librería.

***¿Puedo establecer varias alarmas a la vez?***
- Sí, no supondría ningún problema. 

***¿Hay niveles de dificultad en los minijuegos?***
- No, pero entre los mini-juegos ya establecidos si que hay diferencia de dificultad. Existen mini-juegos más fáciles y más complejos.
 
 ***¿Qué pasa si no logro completar el minijuego?***
 - En caso de completarse el juego en un periodo de 5 minutos, se apagrá automáticamente. 

 ***¿Puedo desactivar la opción de minijuegos y apagar la alarma manualmente?***
 - ¡Sí! No obligamos a configurar un mini-juego a tu alarma, pero si te lo recomendamos. 

 ***¿Cual es el correo para contactar en caso de incidencias?***
 - Contáctianos mediante <wakkey@atencionalcliente.com>. 

___
## Diagrama de Flujo Flowchar

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {
    'primaryColor': '#f5dbdf',
    'labelBackground': '#FF0000',
    'primaryTextColor': '#543c5a',
    'lineColor': '#FF00FF',
    'primaryBorderColor': '#000000'
}}}%%
graph TD
    A(Inicia aplicación) --> B[Configurar nueva alarma]
    B --> C{¿Seleccionar hora?}
    C -->|Sí| D[Elegir hora y minutos]
    C -->|No| B
    D --> E{¿Seleccionar minijuego?}
    E -->|Sí| F[Elegir minijuego]
    E -->|No| G
    F --> G[Guardar alarma]
    G --> H[Alarma configurada]
    H --> I((Fin))

```

___
## Diagrama de Secuencia
```mermaid
sequenceDiagram
actor User as Usuario
participant FE as Wakkey
participant BE as Configuración de alarma
participant DB as Alarma guardada

User ->> FE: Añadir nueva alarma
FE ->> BE: Validación de hora
BE ->> DB: Validación de seleccion de minijuego
DB -->> BE: Alarma creada
BE -->> FE: Configuración correcta
FE -->> User: Alarma progamada
```

___
## Gráfico circular
```mermaid
pie
    title Juegos más jugados de Wakkey
    "Suma!": 20
    "Agita el móvil": 50
    "Fotografía algo": 35
    "Completa la frase": 25
    "Escanea tu producto favorito": 10
```
___
## Diagrama Entidad-Relación
```mermaid
erDiagram
    ALARMA {
        string nombre
        int hora
        int minuto
    }
    USUARIO {
        string id_usuario
        string nombre
        string correo_electronico
    }
    JUEGO {
        string id_juego
        string nivel_dificultad
    }
    USUARIO ||--o{ ALARMA : "configura"
   ALARMA }o--|| JUEGO : "incluye"
```
___
## Diagramas Journey
```mermaid
journey
    title Configurar una alarma
    section Selección hora 
        seleccionar una hora: 5: Usuario
        seleccionar los mitos: 4: Usuario
    section Configurar mini juego
        probar mini-juego: 3: Usuario
        configurar mini juego a la alarma: 5: Sistema
```
___
## Diagrama Git
```mermaid
gitGraph
    commit id: "Inicio del proyecto Wakkey"
    branch dev
    commit id: "Estructura base de la app"
    commit id: "Implementación de interfaz de usuario"
    checkout main
    commit id: "Primer release estable"
    merge dev
    commit id: "Merge de dev a main"
    branch game-mechanic
    commit id: "Añadir lógica del juego"
    checkout dev
    commit id: "Optimización de interfaz y ajustes de UX" tag: "Versión 1.0.0"
    merge game-mechanic
    branch sound-feature
    commit id: "Implementación de alarmas y sonidos"
    checkout main
    commit id: "Versión 2.0.0"
```
___
## Diagramas Gantt
```mermaid
gantt
    title Desarrollo de Wakkey
    dateFormat DD-MM-YYYY

    section Planificación
        Análisis de requisitos   :a1, 01-02-2025, 10d
        Diseño de interfaz       :a2, after a1, 15d

    section Desarrollo
        Implementación de UI     :b1, after a2, 20d
        Lógica del juego         :b2, after b1, 25d
        Configuración de alarmas :b3, after b2, 15d

    section Pruebas y Lanzamiento
        Pruebas funcionales      :c1, after b2, 15d
        Optimización y correcciones :c2, after c1, 10d
        Versión 1.0.0            :c3, after c2, 5d

```
___
## Diagramas de Requerimientos
```mermaid
requirementDiagram

requirement desactivacion_alarma {
  id: 1
  text: "La alarma solo se desactiva al completar un juego"
  risk: medium
  verifyMethod: test
}

requirement personalizacion {
  id: 2
  text: "El usuario puede elegir el tipo de juego para desactivar la alarma"
  risk: low
  verifyMethod: inspection
}

requirement interfaz_intuitiva {
  id: 3
  text: "La interfaz debe ser fácil de usar y configurar"
  risk: low
  verifyMethod: inspection
}

element minijuegos {
  type: gameLogic
}

element configuracion {
  type: userExperience
}

minijuegos -satisfies-> desactivacion_alarma
configuracion -satisfies-> personalizacion
configuracion -satisfies-> interfaz_intuitiva

```


