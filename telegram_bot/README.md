# Telegram Group Management Bot

A powerful Telegram bot for managing group chats with features like user moderation, administrative controls, and automated welcome messages.

## Features

### Basic Commands
- `/start` - Initialize the bot
- `/help` - Display available commands
- `/rules` - Show group rules
- `/info` - Display group information

### Admin Commands
- `/ban` - Ban a user from the group
- `/unban` - Unban a previously banned user
- `/mute` - Restrict a user from sending messages
- `/unmute` - Remove message restrictions from a user
- `/kick` - Remove a user (they can rejoin)
- `/pin` - Pin a message to the group
- `/unpin` - Unpin a message
- `/listadmins` - Show all group administrators

### Automated Features
- Welcome messages for new members
- Logging of all administrative actions
- Error handling and reporting

## Setup Instructions

1. **Prerequisites**
   - Python 3.9 or higher
   - pip (Python package manager)

2. **Installation**
   ```bash
   # Clone the repository
   git clone <repository-url>
   cd telegram_bot

   # Create a virtual environment
   python -m venv venv

   # Activate the virtual environment
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate

   # Install dependencies
   pip install -r requirements.txt
   ```

3. **Configuration**
   - Create a `.env` file in the project root with the following content:
     ```
     BOT_TOKEN=your_bot_token_here
     ADMIN_IDS=123456789,987654321  # Comma-separated list of admin user IDs
     ```
   - Replace `your_bot_token_here` with your Telegram Bot Token (get it from [@BotFather](https://t.me/botfather))
   - Add the Telegram user IDs of all administrators in `ADMIN_IDS`

4. **Running the Bot**
   ```bash
   python bot.py
   ```

## Usage Guide

### For Administrators

1. **Basic Group Management**
   - Use `/ban` or `/kick` to remove problematic users
   - Use `/mute` to temporarily restrict users from sending messages
   - Use `/pin` to highlight important messages

2. **Command Usage Examples**
   - Ban a user: `/ban 123456789 Spamming`
   - Mute a user: `/mute 123456789`
   - Pin a message: Reply to a message with `/pin`

### For Users

1. **Getting Started**
   - Use `/start` to initialize the bot
   - Use `/help` to see available commands
   - Use `/rules` to review group rules

## Logging

- All administrative actions are logged in `logs/bot.log`
- Logs include timestamps, action types, and relevant user information
- Error logs help in troubleshooting issues

## Security Features

- Admin-only commands are protected
- User permission validation
- Error handling and logging
- Rate limiting on certain commands

## Troubleshooting

1. **Bot Not Responding**
   - Check if the bot is running
   - Verify the BOT_TOKEN in .env
   - Ensure the bot has admin privileges in the group

2. **Permission Errors**
   - Verify bot's admin status
   - Check ADMIN_IDS configuration
   - Ensure bot has necessary group permissions

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
