<p align="center">
    <img src="https://github.com/KeirLoire/topwar-discord-chat/blob/main/img/logo.png?raw=true" width="200" alt="TopWar Discord Chat Sync logo"/><br>
    <b style="font-size:25px">TopWar Discord Chat Spy</b><br>
    <a href="https://www.python.org/downloads/release/python-379/"><img src="https://img.shields.io/badge/python-3.7-00a0dc?label=python&style=flat&logo=python" alt="Python logo"/></a>
</p>

## About

This script listens from TopWar chat websocket to read real-time chats (world/alliance) in the game then sends it to a webhook of a Discord channel.

There are two websockets in the game:
- The first one is for receiving real-time chats.
  - This is the websocket that we will be using this one in the script.
- The second one is for interacting within the game.

## Prerequisites
This script requires prerequisites in order to run.

- Python 3.7.9 or later.

## How to setup
- Run `pip install -r requirements.txt` to install all dependencies
- Configuring `config.ini`
  - [discord_webhooks]
    - main
      - This is where the webhook URL of a Discord channel is stored. You can find more info [here](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).
    - You could add more if you want, any name will do.
  - [topwar]
    - websocket
      - The websocket of the world. Technically, works for any worlds, you don't need to change this.
    - uuid
      - The UUID of your TopWar account. Used for saying hi to websocket before letting you in.
  - [topwar_channels]
    - This is the placeholders for the chat channel IDs of the alliances or servers that you want to listen.
    - You can change these names, they're just names for the channel IDs:
      > world_721  
      > alliance_21BC  
    - And you could add more channels to listen.
    - The World Chat ID
      - You can get the ID by modifying the format. Simply replace the <server_number> from the format with the server number that you want:
        - Format: 
          - 102_1_<server_number>g123
        - Examples:
          - world_1000 = 102_1_1000g123
          - world_721 = 102_1_721g123
    - The Alliance Chat ID
      > Still working on the guide for it.

    > NOTE: You can also spy from other servers and alliances despite not being a part of it.
- Run `python main.py`
- Leave the script open and notice chats being sent to the Discord channel.

If you want the script to end, just press `CTRL + C`.

## How did I get the websocket of the game?

> Still working on the guide for it.

## How did I get the chat channels of the game?

> Still working on the guide for it.

## Disclaimer

We are not responsible for any damages or loss upon use of this software. Use at your own risk. We don't encourage any illegal activity against TopWar and this is for educational purposes only.