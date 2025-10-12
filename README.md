# ↔️ Pehkui Figura

A Figura library that allows models to send Pehkui and P4A scaling commands, as well as toggling scaling

## ⚙️ Features

- **Pehkui and Pehkui4All compatibility**: automatically send Pehkui or P4A commands depending on which mod is installed.
- **Scaling preferences via config**: set which scaling option the script is supposed to change.

## 🛠️ Installation

1. Download both [`Pehkui.lua`](https://github.com/nexidict/Pehkui-Figura/blob/main/Pehkui.lua) and [`Queue.lua`](https://github.com/nexidict/Pehkui-Figura/blob/main/Queue.lua) and drop them in your Figura project! **Both files are necessary for the script to work.**

2. Import the library:

    ```lua
    local adipose = require('Adipose')
    ```

3. In Minecraft, open the pause menu, and click on the Figura icon. Click on the settings tab, and search for **Chat Messages** under the **Dev** section, and enable it.

4. Done!

Now you can make your model send Pehkui/P4A commands for you, this by using the provided functions listed below.

## 📃 Functions

### Pehkui Figura

### Require

Import the Pehkui script.

**Example:**

```lua
local pehkui = require("Pehkui")
```

### Flags

#### `setScaleState()`

Sets the state of a flag. 

Setting a scaling option to false will make the script ignore that scaling option, even if this has been passed through `setScale`.

**Parameters:**

Name | Type | Description
---  | ---  | ---
scale | `String` | The scaling option as string
state | `Boolean` | Whether the script should scale this option

**Example:**

```lua
pehkui.setScale("pehkui:motion", false)
```

### Scaling

#### `setScale()`

Sends a Pehkui or P4A command with the provided values.

**Parameters:**

Name | Type | Description
---  | ---  | ---
scale | `String` | The scaling option as string
value | `Number` | The value of the scaling option
forceScaling | `Boolean` | If `true`, forces the function to push a command regardless of the flag state

**Example:**

```lua
pehkui.setScale("pehkui:motion", 0.8)
```