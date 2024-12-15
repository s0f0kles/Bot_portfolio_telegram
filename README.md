# Telegram Project Manager Bot

A Telegram bot designed to help users manage and track their projects efficiently. This bot provides features for adding, updating, deleting, and viewing projects, along with associating skills and statuses with projects.

## Features

- **Add New Projects**: Users can create new projects, add descriptions, links, and assign statuses.
- **View Projects**: Display a list of all saved projects with their details.
- **Update Project Information**: Modify attributes such as project name, description, link, and status.
- **Delete Projects**: Remove projects no longer needed.
- **Associate Skills**: Link specific skills to projects to keep track of required expertise.
- **Inline Buttons and Markup**: Intuitive keyboard and inline button interface for easy navigation.

## Commands

### Core Commands
- `/start`: Initialize the bot and display a welcome message.
- `/info`: Get information about the bot's features and commands.
- `/new_project`: Add a new project with details like name, description, link, and status.
- `/projects`: View a list of all projects.
- `/delete`: Remove a project by its name.
- `/update_projects`: Update details of an existing project.

### Additional Commands
- `/skills`: Assign skills to projects.

## Setup

### Prerequisites

- Python 3.x
- Required libraries: `pyTelegramBotAPI` (telebot), database handler (`logic.DB_Manager`)
- Database configuration file (`config.py`) containing `TOKEN` (Telegram bot token) and `database` (database connection details).

### Installation

1. Clone the repository or download the bot's source code.
2. Install the required Python libraries:
   ```bash
   pip install pyTelegramBotAPI
   ```
3. Configure the `config.py` file with:
   - Your Telegram bot token (`TOKEN`).
   - Your database details (`database`).
4. Ensure your database is set up and matches the structure expected by the `DB_Manager` class.

### Run the Bot

Execute the bot script:
```bash
python bot.py
```

## How It Works

### Adding a New Project
1. Use the `/new_project` command.
2. Follow the prompts to:
   - Enter the project name.
   - Add a description.
   - Provide a link.
   - Select a status from a predefined list.
3. The bot saves the project to the database.

### Viewing Projects
Use the `/projects` command to get a list of all projects. Click on a project name to see its full details.

### Updating Projects
1. Use `/update_projects` to select a project to update.
2. Choose the attribute to modify (e.g., name, description, link, status).
3. Provide the new information.

### Deleting Projects
1. Use `/delete` to display a list of your projects.
2. Select the project to delete.
3. Confirm the deletion.

### Associating Skills
1. Use `/skills` to select a project.
2. Choose a skill from the list to associate it with the selected project.

## File Structure

```
.
├── bot.py                # Main bot script
├── logic/
│   └── DB_Manager.py     # Database management class
├── config.py             # Configuration file with TOKEN and database details
└── README.md             # Documentation file (this file)
```

## Notes

- Inline and reply keyboard markups are used to enhance user interaction.
- The bot gracefully handles invalid inputs and guides the user through the commands.
- A "Cancel" button is available during multi-step processes to exit the operation.

## Future Enhancements

- Add support for project deadlines and reminders.
- Enhance skill management with categories or levels.
- Provide analytics or summary of user projects.

## License

This project is open-source and available under the MIT License.