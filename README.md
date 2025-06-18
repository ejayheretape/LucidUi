# LucidUi
# 🌙 LucidUI
A clean, minimal, and easily customizable Roblox UI Library made for script developers.  
LucidUI supports tabbed interfaces, buttons, toggles, and even custom Lua code execution — perfect for executors or advanced script GUIs.

---

## 📦 Features

- 🎯 Tab system for organizing scripts  
- 🟢 Buttons with hover effects  
- ✅ Toggle support with callbacks  
- 🧠 Lua code execution window (`loadstring`)  
- ✨ Stylish, minimal dark UI with rounded corners  
- 🧱 Zero dependencies – just pure Roblox Lua  

---

## 📁 How to Use

1. **Load the library:**
   ```lua
   local LucidUI = loadstring(game:HttpGet("https://raw.githubusercontent.com/YOUR_USERNAME/LucidUI/main/LucidUI.lua"))()
   ```

2. **Create a window:**
   ```lua
   local win = LucidUI:CreateWindow("Lucid Executor")
   ```

3. **Add a tab:**
   ```lua
   local mainTab = win:CreateTab("Main")
   ```

4. **Add a button:**
   ```lua
   mainTab:AddButton("Click Me", function()
       print("You clicked the button!")
   end)
   ```

5. **Add a toggle:**
   ```lua
   mainTab:AddToggle("God Mode", false, function(state)
       print("God Mode:", state)
   end)
   ```

6. **Add a code executor:**
   ```lua
   mainTab:AddCodeBox("Paste your Lua code here...")
   ```

---

## 🛠 Adding More Features

You can extend LucidUI by adding:

- Sliders  
- Dropdowns  
- Text inputs  
- Notifications or Popups  
- Theme customization  

Open `LucidUI.lua` and add new widget functions under `tabAPI`, following the style of `AddButton`, `AddToggle`, etc.

---

## 🧪 Sample Script

```lua
local LucidUI = loadstring(game:HttpGet("https://raw.githubusercontent.com/YOUR_USERNAME/LucidUI/main/LucidUI.lua"))()
local win = LucidUI:CreateWindow("Lucid Tester")

local tab = win:CreateTab("Tools")

tab:AddButton("Print Hello", function()
   print("Hello from LucidUI!")
end)

tab:AddToggle("Auto-Farm", false, function(state)
   print("Auto-Farm Enabled:", state)
end)

tab:AddCodeBox("Type your Lua code here...")
```

---

## ⚠️ Disclaimer

This is a **client-side UI library**, meant for testing, development, and scripting purposes.  
Running code through `loadstring()` can be dangerous — **never run unknown or obfuscated code**.

---

## 📄 License

MIT License – You can modify and use it however you want. Please give credit if you make public versions.

---

## 💬 Credits

Created by **DevX(Me)**  
Inspired by Rayfield and KavoUI, but fully original and clean.
