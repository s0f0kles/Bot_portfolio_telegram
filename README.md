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

### Prerequisites

- Python 3.x
- Required libraries: `pyTelegramBotAPI` (telebot), database handler (`logic.DB_Manager`)
- Database configuration file (`config.py`) containing `TOKEN` (Telegram bot token) and `database` (database connection details).


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

