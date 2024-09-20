# **Multi-Purpose Discord Bot**

[![Discord](https://img.shields.io/badge/Discord4J-v3.2.2-blue)](https://github.com/Discord4J/Discord4J) [![Javacord](https://img.shields.io/badge/Javacord-v3.1.5-green)](https://github.com/Javacord/Javacord)

This bot is built on **Discord4J** and **Javacord** frameworks, designed to provide a variety of functionalities, including **AutoModeration** and **AnswerOverflow**. It's perfect for managing and improving your Discord server's workflow and enhancing user interaction.

## Features

- **AutoMod**: Automatic moderation to ensure server rules are followed. Capable of detecting:
  - Spam and excessive mentions
  - Offensive language filtering
  - Flood protection (limiting messages per user)
  - Banning or muting users after reaching a warning threshold
  
- **AnswerOverflow**: Integration with AnswerOverflow API to provide relevant answers to frequently asked questions within the server.

- **Utility Commands**: Including:
  - `!ban`, `!kick`, `!mute` for moderating users.
  - `!faq <query>`: Automatically fetches FAQ answers from AnswerOverflow.
  - `!purge <number>`: Deletes the specified number of messages from a channel.
  
- **Fun Commands**: Games and interaction commands like `!8ball`, `!meme`, `!roll`.
  
- **Information Commands**: Including server info, user info, and bot uptime.
  - `!serverinfo`, `!userinfo <user>`, `!uptime`
  
- **Customizable Roles**: Automatic assignment of roles based on user actions or manual commands.

## Tech Stack

The bot is powered by a mix of modern Java technologies, ensuring seamless performance and extendability:

- **[Discord4J](https://github.com/Discord4J/Discord4J)** – A reactive Java wrapper for the Discord API.
- **[Javacord](https://github.com/Javacord/Javacord)** – A simple, lightweight, and easy-to-use Java library for Discord.
- **[MongoDB](https://www.mongodb.com/)** – Database for storing user data, warnings, and configurations.
- **[Spring Boot](https://spring.io/projects/spring-boot)** – Framework used for microservice architecture and easy deployment.

## Installation

### Requirements

- **Java 17** or higher
- **Maven** or **Gradle** (for managing dependencies)
- **MongoDB** for data storage
- **Discord Developer Application** with bot token

### Setup

Clone the repository and navigate to the bot's directory:

```sh
git clone https://github.com/venkat1701/venkio
cd venkio
```

Install dependencies:

```sh
mvn clean install
```

Set up environment variables in `.env` file:

```bash
DISCORD_TOKEN=<your-bot-token>
MONGO_URI=<your-mongo-database-uri>
```

Run the bot:

```sh
mvn spring-boot:run
```

## Commands

| Command                | Description                                                   |
|------------------------|---------------------------------------------------------------|
| `!ban <user>`          | Bans a user from the server                                    |
| `!kick <user>`         | Kicks a user from the server                                   |
| `!mute <user>`         | Mutes a user for violating rules                              |
| `!purge <number>`      | Deletes a specified number of messages from a channel          |
| `!faq <query>`         | Fetches an answer from AnswerOverflow API                      |
| `!8ball <question>`    | Ask the magic 8 ball any question!                             |
| `!roll`                | Rolls a dice between 1 and 100                                 |
| `!serverinfo`          | Shows details about the current server                         |
| `!userinfo <user>`     | Displays information about a user                              |
| `!uptime`              | Shows how long the bot has been online                         |

## AutoMod Features

The AutoMod system monitors the following:

- **Spam Control**: Detects repeated messages, excessive mentions, and link flooding.
- **Profanity Filter**: Censors offensive language based on predefined word lists.
- **Action Thresholds**: Issues warnings, mutes, or bans based on a user’s violation history.
  
## Development

To contribute, follow these steps:

1. **Fork the repository**: Fork and clone this repo to your local machine.
2. **Create your feature branch**: 
   ```sh
   git checkout -b feature/your-feature-name
   ```
3. **Commit your changes**: 
   ```sh
   git commit -m 'Add some feature'
   ```
4. **Push to the branch**: 
   ```sh
   git push origin feature/your-feature-name
   ```
5. **Open a pull request**: Submit a PR for review!

## License

This project is licensed under the **MIT License**.

---

Enjoy moderating your Discord server with ease, and let the bot handle the rest!

**Free Software, Cheers!**

