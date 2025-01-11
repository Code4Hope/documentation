# Getting Started
Welcome to the project! This guide will walk you through the process of setting up your local development environment and collaborating with the team on GitHub.

## Step 1: Install Required Tools

To get started, you’ll need to install the necessary tools on your machine:

### 1. **Git** (Version Control)
Git is a version control system that allows you to track changes and collaborate with others on code. It will be used to manage project code across multiple developers.

- **Windows**: 
  - [Download Git for Windows](https://git-scm.com/download/win)
  - After downloading, follow the installation wizard and make sure to add Git to your system PATH during installation.
  
- **macOS**:
  - [Download Git for macOS](https://git-scm.com/download/mac)
  - Follow the installation instructions

- **Linux**:
  - Use your package manager to install Git. For example, on Ubuntu, run:
    ```bash
    sudo apt-get install git
    ```

After installing, verify Git is correctly installed by running the following command in your terminal:
```bash
git -v
```

### 2. **Node.js** (JavaScript Runtime)
Node.js is a JavaScript runtime used for running JavaScript on the server-side and also for managing project dependencies. You’ll use Node.js to run local servers, package management, and more.

- **Download for Windows and macOS**:
  - [Download Node.js](https://nodejs.org/)

Follow the installation steps for your OS. During installation, ensure that the option to install `npm` (Node Package Manager) is selected.

- **Linux**:
  - You can install Node.js through the package manager. For Ubuntu, run:
    ```bash
    sudo apt-get install nodejs
    sudo apt-get install npm
    ```

Verify the installation by running:
```bash
node -v
npm -v
npx -v
```

## Step 2: Explore Development Frameworks

### 1. **Web Development: React**
React is a popular JavaScript library used for building user interfaces. It allows developers to build reusable UI components.

- **Why React**: React makes it easy to develop complex user interfaces with a component-based architecture. It is fast, flexible, and supports building both web and mobile applications.
- **Official Documentation**: For detailed guidance, examples, and best practices, visit the [React Documentation](https://reactjs.org/).
- **Recommended Setup**: You can set up a new React project using the command:
  ```bash
  npx create-react-app my-app
  cd my-app
  npm start
  ```

### 2. **Mobile App Development: Flutter**
Flutter is an open-source framework by Google for building natively compiled applications for mobile, web, and desktop from a single codebase. It uses the Dart programming language.

- **Why Flutter**: Flutter is fast, expressive, and allows for seamless UI design with a vast set of pre-designed widgets. It’s an excellent choice for cross-platform mobile app development.
- **Official Documentation**: Check out the [Flutter Documentation](https://flutter.dev/docs) for setup instructions and tutorials.
- **Recommended Setup**: To set up Flutter, follow these steps:
  - Install Flutter SDK following the instructions for your OS on the [Flutter Install Page](https://flutter.dev/docs/get-started/install).
  - Once installed, run the following command to check that Flutter is installed correctly:
    ```bash
    flutter doctor
    ```

## Step 3: Collaborate Using GitHub

GitHub is where all of our project’s code will be stored, and it allows for easy collaboration among team members. Here’s how you can get started:

### 1. **Join the GitHub Repository**
- All operations team members will be sent an invitation to join the repository for whichever project we are currently working on at the time. Follow the link in the invitation email to gain access to the project’s GitHub repository.

### 2. **Clone the Repository**
Once you’ve accepted the invitation and want to begin working, clone the repository to your local machine using the following command:
```bash
git clone https://github.com/your-organization/your-repository.git
```

### 3. **Working Out of Branches**
- The `main` branch is the default branch where all development will occur, however always check with the rest of the team to ensure you are editing the correct branch to avoid any mistakes. The following steps will work for other branches as well.
- To check out the `main` branch, run:
  ```bash
  git checkout main
  ```
- If you are currently in another branch, you can switch to the `main` branch by running:
  ```bash
  git switch main
  ```

Here's the updated GitHub workflow step with instructions for establishing a remote connection:

---

### 4. **Follow the GitHub Workflow**
To collaborate effectively, follow these steps to set up and work with GitHub:

#### **1. Fork and Clone the Repository**
- Fork the repository to your personal GitHub account (if applicable) by clicking the **Fork** button on the repository page.
- Clone the repository to your local machine using:
  ```bash
  git clone https://github.com/your-organization/your-repository.git
  ```
  Replace `your-organization/your-repository` with the actual repository URL. This creates a local copy of the project on your machine.

#### **2. Establish a Remote Connection**
- Verify that the repository has a remote URL configured by running:
  ```bash
  git remote -v
  ```
- If it doesn’t, that means you still have to establish a remote connection. Use the following commands:
  - Set up the origin repository:
    ```bash
    git remote add origin https://github.com/your-username/your-repository.git
    ```

- To confirm, run:
  ```bash
  git remote -v
  ```
  You should see both `origin` URLs.

#### **3. Create a New Branch**
Before making changes, create a new branch to work on:
```bash
git checkout -b branch-name
```
This keeps your changes separate from the `main` branch until they are ready to be reviewed and merged.

#### **4. Make Changes and Commit**
Make your changes to the project files. After completing your work:
1. Stage your changes (you must add a space after the period or the commmand will not run-- this indicates that you want to stage ALL files in the project's root directory):
   ```bash
   git add .
   ```
2. Commit your changes with a meaningful message:
   ```bash
   git commit -m "Description of your changes"
   ```

#### **5. Push Changes**
Push your changes to your GitHub repository:
```bash
git push origin feature-branch-name
```
If this is your first time pushing to a new branch, Git may prompt you to set the upstream branch. Use:
```bash
git push --set-upstream origin feature-branch-name
```

---

With this detailed guide, you should have a clear understanding of how to set up your environment, collaborate effectively using GitHub, and get started with the frameworks used in this project. If you encounter any issues or need assistance, feel free to ask the team for support!

