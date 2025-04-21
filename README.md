# Peteware Dev Toolbox

Welcome to the **Peteware Dev Toolbox**, a collection of useful tools and guides for Roblox developers. This toolbox includes various scripts that can be quickly loaded into your game to enhance your development experience.

## Features

### Guides Section:
- **Semantic Versioning Guide**:
  - A simple guide that introduces **Semantic Versioning** and how to use it in your projects. 
  - Covers versioning conventions like **MAJOR**, **MINOR**, and **PATCH** versions and provides example scenarios for version upgrades.
  
### Toolbox Section:
- **Infinite Yield**:
  - A powerful and popular admin command tool with a variety of commands to control and manipulate your game environment.
  - Commands include features like:
    - Teleportation of players
    - Admin privileges for players
    - Custom commands such as `:kill`, `:freeze`, and more.
  
- **Remote Spy**:
  - A debugging tool that helps you track and inspect **remote functions** and **remote events** in Roblox games.
  - Allows you to monitor how remotes are triggered and their parameters, helping developers debug their games and identify potential issues.

- **Dex Explorer**:
  - A tool that allows developers to **explore game objects** and their properties.
  - Features include:
    - Viewing objects and their properties in the game
    - Accessing methods and events attached to objects
    - Easy navigation through your game’s hierarchy.

- **Hydroxide**:
  - An advanced scripting and UI toolkit for Roblox developers.
  - Features:
    - Custom UI components for creating professional and unique game interfaces.
    - Various script utilities designed to assist with development and debugging.
    - Built-in functionality for creating enhanced in-game tools and menus.
  
- **Adv AC Scanner**:
  - A script designed to scan your game for **Anti-Cheat** mechanisms.
  - Identifies and reports any anti-cheat systems that are present in your game, helping you test and ensure game security.
  - Helps developers check for potential vulnerabilities and identify existing cheats in games.

## Installation

To use the Peteware Dev Toolbox, simply execute the following script in your Roblox game:

```lua
local Library = loadstring(Game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wizard"))()

local PetewareToolbox = Library:NewWindow("Dev Toolbox | Peteware")

local Guides = PetewareToolbox:NewSection("Guides")

Guides:CreateButton("Semantic Versioning", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/poupeue/VersioningForBeginners/refs/heads/main/guide.lua",true))()
end)

local Tools = PetewareToolbox:NewSection("Toolbox")

Tools:CreateButton("Infinite Yield", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
end)

Tools:CreateButton("Remote Spy", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/infyiff/backup/main/SimpleSpyV3/main.lua"))()
end)

Tools:CreateButton("Dex Explorer", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/infyiff/backup/main/dex.lua"))()
end)

Tools:CreateButton("Hydroxide", function()
    local owner = "Upbolt"
    local branch = "revision"

    local function webImport(file)
        return loadstring(game:HttpGetAsync(("https://raw.githubusercontent.com/%s/Hydroxide/%s/%s.lua"):format(owner, branch, file)), file .. '.lua')()
    end

    webImport("init")
    webImport("ui/main")
end)

Tools:CreateButton("Adv AC Scanner", function()
    loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Advanced-Game-Anti-Cheat-Scanner-33244",true))()
end)
