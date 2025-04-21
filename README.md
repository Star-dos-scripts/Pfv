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
      		-- Script para deixar o modelo "001_BurgerBarn" transparente

-- Primeiro, localiza o modelo na workspace
local burgerBarn = workspace:FindFirstChild("001_BurgerBarn")

-- Verifica se o modelo existe
if burgerBarn then
    -- Percorre todos os descendentes do modelo
    for _, part in ipairs(burgerBarn:GetDescendants()) do
        -- Verifica se é uma peça que pode ficar transparente
        if part:IsA("BasePart") then
            part.Transparency = 1
            part.CanCollide = false -- opcional: desativa colisão também
        end
    end
else
    warn("Modelo '001_BurgerBarn' não encontrado!")
end
  	end    
})

