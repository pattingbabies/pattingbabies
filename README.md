local library = loadstring(game:HttpGet(('https://raw.githubusercontent.com/AikaV3rm/UiLib/master/Lib.lua')))()

local w = library:CreateWindow("Navy Simulator") -- Creates the window


local a = w:CreateFolder("GUI")
local b = w:CreateFolder("Teleports")
local c = w:CreateFolder("Extra")

b:Button("Bank Guard Spawn",function()
    local New_CFrame = game:GetService("Workspace").Islands.Bank.EssentialWorkers.TeleportPositions.BankGuard.CFrame

local ts = game:GetService('TweenService')
local char = game.Players.LocalPlayer.Character

local part = char.HumanoidRootPart
local ti = TweenInfo.new(10, Enum.EasingStyle.Linear)
local tp = {CFrame = New_CFrame}
ts:Create(part, ti, tp):Play()
end)

b:Button("Vault",function()
    local New_CFrame = game:GetService("Workspace").Zones.BankVault.Vault.CFrame

    local ts = game:GetService('TweenService')
    local char = game.Players.LocalPlayer.Character
    
    local part = char.HumanoidRootPart
    local ti = TweenInfo.new(10, Enum.EasingStyle.Linear)
    local tp = {CFrame = New_CFrame}
    ts:Create(part, ti, tp):Play()
end)


b:Button("Sea Ship Spawn",function()
    local New_CFrame = game:GetService("Workspace").SEAShipSpawns.CFrame

    local ts = game:GetService('TweenService')
    local char = game.Players.LocalPlayer.Character
    
    local part = char.HumanoidRootPart
    local ti = TweenInfo.new(15, Enum.EasingStyle.Linear)
    local tp = {CFrame = New_CFrame}
    ts:Create(part, ti, tp):Play()
end)

b:Button("Pirate Ship Spawn",function()
    local New_CFrame = CFrame.new(293, 47, -5546)

    local ts = game:GetService('TweenService')
    local char = game.Players.LocalPlayer.Character
    
    local part = char.HumanoidRootPart
    local ti = TweenInfo.new(10, Enum.EasingStyle.Linear)
    local tp = {CFrame = New_CFrame}
    ts:Create(part, ti, tp):Play()
    
end)

c:Button("bypass anti-cheat",function()
    while wait() do
        local args = {
        [1] = false
    }
    
    game:GetService("ReplicatedStorage").Framework.Events.SwimState:FireServer(unpack(args))
   end 
end)

c:Button("Sea Military Team",function()

    local args = {
        [1] = game:GetService("Teams"):FindFirstChild("SEA Military")
    }
    
    game:GetService("ReplicatedStorage").TeamChanged:FireServer(unpack(args))


  
end)

if is_synapse_function then
    messagebox("discord.gg/vDhatuGQzn","Discord",0)
end

a:DestroyGui()
