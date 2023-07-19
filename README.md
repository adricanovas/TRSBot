# TRS ChatBot (therealshow)

## Project

The project consists of a chatbot programmed in _python 3_ and accessible through the _Telegram_ application, in which you can consult and store data related to an amateur football team. The application allows you to display your statistics for each season as well as compare them with other players.

## Design

The application has three elements: The chatbot or command interpreter in Telegram, the deployment server, and the server that stores the database.

### Commands

| Command | Description | Active |
|---:|---|---|
| alta | Command to register in the system. Create your profile and initialize the stats | ✔️ | 
| stats | Shows a summary of the statistics of each player and their profile picture | ✔️ |
| partidos | Shows a list with all the matches | ✔️ |
| mypartidos | Create | ✔️ |
| mygraph | Generates a graph of the results of the matches | ✔️ |
| subirstats | Upload the statistics in text of a match | ❌ |

### Installation

The persistence server is continuously operational. Configuration is done by installing the _requirements.txt_ file. The necessary libraries for program execution are installed.

> **Requirements**: python-telegram-bot, matplotlib

### Database

The database and player profile images are stored on a server accessible via FTP. The database is programmed in SQlite and is divided into seasons. Each season receives the following data:

> **Player data**: name, number of goals, number of assists, matches won, matches tied, matches played, file

> **Match data**: theme, result, players, equipment, field, date

## Execution

There are two modes of execution:

* Local Execution (Development)
  * Allows execution on a local machine for testing and updates. Uses the variable _MODE == "dev"_ and changes are not applied until a commit is made.
* Remote Execution (Release)
  * Code execution through a _deploy_ implemented in _Heroku_, specifically a _listener_ that listens for _HTTP_ requests. The mode must be in _MODE == "prod"_.

## Deployment

Deployment is done through _Heroku_, a free web hosting and program platform. A machine with the following characteristics is used:
```shell
System: Linux
RAM: 512MB
HD: 500 MiB
```

## Information Sources

[Python Telegram Bot](https://python-telegram-bot.readthedocs.io/en/stable/)

[Request reception logic](https://github.com/python-telegram-bot/python-telegram-bot/wiki/Webhooks#heroku)

Citations:
[1] https://pypi.org/project/md-translate/
[2] https://www.stepes.com/markdown-translation/
[3] https://help.smartling.com/hc/en-us/articles/360012489774-Markdown
[4] https://stackoverflow.com/questions/30585841/is-there-a-method-for-translating-markdown-formatted-text
[5] https://www.markdownguide.org/tools/simpleen/
[6] https://products.groupdocs.app/translation/markdown
