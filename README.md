-- Criando a GUI do Menu
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Feito por Swiz"
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 400, 0, 400)
frame.Position = UDim2.new(0.5, -200, 0.5, -200)
frame.BackgroundColor3 = Color3.new(0, 0, 0)
frame.BackgroundTransparency = 0.5
frame.Draggable = true
frame.Active = true
frame.DraggableSpeed = 2 -- Aumentar a velocidade do arrasto
frame.Parent = screenGui

local titleLabel = Instance.new("TextLabel")
titleLabel.Size = UDim2.new(1, 0, 0.1, 0)
titleLabel.Position = UDim2.new(0, 0, 0, 0)
titleLabel.Text = "DESTRUIR MINI CITY HAHA - Feito por Swiz"
titleLabel.TextColor3 = Color3.new(1, 1, 1)
titleLabel.BackgroundTransparency = 1
titleLabel.TextScaled = true
titleLabel.Parent = frame

local tab1Button = Instance.new("TextButton")
tab1Button.Size = UDim2.new(0.5, 0, 0.1, 0)
tab1Button.Position = UDim2.new(0, 0, 0.1, 0)
tab1Button.Text = "Tab 1"
tab1Button.TextScaled = true
tab1Button.Parent = frame

local tab2Button = Instance.new("TextButton")
tab2Button.Size = UDim2.new(0.5, 0, 0.1, 0)
tab2Button.Position = UDim2.new(0.5, 0, 0.1, 0)
tab2Button.Text = "Tab 2"
tab2Button.TextScaled = true
tab2Button.Parent = frame

local tab1Content = Instance.new("Frame")
tab1Content.Size = UDim2.new(1, 0, 0.8, 0)
tab1Content.Position = UDim2.new(0, 0, 0.2, 0)
tab1Content.BackgroundTransparency = 1
tab1Content.Visible = true
tab1Content.Parent = frame

local tab2Content = Instance.new("Frame")
tab2Content.Size = UDim2.new(1, 0, 0.8, 0)
tab2Content.Position = UDim2.new(0, 0, 0.2, 0)
tab2Content.BackgroundTransparency = 1
tab2Content.Visible = false
tab2Content.Parent = frame

tab1Button.MouseButton1Click:Connect(function()
    tab1Content.Visible = true
    tab2Content.Visible = false
end)

tab2Button.MouseButton1Click:Connect(function()
    tab1Content.Visible = false
    tab2Content.Visible = true
end)

local flyButton = Instance.new("TextButton")
flyButton.Size = UDim2.new(1, 0, 0.1, 0)
flyButton.Position = UDim2.new(0, 0, 0, 0)
flyButton.Text = "Ativar Voo"
flyButton.TextScaled = true
flyButton.Parent = tab1Content

local espButton = Instance.new("TextButton")
espButton.Size = UDim2.new(1, 0, 0.1, 0)
espButton.Position = UDim2.new(0, 0, 0.1, 0)
espButton.Text = "Ativar ESP"
espButton.TextScaled = true
espButton.Parent = tab1Content

local noclipButton = Instance.new("TextButton")
noclipButton.Size = UDim2.new(1, 0, 0.1, 0)
noclipButton.Position = UDim2.new(0, 0, 0.2, 0)
noclipButton.Text = "Ativar Noclip"
noclipButton.TextScaled = true
noclipButton.Parent = tab1Content

local speedLabel = Instance.new("TextLabel")
speedLabel.Size = UDim2.new(1, 0, 0.1, 0)
speedLabel.Position = UDim2.new(0, 0, 0.3, 0)
speedLabel.Text = "Velocidade de Voo"
speedLabel.TextColor3 = Color3.new(1, 1, 1)
speedLabel.BackgroundTransparency = 1
speedLabel.TextScaled = true
speedLabel.Parent = tab1Content

local speedBox = Instance.new("TextBox")
speedBox.Size = UDim2.new(1, 0, 0.1, 0)
speedBox.Position = UDim2.new(0, 0, 0.4, 0)
speedBox.Text = "50"
speedBox.TextScaled = true
speedBox.Parent = tab1Content

local antFallDamageButton = Instance.new("TextButton")
antFallDamageButton.Size = UDim2.new(1, 0, 0.1, 0)
antFallDamageButton.Position = UDim2.new(0, 0, 0, 0)
antFallDamageButton.Text = "Ativar Ant Dano de Queda"
antFallDamageButton.TextScaled = true
antFallDamageButton.Parent = tab2Content

-- Adicionando o script fornecido ao Tab 2
local aimConfigSection = Instance.new("Frame")
aimConfigSection.Size = UDim2.new(1, 0, 0.2, 0)
aimConfigSection.Position = UDim2.new(0, 0, 0.1, 0)
aimConfigSection.BackgroundTransparency = 1
aimConfigSection.Parent = tab2Content

local aimConfigLabel = Instance.new("TextLabel")
aimConfigLabel.Size = UDim2.new(1, 0, 0.2, 0)
aimConfigLabel.Position = UDim2.new(0, 0, 0, 0)
aimConfigLabel.Text = "aim config"
aimConfigLabel.TextColor3 = Color3.new(1, 1, 1)
aimConfigLabel.BackgroundTransparency = 1
aimConfigLabel.TextScaled = true
aimConfigLabel.Parent = aimConfigSection

-- Toggle para habilitar/desabilitar o Aimbot
Tab:CreateToggle({
    Name = "ativar aimbot",
    CurrentValue = getgenv().Aimbot.Settings.Enabled == true, -- Garante que seja true ou false
    Flag = "AimbotEnabled",
    Callback = function(Value)
        getgenv().Aimbot.Settings.Enabled = Value
    end
})

-- Toggle para checar se o jogador está vivo
Tab:CreateToggle({
    Name = "vivo check",
    CurrentValue = getgenv().Aimbot.Settings.AliveCheck == true, -- Garante que seja true ou false
    Flag = "AliveCheck",
    Callback = function(Value)
        getgenv().Aimbot.Settings.AliveCheck = Value
    end
})

-- Script de Voo com Animação
local flySpeed = 50
local flyEnabled = false
local flyingConnection
local flyingAnim

local function startFlying()
    local character = game.Players.LocalPlayer.Character
    if character then
        local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
        local bodyVelocity = Instance.new("BodyVelocity")
        bodyVelocity.Velocity = Vector3.new(0, flySpeed, 0)
        bodyVelocity.Parent = humanoidRootPart

        flyingAnim = character:WaitForChild("Humanoid"):LoadAnimation(Instance.new("Animation", {AnimationId = "rbxassetid://YourAnimationID"}))
        flyingAnim:Play()

        flyingConnection = game:GetService("RunService").RenderStepped:Connect(function()
            humanoidRootPart.Velocity = humanoidRootPart.CFrame.lookVector * flySpeed
        end)
    end
end

local function stopFlying()
    local character = game.Players.LocalPlayer.Character
    if character then
        local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
        if humanoidRootPart:FindFirstChild("BodyVelocity") then
            humanoidRootPart.BodyVelocity:Destroy()
        end

        if flyingAnim then
            flyingAnim:Stop()
            flyingAnim = nil
        end

        if flyingConnection then
            flyingConnection:Disconnect()
            flyingConnection = nil
        end
    end
end

flyButton.MouseButton1Click:Connect(function()
    flySpeed = tonumber(speedBox.Text) or 50
    flyEnabled = not flyEnabled
    if flyEnabled then
        flyButton.Text = "Desativar Voo"
        startFlying()
    else
        flyButton.Text = "Ativar Voo"
        stopFlying()
    end
end)
