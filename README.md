# EvadeScripterV2
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local SpeedValue = 16
local Window = OrionLib:MakeWindow({Name = "EvadeScripter", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
local Tab = Window:MakeTab({
	Name = "Tab 1",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Tab:AddSection({
	Name = "Section : Evade"
})

Tab:AddSlider({
	Name = "Speed Modifier",
	Min = 16,
	Max = 500,
	Default = 16,
	Color = Color3.fromRGB(255,255,255),
	Increment = 5,
	ValueName = "Speed",
	Callback = function(Value)
		SpeedValue = Value
	end
})

Tab:AddButton({
	Name = "U to fly",
	Callback = function()
      		loadstring(game:HttpGet("https://pastebin.com/raw/qZkK3ZXy", true))()
      		OrionLib:MakeNotification({
	Name = "U To Fly CONTROLS",
	Content = "Press U to fly and while you are flying press J to speed up.",
	Image = "rbxassetid://4483345998",
	Time = 10
})
  	end    
})

local Tab = Window:MakeTab({
	Name = "Tab 2",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Tab:AddSection({
	Name = "Section : Visuals"
})

Tab:AddButton({
	Name = "ESP",
	Callback = function()
      		loadstring(game:HttpGet('https://raw.githubusercontent.com/ic3w0lf22/Unnamed-ESP/master/UnnamedESP.lua'))()
      		OrionLib:MakeNotification({
	Name = "ESP CONTROLS",
	Content = "Press F3 to dont see the esp lines and boxs and press F4 to dont see the things to modify the ESP.",
	Image = "rbxassetid://4483345998",
	Time = 15
})
  	end    
})

Tab:AddButton({
	Name = "Tickets ESP",
	Callback = function()
      		repeat wait() until game:IsLoaded() 
local camera = workspace.CurrentCamera


local function drawItem(item)
    local DropText = Drawing.new("Text")
    DropText.Visible = false
    DropText.Center = true
    DropText.Outline = true
    DropText.Font = 3
    DropText.Size = 16
    DropText.OutlineColor = Color3.fromRGB(0, 0, 0);
    DropText.Color = Color3.fromRGB(0, 255, 0)

    local function UPDATER()
        --declare the variables for the loop
        local c
        --Super fast loop
        c = game:GetService("RunService").RenderStepped:Connect(function()
            if item then
                local itemVector , onscree = camera:WorldToViewportPoint(item.Position)
                    if onscree then
                        DropText.Visible = true
                        DropText.Text = "Ticket"
                        DropText.Position = Vector2.new(itemVector.X, itemVector.Y+5)
                    else
                        DropText.Visible = false
                    end
                else 
                    DropText.Visible = false
            end
        end)--end loop
    end--end function updater
    coroutine.wrap(UPDATER)()
end


for i , v in pairs(game:GetService("Workspace"):GetDescendants())do
    if v.Parent == game:GetService("Workspace").Game.Effects.Tickets then
        drawItem(v.Mover)
    end
end
--on new thing added
game:GetService("Workspace").DescendantAdded:Connect(function(thing)
    if thing.Parent == game:GetService("Workspace").Game.Effects.Tickets then
        drawItem(thing.Mover)
    end
end) 
  	end    
})


game:GetService("RunService").RenderStepped:Connect(function()
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = SpeedValue
end)
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local SpeedValue = 16
local Window = OrionLib:MakeWindow({Name = "EvadeScripter", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
local Tab = Window:MakeTab({
	Name = "Tab 1",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Tab:AddSection({
	Name = "Section : Evade"
})

Tab:AddSlider({
	Name = "Speed Modifier",
	Min = 16,
	Max = 500,
	Default = 16,
	Color = Color3.fromRGB(255,255,255),
	Increment = 5,
	ValueName = "Speed",
	Callback = function(Value)
		SpeedValue = Value
	end
})

Tab:AddButton({
	Name = "U to fly",
	Callback = function()
      		loadstring(game:HttpGet("https://pastebin.com/raw/qZkK3ZXy", true))()
      		OrionLib:MakeNotification({
	Name = "U To Fly CONTROLS",
	Content = "Press U to fly and while you are flying press J to speed up.",
	Image = "rbxassetid://4483345998",
	Time = 10
})
  	end    
})

local Tab = Window:MakeTab({
	Name = "Tab 2",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Tab:AddSection({
	Name = "Section : Visuals"
})

Tab:AddButton({
	Name = "ESP",
	Callback = function()
      		loadstring(game:HttpGet('https://raw.githubusercontent.com/ic3w0lf22/Unnamed-ESP/master/UnnamedESP.lua'))()
      		OrionLib:MakeNotification({
	Name = "ESP CONTROLS",
	Content = "Press F3 to dont see the esp lines and boxs and press F4 to dont see the things to modify the ESP.",
	Image = "rbxassetid://4483345998",
	Time = 15
})
  	end    
})

Tab:AddButton({
	Name = "Tickets ESP",
	Callback = function()
      		repeat wait() until game:IsLoaded() 
local camera = workspace.CurrentCamera


local function drawItem(item)
    local DropText = Drawing.new("Text")
    DropText.Visible = false
    DropText.Center = true
    DropText.Outline = true
    DropText.Font = 3
    DropText.Size = 16
    DropText.OutlineColor = Color3.fromRGB(0, 0, 0);
    DropText.Color = Color3.fromRGB(0, 255, 0)

    local function UPDATER()
        --declare the variables for the loop
        local c
        --Super fast loop
        c = game:GetService("RunService").RenderStepped:Connect(function()
            if item then
                local itemVector , onscree = camera:WorldToViewportPoint(item.Position)
                    if onscree then
                        DropText.Visible = true
                        DropText.Text = "Ticket"
                        DropText.Position = Vector2.new(itemVector.X, itemVector.Y+5)
                    else
                        DropText.Visible = false
                    end
                else 
                    DropText.Visible = false
            end
        end)--end loop
    end--end function updater
    coroutine.wrap(UPDATER)()
end


for i , v in pairs(game:GetService("Workspace"):GetDescendants())do
    if v.Parent == game:GetService("Workspace").Game.Effects.Tickets then
        drawItem(v.Mover)
    end
end
--on new thing added
game:GetService("Workspace").DescendantAdded:Connect(function(thing)
    if thing.Parent == game:GetService("Workspace").Game.Effects.Tickets then
        drawItem(thing.Mover)
    end
end) 
  	end    
})


game:GetService("RunService").RenderStepped:Connect(function()
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = SpeedValue
end)
