# django-discord-bot
Framework for creating Discord bots using Django

* Uses ASGI for high efficiency and modern features
* Allows using a single daemon for both HTTP and Discord, making for easy deployment
* Integrates into Django's model, allowing for highly modular applications

## prior art

* https://pycord.dev/
* https://github.com/AdvocatesInc/django-channels-discord


## ASGI Messages


* -> `discord.disconnect`: The WebSocket connection was closed. This does not
  mean we're shutting down, though--the framework will attempt to reconnect and
  resume.
* -> `discord.*`: Discord DISPATCH events are dynamically mapped to message types
  Of interest is `discord.ready`, which is sent after authentication has happened
