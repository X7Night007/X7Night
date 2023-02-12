local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Rock Fruit", "Ocean")

--// Main Tab
local Main = Window:NewTab("Abilities")
local MainSection = Main:NewSection("One Punch Abilities")

--// Buttons
MainSection:NewButton("Normal Punch", "Uses One Punch Man's First ability", function()
    
local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").OnePunch.Client:FireServer(unpack(args))

end)

MainSection:NewButton("Ground Punch", "Uses One Punch Man's Second ability", function()
    
local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").OnePunch.Client2:FireServer(unpack(args))

end)

MainSection:NewButton("Serious Punch", "Uses One Punch Man's Final ability", function()
    
local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").OnePunch.Client3:FireServer(unpack(args))

end)

MainSection:NewButton("Jet Pistol", "Uses Rubber's First ability", function()
    
local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").Rubber.RubberEvent:FireServer(unpack(args))

end)

MainSection:NewButton("Bazooka", "Uses Rubber's Second ability", function()
    
local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").Rubber.BazookaEvent:FireServer(unpack(args))

end)

MainSection:NewButton("Jet Gatling", "Uses Rubber's Final ability", function()
    
local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").Rubber.GatlingEvent:FireServer(unpack(args))

end)

--// Keybinds
local Keybind = Window:NewTab("Keybinds")
local KeybindSection = Keybind:NewSection("Keybinds")

KeybindSection:NewKeybind("Serious Punch", "One Punch Final Move Keybind", Enum.KeyCode.G, function()

local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").OnePunch.Client3:FireServer(unpack(args))

end)

KeybindSection:NewKeybind("Jet Gatling", "Rubber Final Move Keybind", Enum.KeyCode.B, function()

local args = {
    [1] = 1
}

game:GetService("ReplicatedStorage").Rubber.GatlingEvent:FireServer(unpack(args))

end)

--// UI Tab
local UI = Window:NewTab("UI")
local UISection = UI:NewSection("UI Toggle Keybind")

UISection:NewKeybind("UI Keybind", "Button to Open/Close the UI", Enum.KeyCode.LeftAlt, function()
	Library:ToggleUI()
end)
