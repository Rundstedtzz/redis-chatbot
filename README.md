# LoveYourself Chatbot

## Table of Contents
1. [Introduction](#introduction)
2. [Features & Commands](#features--commands)
3. [Getting Started](#getting-started)

## Introduction
The LoveYourself Chatbot is a Python-based chatbot project created for a NoSQL class. This chatbot uses Redis for data storage and offers multiple features like weather updates, fun facts, user-specific data storage, channel communications, and ask questions to large language model. The functionality of this chatbot will be continuously added and thank you for any questions, feedbacks and suggestions.

## Features & Commands

#### General Commands
- !help: Displays a list of all available commands and their usage.
- !weather <city>: Provides the current weather conditions for the specified city.
- !fact: Delivers a random fun fact.
- !whoami: Displays stored user information.
- exit: Exit the chatbot

#### Channel Commands
- !join <channel>: Join a specified channel to send and receive messages.
- !leave <channel>: Leave a channel you previously joined.
- !send <channel> <message>: Send a message to all users in a specified channel.
- !listen <channel>: Start receiving messages from a particular channel.
- !pm <username> <message>: end a private message to a specific user.
- !who <channel>: List all active users in a channel

#### Advanced Command
- !QA LLM <question>: Asks a question to a language model and receives an answer. You will be prompted to enter your OpenAI API key securely.

## Getting Started

#### Requirements (Packages & Environment)
- Docker
- Python 3.x
- Redis
- Langchain
- OpenAI

#### Setup （Step by step)
1. Download the docker-compose.yml file (don't forget to change paths), go to the directory, and run `docker-compose up` to activate python and redis containers and allow these two containers to connect
2. run `docker exec -it <container_id> bash` and `docker exec -it <container_id> redis_cli` to go to python and redis_cli containers (use different tabs of terminal to do so)
3. Download the mp1.py file and run `python mp1.py` to use the chatbot
<img width="625" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/66525435-a8b7-4f6d-8c66-ee1ea1c094ee">


#### Use Chatbot （Step by step)
1. You will be asked to enter some basic information; the information will then be stored, so next time you enter the chatbot, you will only be asked to enter username if there is an existing username:
<img width="249" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/df4b395c-25bd-466e-a05b-8a8611878059">
<img width="230" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/3db8b26b-2dbc-45d3-830b-b316e4b9cff2">


2. You can then play around the general commands:
<img width="713" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/15f3c7de-557a-4102-871a-9f875792c16a">


3. You can also play around with the channel commands and monitor the activities in channels by running `MONITOR` in redis_cli:
<img width="302" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/127cec78-1d63-4716-a925-9a5b23678a66">
<img width="954" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/d46518bd-f86a-4e54-82a8-7da2c249c8d4">

<img width="389" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/7da5b678-ef2d-40b9-b642-9f901a9b7473">
<img width="1231" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/9d16faff-2ea0-4f19-acb5-b461a71b9723">


4. You can also use the QA functionality if you have any question to GPT4
<img width="1284" alt="image" src="https://github.com/Rundstedtzz/redis-chatbot/assets/63605514/420da145-51f3-4bd9-afda-08503d5e1d6e">

