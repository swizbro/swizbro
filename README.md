-- Criando a GUI do Menu
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Feito por Swiz"
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 400, 0, 300)
frame.Position = UDim2.new(0.5, -200, 0.5, -150)
frame.BackgroundColor3 = Color3.new(0, 0, 0)
frame.BackgroundTransparency = 0.5
frame.Draggable = true
frame.Active = true
frame.Parent = screenGui

local titleLabel = Instance.new("TextLabel")
titleLabel.Size = UDim2.new(1, 0, 0.1, 0)
titleLabel.Position = UDim2.new(0, 0, 0, 0)
titleLabel.Text = "DESTRUIR MINI CITY HAHA - Feito por Swiz"
titleLabel.TextColor3 = Color3.new(1, 1, 1)
titleLabel.BackgroundTransparency = 1
titleLabel.TextScaled = true
titleLabel.Parent = frame

local flyButton = Instance.new("TextButton")
flyButton.Size = UDim2.new(1, 0, 0.3, 0)
flyButton.Position = UDim2.new(0, 0, 0.1, 0)
flyButton.Text = "Ativar Voo"
flyButton.TextScaled = true
flyButton.Parent = frame

local espButton = Instance.new("TextButton")
espButton.Size = UDim2.new(1, 0, 0.3, 0)
espButton.Position = UDim2.new(0, 0, 0.4, 0)
espButton.Text = "Ativar ESP"
espButton.TextScaled = true
espButton.Parent = frame

local noclipButton = Instance.new("TextButton")
noclipButton.Size = UDim2.new(1, 0, 0.3, 0)
noclipButton.Position = UDim2.new(0, 0, 0.7, 0)
noclipButton.Text = "Ativar Noclip"
noclipButton.TextScaled = true
noclipButton.Parent = frame

-- Script de Voo
local flySpeed = 50
local flyEnabled = false
local flyingConnection

local function startFlying()
    local character = game.Players.LocalPlayer.Character
    if character then
        local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
        local bodyVelocity = Instance.new("BodyVelocity")
        bodyVelocity.Velocity = Vector3.new(0, flySpeed, 0)
        bodyVelocity.Parent = humanoidRootPart

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

        if flyingConnection then
            flyingConnection:Disconnect()
            flyingConnection = nil
        end
    end
end

flyButton.MouseButton1Click:Connect(function()
    flyEnabled = not flyEnabled
    if flyEnabled then
        flyButton.Text = "Desativar Voo"
        startFlying()
    else
        flyButton.Text = "Ativar Voo"
        stopFlying()
    end
end)

-- Script de ESP
local espEnabled = false

local function createESP(player)
    if player.Character then
        local highlight = Instance.new("BoxHandleAdornment")
        highlight.Size = player.Character.HumanoidRootPart.Size
        highlight.Adornee = player.Character.HumanoidRootPart
        highlight.Color3 = Color3.new(0, 1, 0) -- Cor da caixa (verde)
        highlight.Transparency = 0.5
        highlight.AlwaysOnTop = true
        highlight.Parent = player.Character.HumanoidRootPart

        -- Criar um BillboardGui para mostrar a distância
        local billboardGui = Instance.new("BillboardGui")
        billboardGui.Adornee = player.Character.HumanoidRootPart
        billboardGui.Size = UDim2.new(0, 100, 0, 50)
        billboardGui.StudsOffset = Vector3.new(0, 3, 0)
        billboardGui.AlwaysOnTop = true
        billboardGui.Parent = player.Character.HumanoidRootPart

        local textLabel = Instance.new("TextLabel")
        textLabel.Size = UDim2.new(1, 0, 1, 0)
        textLabel.BackgroundTransparency = 1
        textLabel.TextColor3 = Color3.new(1, 0, 0) -- Cor do texto (vermelho)
        textLabel.TextScaled = true
        textLabel.Parent = billboardGui

        -- Função para atualizar a distância
        local function updateDistance()
            local distance = (player.Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            textLabel.Text = string.format("%.1f studs", distance)
        end

        -- Atualizar a distância a cada quadro
        game:GetService("RunService").RenderStepped:Connect(updateDistance)
    end
end

local function enableESP()
    for _, player in pairs(game.Players:GetPlayers()) do
        createESP(player)
    end

    game.Players.PlayerAdded:Connect(function(player)
        player.CharacterAdded:Connect(function()
            createESP(player)
        end)
    end)
end

espButton.MouseButton1Click:Connect(function()
    espEnabled = not espEnabled
    if espEnabled then
        espButton.Text = "Desativar ESP"
        enableESP()
    else
        espButton.Text = "Ativar ESP"
        -- Para desativar ESP, você precisaria remover os adornos e labels adicionados, isso pode ser feito com um script adicional.
    end
end)

-- Script de Noclip (atravessar paredes)
local noclipEnabled = false

local function startNoclip()
    local character = game.Players.LocalPlayer.Character
    if character then
        for _, part in pairs(character:GetDescendants()) do
            if part:IsA("BasePart") and part.CanCollide then
                part.CanCollide = false
            end
        end
    end
end

local function stopNoclip()
    local character = game.Players.LocalPlayer.Character
    if character then
        for _, part in pairs(character:GetDescendants()) do
            if part:IsA("BasePart") then
                part.CanCollide = true
            end
        end
    end
end

noclipButton.MouseButton1Click:Connect(function()
    noclipEnabled = not noclipEnabled
    if noclipEnabled then
        noclipButton.Text = "Desativar Noclip"
        startNoclip()
    else
        noclipButton.Text = "Ativar Noclip"
        stopNoclip()
    end
end)local Section11 = Tab:CreateSection("aim config")
-- Toggle para habilitar/desabilitar o Aimbot
Tab:CreateToggle({
    Name = "ativar aimbot",
    CurrentValue = getgenv().Aimbot.Settings.Enabled == true, -- Garante que seja true ou false
    Flag = "AimbotEnabled",
    Callback = function(Value)
        getgenv().Aimbot.Settings.Enabled = Value
    end,
})

-- Toggle para checar se o jogador estÃ¡ vivo
Tab:CreateToggle({
    Name = "vivo check",
    CurrentValue = getgenv().Aimbot.Settings.AliveCheck == true, -- Garante que seja true ou false
    Flag = "AliveCheck",
    Callback = function(Value)
        getgenv().Aimbot.Settings.AliveCheck = Value
    end,
