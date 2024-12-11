
# Kinx UI 使用文档

这是一个完整的 Kinx UI 示例代码文档，展示了如何添加各种控件。

---

## 初始化 UI

```lua
local lib = loadstring(game:HttpGet("https://github.com/XiaoYunCN/UWU/raw/main/Library%2FKinxui.lua"))()

local win = lib:Window("Kinx ui", Color3.fromRGB(44, 120, 224), Enum.KeyCode.RightControl)
```

---

## 添加标签页

```lua
local tab = win:Tab("Tab 1")
```

---

## 添加按钮

```lua
tab:Button("Button", function()
    lib:Notification("Notification", "Hello!", "Hi!")
end)

tab:Button("Button", function()
    print("Hello!")
end)
```

---

## 添加开关

```lua
tab:Toggle("Toggle", false, function(t)
    print(t)
end)
```

---

## 添加滑块

```lua
tab:Slider("Slider", 0, 100, 30, function(value)
    print("当前滑块值为: " .. value)
end)
```

---

## 添加下拉菜单

```lua
tab:Dropdown("Dropdown", {"Option 1", "Option 2", "Option 3", "Option 4", "Option 5"}, function(option)
    print("当前选择: " .. option)
end)
```

---

## 添加颜色选择器

```lua
tab:Colorpicker("Colorpicker", Color3.fromRGB(255, 0, 0), function(color)
    print("当前颜色为: ", color)
end)
```

---

## 添加文本框

```lua
tab:Textbox("Textbox", true, function(text)
    print("输入内容: " .. text)
end)
```

---

## 添加按键绑定

```lua
tab:Bind("Bind", Enum.KeyCode.RightShift, function()
    print("按键被触发!")
end)
```

---

## 添加标签

```lua
tab:Label("Label")
```

---

## 更改 UI 颜色

```lua
local changeclr = win:Tab("Change UI Color")

changeclr:Colorpicker("Change UI Color", Color3.fromRGB(44, 120, 224), function(color)
    lib:ChangePresetColor(Color3.fromRGB(color.R * 255, color.G * 255, color.B * 255))
end)
```

---

## 示例代码整合

完整代码如下：

```lua
local lib = loadstring(game:HttpGet("https://github.com/XiaoYunCN/UWU/raw/main/Library%2FKinxui.lua"))()

local win = lib:Window("Kinx ui", Color3.fromRGB(44, 120, 224), Enum.KeyCode.RightControl)

local tab = win:Tab("Tab 1")

tab:Button("Button", function()
    lib:Notification("Notification", "Hello!", "Hi!")
end)

tab:Button("Button", function()
    print("Hello!")
end)

tab:Toggle("Toggle", false, function(t)
    print(t)
end)

tab:Slider("Slider", 0, 100, 30, function(value)
    print("当前滑块值为: " .. value)
end)

tab:Dropdown("Dropdown", {"Option 1", "Option 2", "Option 3", "Option 4", "Option 5"}, function(option)
    print("当前选择: " .. option)
end)

tab:Colorpicker("Colorpicker", Color3.fromRGB(255, 0, 0), function(color)
    print("当前颜色为: ", color)
end)

tab:Textbox("Textbox", true, function(text)
    print("输入内容: " .. text)
end)

tab:Bind("Bind", Enum.KeyCode.RightShift, function()
    print("按键被触发!")
end)

tab:Label("Label")

local changeclr = win:Tab("Change UI Color")

changeclr:Colorpicker("Change UI Color", Color3.fromRGB(44, 120, 224), function(color)
    lib:ChangePresetColor(Color3.fromRGB(color.R * 255, color.G * 255, color.B * 255))
end)
```
