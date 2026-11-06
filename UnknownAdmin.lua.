
-- UNKNOWN ADMIN PANEL
-- Black & Purple Theme

local Players = game:GetService("Players")
local player = Players.LocalPlayer

local gui = Instance.new("ScreenGui")
gui.Name = "UNKNOWN_ADMIN"
gui.ResetOnSpawn = false
gui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.fromOffset(250, 400)
frame.Position = UDim2.new(0.5, -125, 0.3, 0)
frame.BackgroundColor3 = Color3.fromRGB(12, 12, 16)
frame.BorderColor3 = Color3.fromRGB(160, 70, 255)
frame.Parent = gui

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 45)
title.Text = "UNKNOWN ADMIN"
title.TextColor3 = Color3.fromRGB(190, 120, 255)
title.BackgroundColor3 = Color3.fromRGB(25, 15, 35)
title.Font = Enum.Font.GothamBold
title.TextSize = 18
title.Parent = frame

local function addButton(name, y, callback)
    local b = Instance.new("TextButton")
    b.Size = UDim2.new(0.9, 0, 0, 34)
    b.Position = UDim2.new(0.05, 0, 0, y)
    b.BackgroundColor3 = Color3.fromRGB(45, 25, 65)
    b.TextColor3 = Color3.new(1, 1, 1)
    b.Font = Enum.Font.GothamBold
    b.Text = name
    b.Parent = frame
    b.MouseButton1Click:Connect(callback)
end

local function getHumanoid()
    local character = player.Character
    return character and character:FindFirstChildOfClass("Humanoid")
end

addButton("Speed", 55, function()
    local h = getHumanoid()
    if h then h.WalkSpeed = 32 end
end)

addButton("Super Jump", 95, function()
    local h = getHumanoid()
    if h then
        h.UseJumpPower = true
        h.JumpPower = 100
    end
end)

addButton("Reset Speed", 135, function()
    local h = getHumanoid()
    if h then h.WalkSpeed = 16 end
end)

addButton("Reset Character", 175, function()
    player:LoadCharacter()
end)

addButton("Close Panel", 215, function()
    gui:Destroy()
end)
