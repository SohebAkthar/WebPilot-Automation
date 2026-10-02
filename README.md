🤖 WebPilot-Automation
WebPilot-Automation is a configurable browser automation project built with React and JavaScript.
It allows users to create browser automation tasks by defining an automation name, target website URL, target element CSS selector, and action. A browser-side worker reads the saved configuration and performs the configured action when the target element appears.
🚀 Project Overview
WebPilot-Automation demonstrates how a web application can create and store browser automation configurations and how a browser-side worker can detect target elements and perform predefined actions.
Core Workflow
```text
User creates automation
        ↓
Automation saved in localStorage
        ↓
Browser Worker reads configuration
        ↓
Worker checks for configured target
        ↓
Target element appears
        ↓
WebPilot detects the target
        ↓
Configured action is executed
        ↓
Worker stops after successful execution
```
✨ Features
Create browser automation tasks
Configure automation name
Configure target website URL
Configure CSS element selector
Configure action type
Save automations using `localStorage`
Persist automations after page refresh
Delete saved automations
Detect dynamically rendered webpage elements
Automatically execute click actions
Prevent duplicate execution
Stop the worker after successful execution
Controlled demo environment for testing automation
🛠️ Tech Stack
Category	Technologies
Frontend	React, JavaScript, Vite, CSS
Browser Automation	JavaScript, Safari Userscripts, DOM APIs
Browser APIs	`localStorage`, `querySelector`, `setInterval`
Development Tools	Git, GitHub, VS Code
📸 Demo
The project contains a controlled local demo environment for testing browser automation.
Demo Flow
Open the WebPilot-Automation application.
Create an automation.
Configure the target selector.
Save the automation.
The Browser Worker reads the configuration.
The worker monitors the webpage.
When the target element appears, the worker detects it.
The configured action is executed.
The worker stops after successful execution.
Example Automation
Setting	Value
Name	`Confirm Presence Demo`
Website	`http://localhost:5173/`
Selector	`#confirm-presence`
Action	`click`
🌐 Browser Worker
The Browser Worker uses a Safari Userscript as its current browser integration layer.
It:
Reads the saved automation configuration from `localStorage`.
Reads the configured CSS selector.
Checks the webpage for the target element.
Detects the target when it appears.
Executes the configured action.
Prevents duplicate execution.
Stops checking after successful execution.
Currently Supported Action
`Click`
> **Note:** The current version uses Safari Userscripts as its browser integration layer. A dedicated browser extension is planned for a future version.
⚙️ Getting Started
Prerequisites
Before running the project, make sure you have:
Node.js
npm
Git
Safari
A compatible Userscripts Safari extension
1. Clone the Repository
```bash
git clone https://github.com/SohebAkthar/WebPilot-Automation.git
```
2. Navigate to the Project
```bash
cd WebPilot-Automation
```
3. Install Dependencies
```bash
npm install
```
4. Start the Development Server
```bash
npm run dev
```
The application will be available at:
```text
http://localhost:5173/
```
🧪 Running the Automation Demo
After starting the application:
Open the application in Safari.
Install/open your Userscripts extension.
Add the following worker script:
```text
browser-worker/browser-worker.js
```
Allow Userscripts to run on `localhost`.
Create the following automation:
Setting	Value
Name	`Confirm Presence Demo`
Website	`http://localhost:5173/`
Selector	`#confirm-presence`
Action	`click`
Open the Demo section.
Wait for the target button to appear.
The Browser Worker detects the target.
The configured click action is executed.
📂 Project Structure
```text
WebPilot-Automation/
│
├── backend/
├── browser-worker/
├── extension/
├── public/
├── safari-extension/
│
├── src/
│   ├── assets/
│   ├── Pages/
│   │
│   ├── App.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
│
├── .gitignore
├── eslint.config.js
├── index.html
├── package.json
├── package-lock.json
├── README.md
└── vite.config.js
```
🔐 Safety
WebPilot-Automation is designed around controlled and predefined browser automation actions.
The current demo uses a locally controlled environment.
The project is not designed to bypass:
CAPTCHA
MFA
Authentication security
Anti-bot protections
Paywalls
Access controls
🗺️ Roadmap
V1 — Core Automation
[x] React automation dashboard
[x] Create automation
[x] Save automation configuration
[x] `localStorage` persistence
[x] Configurable CSS selector
[x] Dynamic target detection
[x] Click action
[x] Duplicate execution prevention
[x] Stop worker after successful execution
[x] Controlled demo environment
V2 — Browser Integration
[ ] Dedicated browser extension
[ ] Visual element picker
[ ] Multiple automation targets
[ ] Additional predefined actions
[ ] Enable / disable automation
V3 — Automation Platform
[ ] Backend API
[ ] PostgreSQL database
[ ] User authentication
[ ] Scheduling
[ ] Execution history
[ ] Execution logs
[ ] Safety policies
Future Enhancements
[ ] Conditional workflows
[ ] Notifications
[ ] Automation templates
[ ] Import / export
[ ] AI-assisted element discovery
🎯 Project Purpose
This project was developed to explore and demonstrate:
Browser automation
DOM interaction
Configurable automation workflows
React application development
Browser-side automation
Client-side data persistence
JavaScript browser APIs
The project demonstrates how a frontend application can store automation configurations and how a browser-side worker can read those configurations and execute predefined actions.
👨‍💻 Author
Soheb Akthar
GitHub: https://github.com/SohebAkthar
LinkedIn: https://www.linkedin.com/in/k-md-soheb-akthar/
📄 License
This project is currently provided for learning and portfolio purposes.
There is currently no open-source license.