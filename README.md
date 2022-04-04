# TRS ChatBot (therealshow)

## Proyecto

El proyecto consiste en un chatbot programado en _python 3_ y accesible mediante la aplicación _Telgram_ en la que se pueden consultar y almacenar los datos relativos a un equipo de futbol amateur.

## Diseño

La aplicación cuenta con un

| Comando | Descripción | Activo |
|---:|---|---|
| alta | Dirección del Viento, medido a 2 m | ✔️ | 
| stats | Dirección del Viento, medido a 2 m | ✔️ |
| partidos | Dirección del Viento, medido a 2 m | ✔️ |
| mypartidos | Dirección del Viento, medido a 2 m | ✔️ |
| mygraph | Dirección del Viento, medido a 2 m | ✔️ |
| subirstats | Dirección del Viento, medido a 2 m | ✖️ |


## Ejecución

Existen dos modos de ejecución:

* Ejecución Local (Desarrollo)
  * Permite la ejecución en una maquina local para pruebas y actualizaciones. Utiliza la variable _MODE == "dev"_ y los cambios no se aplican hasta realizar un commit.
* Ejecución Remota (Release)
  * Ejecución del código mediante un _deploy_ implementado en _Heroku_, concretamente es un _listener_ que escucha peticiones _HTTP_.

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
