# Google Apps Script (GAS)

Google Apps Script, commonly abbreviated GAS, is a JavaScript-based scripting system for Google products such as Gmail, Google Drive, Google Sheets, and more. GAS powers addons and allows you to create custom utilities or automation functions that integrate with various Google services.  

Since GAS runs on Google Cloud, you don’t need to host your own backend—Google handles everything for free.

## Example Use Cases:
- Automated data storage
- Cross-platform web apps integrating with Google services
- Automatic email template rendering and sending
- Automatic Google Calendar event creation

For more information, visit the [official documentation](https://developers.google.com/apps-script).

---

## Types of GAS Projects

### Standalone Projects
- Not tied to a specific Google Drive file.
- Created from [script.google.com](https://script.google.com).
- Best for apps intended for multiple unrelated files.

### Container-Bound Projects
- Linked to a specific Google Drive file.
- Copied and shared along with the file.
- Ideal for automation functions tailored to that file (e.g., a Google Sheet).

Both types can be managed with Google's in-browser IDE, which includes execution logs, error tracking, deployment tools, and more.

---

## Getting Started
Visit the GAS homepage [here](https://developers.google.com/apps-script). Start with their [official guide](https://developers.google.com/apps-script/guides) to learn the basics.

---

## Clasp

**Clasp** is a CLI tool that allows you to write GAS code in any IDE instead of the browser-based IDE. Though similar to Git, Clasp is **not** a version control system but works well alongside Git for managing your projects.

### Installation
1. Install Node.js and a package manager (e.g., npm).
2. Install Clasp globally:
   ```
   npm install -g @google/clasp
   ```

### First-Time Setup
Authenticate with your Google account by running:
```
clasp login
```
You can log out with:
```
clasp logout
```

### Creating a Project
Create a GAS project with:
```
clasp create
```
This will generate a GAS project and a linked Google Drive file (if container-bound). Links to the project will be provided in the terminal.

### Syncing Changes
- Pull updates from Google:
  ```
  clasp pull
  ```
- Push changes to Google:
  ```
  clasp push
  ```

> Note: These commands sync with Google but don’t affect your Git repository. Use Git commands separately for version control.

### File Types
Clasp supports JavaScript (`.js`) and TypeScript (`.ts`). TypeScript is automatically compiled when you push the project.

### Adding Dependencies
To include NPM dependencies, create a project in the directory:
```
npm init -y
```

---

## GAS Type Hinting

To enable type hinting and autocompletion in your IDE, install GAS type definitions:
```
npm install --save @types/google-apps-script
```

For web apps, install:
```
npm install --save @dgcode/html-service
```

---

## Web Apps with GAS

GAS can host serverless web apps that interact with Google services. For example, you could create a frontend that reads and modifies data in a Google Sheet. Learn more in the [GAS Web Apps Guide](https://developers.google.com/apps-script/guides/web).

---