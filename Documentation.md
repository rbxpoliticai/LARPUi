Here’s the documentation with double quotes as requested:

# LARP UI Library
This documentation covers the usage of the LARP UI Library.

## Booting the Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/rbxpoliticai/LARPUi/refs/heads/main/Main.lua", true))()
Library:Settings("Library Name", "1.0", Color3.fromRGB(91, 133, 197))
```

## Creating a Window
```lua
local Legit = Library:AddWindow("Legit")
```

- **AddWindow** creates a new window in the UI.
  - "Legit" is the name of the window.

---

## Creating a Section
```lua
local Home = Legit:AddSection("All Features")
```

- **AddSection** adds a new section within a window.
  - "All Features" is the name of the section.

---

## Adding a Label
```lua
Home:AddLabel("Template Label")
```

- **AddLabel** adds a label to the section.
  - "Template Label" is the text displayed by the label.

---

## Creating a Button
```lua
Home:AddButton("Test Button", false, nil, function() 
  print("a") 
end)
```

- **AddButton** creates a clickable button.
  - "Test Button" is the text on the button.
  - The `Callback` function is executed when the button is clicked, printing "a".

---

## Creating a Toggle
```lua
Home:AddToggle("Testing Toggle", true, Enum.KeyCode.LeftControl, function(v)
    print(v)
end)
```

- **AddToggle** creates a toggle switch.
  - "Testing Toggle" is the name of the toggle.
  - The default value is set to `true`.
  - `Enum.KeyCode.LeftControl` is the keybind to activate/deactivate the toggle.
  - The `Callback` function will print `true` or `false` depending on the toggle state.

---

## Creating a Slider
```lua
Home:AddSlider("Template Slider", 100, 10, 50, function(c) 
  print(c)
end)
```

- **AddSlider** creates a slider control.
  - "Template Slider" is the name of the slider.
  - `100` is the maximum value.
  - `10` is the minimum value.
  - `50` is the default value.
  - The `Callback` function prints the current slider value.

---

## Adding a Keybind
```lua
Home:AddKeyBind("Template Keybind", Enum.KeyCode.Y, function() 
    -- Toggle visibility of watermark
    if watermark:Visible() then
        watermark:Visible(false)
    else
        watermark:Visible(true)
    end
end)
```

- **AddKeyBind** adds a keybind that toggles the visibility of the UI or watermark.
  - "Template Keybind" is the name of the keybind.
  - `Enum.KeyCode.Y` is the default key for the keybind.
  - The `Callback` function is executed when the keybind is pressed, toggling the visibility of the watermark.

---

## Creating a Color Picker
```lua
Home:AddColorPallete("Testing Color Pallete", Color3.fromRGB(89, 125, 255), function(a) 
  print(a)
end)
```

- **AddColorPallete** creates a color picker.
  - "Testing Color Pallete" is the name of the color picker.
  - `Color3.fromRGB(89, 125, 255)` is the default color.
  - The `Callback` function prints the selected color.

---

## Adding a TextBox
```lua
Home:AddTextBox("No Filter", nil, false, 5, function(a) 
    print(a)
end)
```

- **AddTextBox** adds a text box for user input.
  - "No Filter" is the name of the text box.
  - The `Callback` function prints the inputted text.
  - **Different filters**: You can restrict input to numbers or certain characters by modifying the fourth argument.

---

## Creating a Dropdown Menu
```lua
Home:AddDropdown("Testing Dropdown", {"opt1", "opt2", "opt3"}, "opt2", function(a) 
  print(a)
end)
```

- **AddDropdown** creates a dropdown selection menu.
  - "Testing Dropdown" is the name of the dropdown.
  - `{ "opt1", "opt2", "opt3" }` defines the options in the dropdown.
  - "opt2" is the default selected option.
  - The `Callback` function prints the selected option.

---

## Adding a Separator Bar
```lua
Home:AddSeparateBar()
```

- **AddSeparateBar** creates a simple separator bar for better UI organization.

---

## Adding a Watermark
```lua
local watermark = Library:AddWatermark("")
watermark:ChangeText("Watermark Text")
```
