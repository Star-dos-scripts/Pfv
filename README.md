local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/jensonhirst/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Sumiço", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
local Tab = Window:MakeTab({
	Name = "Visual",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
Tab:AddButton({
	Name = "Button!",
	Callback = function()
-- Script para teleportar o jogador até o "003_CouchGiveTool"

local target = workspace:FindFirstChild("003_CouchGiveTool")

if target and target:IsA("BasePart") then
    -- Teleporta o jogador local (em exploits geralmente é game.Players.LocalPlayer)
    local player = game.Players.LocalPlayer
    if player and player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
        player.Character.HumanoidRootPart.CFrame = target.CFrame + Vector3.new(0, 5, 0)
        -- O + Vector3.new(0, 5, 0) evita que o jogador fique preso no chão
    end
else
    warn("Objeto '003_CouchGiveTool' não encontrado ou não é uma peça válida!")
end
  	end    
})

