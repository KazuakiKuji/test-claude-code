# test-claude-code

English | [日本語](../../README.md)

## Overview

A simple TODO app built with vanilla HTML, CSS, and JavaScript. No frameworks required — data is persisted via LocalStorage.

### Deploy

<https://kazuakikuji.github.io/test-claude-code/>

### App Preview

![App Preview](../images/app-preview-1.png)

## Background

This is a sample repository created to explore a development workflow using Claude Code. Using a simple TODO app as a subject, the project covers the full cycle from planning to coding and committing.

## How It Works

1. On page load, `loadTodos()` restores the TODO list from LocalStorage.
2. When the user submits the form (or presses Enter), `addTodo()` appends a new TODO.
3. Clicking the checkbox or the text label calls `toggleTodo()` to switch the completed state.
4. Clicking the `×` button calls `deleteTodo()` to remove the TODO.
5. After every state change, `saveTodos()` persists the data to LocalStorage and `renderTodos()` updates the DOM.

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/KazuakiKuji/test-claude-code.git
cd test-claude-code
```

### 2. Verify the file structure

No server is required. The app runs with just these three files.

```text
test-claude-code/
├── index.html   # UI markup
├── style.css    # Styles
└── script.js    # Logic (CRUD + LocalStorage)
```

## Usage

### Running manually

Open `index.html` directly in your browser.

```bash
# Linux / macOS
open index.html

# Windows
start index.html
```

You can also use a local server such as the VSCode Live Server extension.

## Common Issues

### TODOs are not displayed after adding

The browser may have failed to load `script.js`. Open the developer tools (F12), check the console for errors, and verify that the file paths are correct.

### TODOs disappear after a page reload

LocalStorage may be disabled in private/incognito mode. Try opening the page in a normal browser window.
