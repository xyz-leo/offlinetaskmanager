# Offline Task Manager (HTML + CSS + JS Only)

This is a fully offline, self-contained Task Manager (To-do list) application built with only HTML, CSS, and JavaScript. No server or backend is required — all data is stored in the browser using `localStorage`.

> Disclaimer: This application is entirely client-side. No encryption or server-side processing is involved. All data is stored in the browser's localStorage. It is recommended for personal, non-sensitive use only.


<img width="608" height="816" alt="Task Manager Screenshot" src="https://github.com/user-attachments/assets/6ee8bbd4-00e3-4b52-a6bf-78a5eb2490e9" />


## Features

- Add tasks with a title and optional description
- Mark tasks as done or not done
- Delete individual tasks
- Automatically saves tasks locally in the browser
- Set a simple password on first access (stored locally)
- Export tasks as a `.json` file
- Import `.json` files to restore or merge tasks
- Responsive design with minimal styling

## How it Works

- Tasks are stored as an array of objects in `localStorage`, under the key `todo-tasks`
- The password (if set) is stored in plain text in `localStorage` under the key `todo-password`
- Importing a `.json` file merges tasks with the existing ones
- Exported files contain the full list of tasks in JSON format

## How to Use

1. Open the `index.html` file in your browser
2. Set a password on first access (required to proceed)
3. Add tasks using the form
4. Use the buttons to export or import `.json` backups
5. All changes are saved automatically

## Data Format

Each task in the JSON array has the following structure:

```json
{
  "title": "Buy groceries",
  "description": "Milk, eggs, bread",
  "done": false
}
```

## Limitations

- Data is limited to approximately 5MB (browser `localStorage` limit)
- All data is stored locally and unencrypted
- If browser data is cleared, all tasks will be lost unless exported

## License

This project is free to use and modify for personal or educational purposes.
