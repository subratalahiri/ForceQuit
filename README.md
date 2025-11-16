# ForceQuit (macOS)

This is a small Automator-based macOS utility that triggers the system shortcut **Command + Option + Escape**, opening the *ForceQuit Applications* window automatically.

## Installation

### Option 1 — Standalone App
1. Download `Force Quit.app.zip`
2. Unzip and move to Applications (optional)
3. Run the app
4. Go to **System Settings → Privacy & Security → Accessibility**  
   Add the app and enable access

### Option 2 — Quick Action
1. Download `Force Quit.workflow`
2. Double-click → it will install into `~/Library/Services`
3. Trigger via Spotlight or keyboard shortcut
4. Grant Accessibility permission when prompted

## How it Works

It uses an AppleScript inside Automator:

```applescript
tell application "System Events"
    key code 53 using {command down, option down}
end tell
# ForceQuit
