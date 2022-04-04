# TRS ChatBot (therealshow)

## Proyecto

El proyecto consiste en un chatbot programado en _python 3_ y accesible mediante la aplicación _Telegram_ en la que se pueden consultar y almacenar los datos relativos a un equipo de futbol amateur. La aplicación permite tanto mostrar tus estadísitcas de cada temporada como compararlas con otros jugadores.

## Diseño

La aplicación dispone de tres elementos: El chatbot o interprete de comandos en Telegram, el servidor de despliegue y el servidor que almacena la base de datos.

### Comandos

| Comando | Descripción | Activo |
|---:|---|---|
| alta | Comando para darse de alta en el sistema. Crea tu perfil e inicializa las stats | ✔️ | 
| stats | Muestra un resumen de las estadisticas de cada jugador y su foto de perfil | ✔️ |
| partidos | Muestra una lista con todos los partidos | ✔️ |
| mypartidos | Crea | ✔️ |
| mygraph | Genera una gráfica de los resultados de los partidos | ✔️ |
| subirstats | Sube las estadisticas en texto de un partido | ❌ |

### Instalación

El servidor de persistencia está operativo de forma ininterrumpida. La configuración se realiza mediante la instalación del archivo de requisitos _requierements.txt_. Se instalan las librerias necesarias para la ejecución del programa.

> **Requisitos**: python-telegram-bot, matplotlib

### Base de datos

La base de datos y las imágenes de los perfiles de los jugadores se almacenan en un servidor accesible mediante FTP. La base de datos está programada en SQlite y está dividida en temporadas. Cada temporada recibe los siguientes datos:

> **Datos de jugador**: nombre, número de goles, número de asistencias, partidos ganados, partidos en empate, partidos jugados, ficha

> **Datos de partido**: temática, resultado, jugadores, equipación, campo, fecha

## Ejecución

Existen dos modos de ejecución:

* Ejecución Local (Desarrollo)
  * Permite la ejecución en una maquina local para pruebas y actualizaciones. Utiliza la variable _MODE == "dev"_ y los cambios no se aplican hasta realizar un commit.
* Ejecución Remota (Release)
  * Ejecución del código mediante un _deploy_ implementado en _Heroku_, concretamente es un _listener_ que escucha peticiones _HTTP_. El modo debe estar en _MODE == "prod"_.

## Despligue

El despliegue se realiza a través de _Heroku_, una plataforma gratuita de hospedage web y programas. Se hace uso de una máquina con las siguientes características:
```shell
System: Linux
RAM: 512MB
HD: 500 MiB
```

## Fuentes de Información

[Python Telegram Bot](https://python-telegram-bot.readthedocs.io/en/stable/)

[Lógica de recepción de peticiones](https://github.com/python-telegram-bot/python-telegram-bot/wiki/Webhooks#heroku)
