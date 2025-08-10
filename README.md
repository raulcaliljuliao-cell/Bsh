-- SERVIÇOS E VARIÁVEIS
local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local player = Players.LocalPlayer
local PlayerGui = player:WaitForChild("PlayerGui")
local KEY_CORRETA = "la_grande"
local pos1, pos2, pos3, pos4 = nil, nil, nil, nil
local tweenEmExecucao = false
local VELOCIDADE_TELEGUIADO = 40
-- CORES NEON
local corFundo = Color3.fromRGB(20, 10, 0)
local corLaranjaNeon = Color3.fromRGB(255, 140, 0)
local corLaranjaEscuro = Color3.fromRGB(255, 110, 0)
local function criarNeon(frame)
local neon = Instance.new("UIStroke")
neon.Color = corLaranjaNeon
neon.Thickness = 2
neon.Transparency = 0.4
neon.Parent = frame
end
-- GUI DE KEY
local keyGui = Instance.new("ScreenGui")
keyGui.Name = "KeyGui"
keyGui.ResetOnSpawn = false
keyGui.Parent = PlayerGui
local keyFrame = Instance.new("Frame")
keyFrame.Size = UDim2.new(0, 280, 0, 160)
keyFrame.Position = UDim2.new(0.5, -140, 0.5, -80)
keyFrame.BackgroundColor3 = corFundo
keyFrame.Active = true
keyFrame.Draggable = true
keyFrame.Parent = keyGui
Instance.new("UICorner", keyFrame).CornerRadius = UDim.new(0, 12)
criarNeon(keyFrame)
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 40)
title.Position = UDim2.new(0, 0, 0, 10)
title.BackgroundTransparency = 1
title.Text = "🔑 Digite a Key:"
title.TextColor3 = corLaranjaEscuro
title.Font = Enum.Font.GothamBlack
title.TextSize = 24
title.Parent = keyFrame
local textBox = Instance.new("TextBox")
textBox.Size = UDim2.new(0.8, 0, 0, 40)
textBox.Position = UDim2.new(0.1, 0, 0, 60)
textBox.PlaceholderText = "Digite a key aqui..."
textBox.Text = ""
textBox.TextSize = 20
textBox.Font = Enum.Font.Gotham
textBox.TextColor3 = corLaranjaNeon
textBox.BackgroundColor3 = Color3.fromRGB(40, 20, 0)
textBox.Parent = keyFrame
Instance.new("UICorner", textBox).CornerRadius = UDim.new(0, 8)
criarNeon(textBox)
local confirmar = Instance.new("TextButton")
confirmar.Size = UDim2.new(0.8, 0, 0, 45)
confirmar.Position = UDim2.new(0.1, 0, 0, 110)
confirmar.Text = "Confirmar"
confirmar.Font = Enum.Font.GothamBlack
confirmar.TextSize = 22
confirmar.TextColor3 = corFundo
confirmar.BackgroundColor3 = corLaranjaNeon
confirma
