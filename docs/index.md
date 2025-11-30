# UniversalAction

UniversalAction is a **robust action system for Roblox**, allowing developers to create, manage, and execute modular actions with minimal boilerplate.

Actions can be **server-side**, **client-side**, or **universal**, and include built-in:

- Middleware
- Hooks (`BeforeRun` / `AfterRun`)
- Async execution (Promises)
- Strict validation and warnings
- Logging

---

## Table of Contents

- [Features](#features)
- [Usage Examples](#usage-examples)
- [API Reference](./api.md)
- [Built-in Actions](./actions.md)
- [Guides](./guides.md)
- [Contributing](./contributing.md)

---

## Features

- Modular and reusable actions  
- Scope control: Server / Client / Any  
- Middleware, BeforeRun / AfterRun hooks  
- Async / Promise-based execution  
- Remote execution, cleanup, and abort  
- Built-in logging  
- Strict warnings for invalid targets or parameters

---

## Usage Examples

### Require the library
```lua
local Actions = require(game.ReplicatedStorage.UniversalAction.init)
```
### Basic NPC MoveTo
```lua
local npc = workspace:WaitForChild("NPC")
Actions:Do("NPC.MoveTo", npc, { Position = Vector3.new(0, 0, 0) })
```
### RandomWalk NPC
```lua
Actions:Do("NPC.RandomWalk", npc, {})
```

### Popup GUI on client
```lua
local gui = game.Players.LocalPlayer:WaitForChild("PlayerGui"):WaitForChild("ScreenGui")
Actions:Do("UI.Popup", gui, { Text = "Hello!", Duration = 2 })
       :andThen(function()
           print("Popup finished")
       end)
```
