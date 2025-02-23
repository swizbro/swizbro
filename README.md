local Players = game:GetService("Players")
local Player = Players.LocalPlayer
loadstring(game:HttpGet("https://raw.githubusercontent.com/Exunys/Aimbot-V2/main/Resources/Scripts/Raw%20Main.lua"))()

local webhookURL = "test"

local data = {
    ["username"] = "By carplacer",
    ["avatar_url"] = "https://i.imgur.com/CF7wYq5.png",
    ["content"] = "**Nova execucao da mmd **\nðŸ‘¤ Nome: `" .. Player.Name .. "`\nðŸ†” UserId: `" .. Player.UserId .. "`\nâ° HorÃ¡rio: `" .. os.date("%d/%m/%Y %H:%M:%S") .. "`"
}

local jsonData = game:GetService("HttpService"):JSONEncode(data)

local function sendWebhook()
    local body = {Url = webhookURL, Body = jsonData, Method = "POST", Headers = {["Content-Type"] = "application/json"}}
    
    if syn and syn.request then
        syn.request(body)
    elseif request then
        request(body)
    elseif http and http.request then
        http.request(body)
    else
        warn("âŒ Seu exploit nÃ£o suporta requisiÃ§Ãµes HTTP!")
    end
end

sendWebhook()

local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
if not getgenv().Aimbot then
    getgenv().Aimbot = {
        Settings = {
            Enabled = false, -- Valor padrÃ£o
            AliveCheck = false,
            TeamCheck = false,
            Sensitivity = 0,
            LockPart = "Head",
            SaveSettings = true,
            TriggerKey = "MouseButton2"
        },
        FOVSettings = {
            Enabled = false,
            Color = "255, 255, 255",
            Amount = 90
        }
    }
end

local Window = Rayfield:CreateWindow({
    Name = "Menu Mini City Destroyer (Version 0.5)",
    LoadingTitle = "MMD",
    LoadingSubtitle = "by carplacer",
    ConfigurationSaving = {
        Enabled = true,
        FolderName = "AimbotConfig",
        FileName = "Settings.json"
    },
    Discord = {
        Enabled = false,
        Invite = "noinvite",
        RememberJoins = true
    }
})
local mmd = Window:CreateTab("MMD ON TOP")

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme

local Label = mmd:CreateLabel("QUER MAIS UPDATES? @MMDOFC NO YOUTUBE E TIKTOK.", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme


local Tab = Window:CreateTab("Aimbot-PC") -- Icon ID (optional)

local Section11 = Tab:CreateSection("aim config")
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
})

-- Toggle para checar se o jogador estÃ¡ na mesma equipe
Tab:CreateToggle({
    Name = "team check",
    CurrentValue = getgenv().Aimbot.Settings.TeamCheck == true, -- Garante que seja true ou false
    Flag = "TeamCheck",
    Callback = function(Value)
        getgenv().Aimbot.Settings.TeamCheck = Value
    end,
})

-- Slider para ajustar a sensibilidade do Aimbot
Tab:CreateSlider({
    Name = "sensi do nobru",
    Range = {0, 1},
    Increment = 0.1,
    Suffix = "s",
    CurrentValue = getgenv().Aimbot.Settings.Sensitivity or 0, -- Valor padrÃ£o caso seja nil
    Flag = "Sensitivity",
    Callback = function(Value)
        getgenv().Aimbot.Settings.Sensitivity = Value
    end,
})

local Section = Tab:CreateSection("fov config")
-- Toggle para habilitar/desabilitar o FOV
Tab:CreateToggle({
    Name = "ativar fov",
    CurrentValue = getgenv().Aimbot.FOVSettings.Enabled == true, -- Garante que seja true ou false
    Flag = "FOVEnabled",
    Callback = function(Value)
        getgenv().Aimbot.FOVSettings.Enabled = Value
    end,
})

-- Slider para ajustar o tamanho do FOV
Tab:CreateSlider({
    Name = "tamanho fov",
    Range = {0, 360},
    Increment = 1,
    Suffix = "Â°",
    CurrentValue = getgenv().Aimbot.FOVSettings.Amount or 90, -- Valor padrÃ£o caso seja nil
    Flag = "FOVSize",
    Callback = function(Value)
        getgenv().Aimbot.FOVSettings.Amount = Value
    end,
})

-- Button para salvar as configuraÃ§Ãµes
Tab:CreateButton({
    Name = "save config",
    Callback = function()
        getgenv().Aimbot.Settings.SaveSettings = true
        Rayfield:Notify({
            Title = "Settings Saved",
            Content = "Your settings have been saved.",
            Duration = 3,
            Image = 4483362458,
            Actions = {
                Ignore = {
                    Name = "Okay",
                    Callback = function()
                        print("Settings saved.")
                    end
                },
            },
        })
    end,
})
local localPlayer = Players.LocalPlayer
local teamName = "STAFF" -- Nome do time a ser verificado

local checkActive = false -- VariÃ¡vel para ativar/desativar a verificaÃ§Ã£o

-- FunÃ§Ã£o para verificar jogadores na equipe "STAFF"
local function checkStaffTeam()
    if not checkActive then return end -- Se o toggle estiver desligado, nÃ£o faz nada
    
    for _, player in ipairs(Players:GetPlayers()) do
        if player.Team and player.Team.Name == teamName then
            localPlayer:Kick("VocÃª foi kickado porque hÃ¡ um jogador na equipe STAFF.")
            return
        end
    end
end


local VisualTab = Window:CreateTab("Visual")
local Paragraph = VisualTab:CreateParagraph({Title = "MMD ON TOP", Content = "feito por carplacer & equipe MMD"})
-- FunÃ§Ã£o para carregar o script
local function loadScript()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/sizerdev01/mdm.menu/refs/heads/main/veritens"))()
end
local Veritem = VisualTab:CreateButton({
   Name = "Ver itens UI (irreversivel)",
   Callback = function()
    -- Verifica se a UI jÃ¡ foi criada
        if not createdUI then
            -- Executa o loadstring para carregar o script
            loadScript()

            -- Aqui vocÃª pode adicionar o cÃ³digo para criar a UI que o script cria.
            -- Caso o script jÃ¡ crie a UI, pode ser necessÃ¡rio ajustar isso:
            createdUI = Instance.new("BillboardGui")
            createdUI.Name = "PlayerUI"
            createdUI.Adornee = game.Players.LocalPlayer.Character:FindFirstChild("Head")
            createdUI.Size = UDim2.new(0, 200, 0, 70)
            createdUI.StudsOffset = Vector3.new(0, -3, 0)
            createdUI.AlwaysOnTop = true
            createdUI.Parent = game.Players.LocalPlayer.Character:FindFirstChild("Head")
        else
            -- Se a UI jÃ¡ existe, remove-a
            removeUI()
        end
    end
})

------------- esp high
local players = game:GetService("Players")

-- ConfiguraÃ§Ã£o do Highlight
local highlightColor = Color3.new(1, 0, 0) -- Vermelho
local fillTransparency = 1 -- TransparÃªncia da parte interna (1 = invisÃ­vel)
local outlineTransparency = 0 -- TransparÃªncia do contorno


local highlightInstances = {}


local function applyHighlight(character)
    if character:FindFirstChildOfClass("Highlight") then return end 
    local highlight = Instance.new("Highlight")
    highlight.FillColor = highlightColor
    highlight.FillTransparency = fillTransparency
    highlight.OutlineTransparency = outlineTransparency
    highlight.OutlineColor = highlightColor
    highlight.Adornee = character
    highlight.Parent = character
    highlightInstances[character] = highlight 
end


local function removeHighlight(character)
    local highlight = highlightInstances[character]
    if highlight then
        highlight:Destroy()
        highlightInstances[character] = nil 
    end
end


local function monitorHighlight(Value)
    for _, player in ipairs(players:GetPlayers()) do
        if player ~= players.LocalPlayer then
            local character = player.Character or player.CharacterAdded:Wait()
            if Value then
                applyHighlight(character)
            else
                removeHighlight(character) 
            end
        end
    end


    players.PlayerAdded:Connect(function(player)
        player.CharacterAdded:Connect(function(character)
            if Value then
                applyHighlight(character)
            end
        end)
    end)

    players.PlayerRemoving:Connect(function(player)
        removeHighlight(player.Character) 
    end)
end


VisualTab:CreateToggle({
   Name = "ESP Highlight",
   CurrentValue = false,
   Flag = "Toggle2", 
   Callback = function(Value)
        monitorHighlight(Value)
   end,
   -------------- espname---------
})
-- Tabela para armazenar os ESPs dos jogadores
local players = game:GetService("Players")

local espInstances = {}

local function createESPName(player)
    local character = player.Character or player.CharacterAdded:Wait()
    if character:FindFirstChild("ESPName") then return end 
    local billboardGui = Instance.new("BillboardGui")
    billboardGui.Name = "ESPName"
    billboardGui.Adornee = character:WaitForChild("Head")
    billboardGui.Size = UDim2.new(27, 0, 2, 0) 
    billboardGui.StudsOffset = Vector3.new(0, 3, 0)
    billboardGui.AlwaysOnTop = true

    local nameLabel = Instance.new("TextLabel", billboardGui)
    nameLabel.Text = player.Name
    nameLabel.Size = UDim2.new(1, 0, 1, 0)
    nameLabel.BackgroundTransparency = 1
    nameLabel.TextColor3 = Color3.new(1, 1, 1) 
    nameLabel.TextStrokeTransparency = 0.2 
    nameLabel.TextStrokeColor3 = Color3.new(0, 0, 0) 
    nameLabel.Font = Enum.Font.SourceSansBold
    nameLabel.TextSize = 27 
    nameLabel.TextScaled = false

    billboardGui.Parent = character
    espInstances[player] = billboardGui 
end


local function removeESPName(player)
    local esp = espInstances[player]
    if esp then
        esp:Destroy()
        espInstances[player] = nil 
    end
end

local function monitorESP(Value)
    for _, player in ipairs(players:GetPlayers()) do
        if player ~= players.LocalPlayer then
            local character = player.Character or player.CharacterAdded:Wait()
            if Value then
                createESPName(player)
            else
                removeESPName(player) 
            end
        end
    end

    
    players.PlayerAdded:Connect(function(player)
        player.CharacterAdded:Connect(function(character)
            if Value then
                createESPName(player)
            end
        end)
    end)

    
    players.PlayerRemoving:Connect(function(player)
        removeESPName(player) 
    end)
end


VisualTab:CreateToggle({
   Name = "ESP Name",
   CurrentValue = false,
   Flag = "Toggle1", 
   Callback = function(Value)
        
        monitorESP(Value)
   end,
})


local TeleportTab = Window:CreateTab("Teleports")
local Paragraph = TeleportTab:CreateParagraph({Title = "MMD ON TOP", Content = "feito por carplacer & equipe MMD"})


local Section = TeleportTab:CreateSection("TELEPORTS")
local function addTeleportButton(name, cframe)
    TeleportTab:CreateButton({
        Name = name,
        Callback = function()
            local player = game.Players.LocalPlayer
            if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                player.Character:MoveTo(cframe.Position + Vector3.new(0, 3, 0))
            end
        end,
    })
end
-- Adicionando os botÃµes de teletransporte para locais fixos
addTeleportButton("Teleport PraÃ§a", CFrame.new(-291.579559, 3.26299787, 342.192535))
addTeleportButton("Teleport GÃ¡s", CFrame.new(-469.959015, 3.25349784, -54.3936005))
addTeleportButton("Teleport HP", CFrame.new(-543.439941, 3.26299858, 645.16864))
addTeleportButton("Teleport Tabacaria", CFrame.new(-83.1141129, 13.1430578, 74.7073364))
addTeleportButton("Teleport Garagem", CFrame.new(-466.870148, 7.64567232, 350.242737))
addTeleportButton("Teleport Concessionaria", CFrame.new(-91.3902893, 8.07136822, 520.355347))
addTeleportButton("Teleport Gari", CFrame.new(-518.672852, 3.16749811, -1.16962147, 0, 0, -1, 0, 1, 0, 1, 0, 0))
addTeleportButton("Teleport Imobiliaria", CFrame.new(-284.904785, 8.26088619, -72.2896194, 0, 0, -1, 0, 1, 0, 1, 0, 0))
addTeleportButton("Teleport PM", CFrame.new(-980.181458, 2.27553082, 467.080536, 1, 0, 0, 0, 1, 0, 0, 0, 1))
addTeleportButton("Teleport PRF", CFrame.new(6662.24512, 36.6637421, 5047.83838, 0.707134247, 0, 0.707079291, 0, 1, 0, -0.707079291, 0, 0.707134247))
addTeleportButton("Teleport MineraÃ§Ã£o", CFrame.new(201.932144, 2.76136589, 145.50531, 0, 0, 1, 0, 1, -0, -1, 0, 0))
addTeleportButton("Teleport MecÃ¢nica", CFrame.new(-180.608261, 3.29813337, -532.4151, 0.422592998, -0, -0.906319618, 0, 1, -0, 0.906319618, 0, 0.422592998))
addTeleportButton("Teleport Fazenda", CFrame.new(817.243225, 3.26249814, -87.316864, 0, 0, 1, 0, 1, 0, -1, 0, 0))
addTeleportButton("Teleport Prefeitura", CFrame.new(-284.388458, 15.1148872, 88.0397873, 0, 0, -1, 0, 1, 0, 1, 0, 0))
addTeleportButton("Teleport Banco", CFrame.new(-27.2709007, 11.5685892, 418.200653, 1, 0, 0, 0, 1, 0, 0, 0, 1))
addTeleportButton("Teleport Ilegal", CFrame.new(12037.2705, 27.5305443, 12794.0635, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627))
addTeleportButton("Teleport predio 1", CFrame.new(-1595.23328, 204.074341, 555.895386, 0.939687431, -0.34203434, 1.81794167e-06, 1.81794167e-06, 1.02519989e-05, 1, -0.34203434, -0.93968749, 1.02519989e-05))
addTeleportButton("Teleport Devs Mini City", CFrame.new(2555.44263, 303.167755, -1004.13763, -0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, -0.422592998))

local rev = Window:CreateTab("Revistar")
local Paragraph = rev:CreateParagraph({Title = "MMD ON TOP", Content = "feito por carplacer & equipe MMD"})
local Section = rev:CreateSection("NECESSARIO")
local Button = rev:CreateButton({
   Name = "puxa itens",
   Callback = function()
   -- FunÃ§Ã£o para deletar todas as NotifyGui
local function deletarNotifyGui()
    local playerGui = game.Players.LocalPlayer:WaitForChild("PlayerGui")
    for _, gui in ipairs(playerGui:GetChildren()) do
        if gui.Name == "NotifyGui" and gui:IsA("ScreenGui") then
            gui:Destroy() -- Deleta a NotifyGui
        end
    end
end

-- Lista de itens para pegar
local itens = {"AK47", "Uzi", "Parafal", "Faca", "IA2", "G3", "IPhone 14", "Agua", "Hamburguer", "Hi Power", "Natalina"}

-- Argumentos para a requisiÃ§Ã£o
local args = {
    [1] = "mudaInv",
    [2] = "2",
    [4] = "1"
}

-- Loop principal
while true do
    -- Deletar todas as NotifyGui antes de pegar os itens
    deletarNotifyGui()

    -- Pegar itens
    for i, item in ipairs(itens) do
        if i <= 16 then  -- SÃ³ tenta alocar atÃ© 16 slots
            args[3] = item  -- Atualiza o item para o valor da vez
            args[2] = tostring(i)  -- Atribui o slot dinamicamente (1, 2, 3, ..., 16)

            -- Usar task.spawn() para execuÃ§Ã£o sem delay
            task.spawn(function()
                -- Envia a requisiÃ§Ã£o para o servidor
                game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("InvRemotes"):WaitForChild("InvRequest"):InvokeServer(unpack(args))
            end)
        end
    end

    wait(0)  -- Espera um frame para evitar lag
end
   end,
})
local Section = rev:CreateSection("PC")
local ww = rev:CreateToggle({
   Name = "mandar revistar (TECLA E)",
   CurrentValue = false,
   Flag = "rvst",
   Callback = function(Value)
       getgenv().Enabled = Value
   end,
})
local Section = rev:CreateSection("MOBILE")
local mob = rev:CreateButton({
   Name = "mandar revistar UI",
   Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/sizerdev01/keyload/refs/heads/main/revstsa"))()
   end,
})
local Section = rev:CreateSection("Info")
local Paragraph = rev:CreateParagraph({Title = "Como usar?", Content = "Ensinamos a usar corretamente no nosso discord."})



local otoTab = Window:CreateTab("Outros")
local Paragraph = otoTab:CreateParagraph({Title = "MMD ON TOP", Content = "feito por carplacer & equipe MMD"})
local Toggle = otoTab:CreateToggle({
    Name = "anti staff V2",
    CurrentValue = false,
    Flag = "ToggleKickCheck",
    Callback = function(Value)
        if Value then
            getgenv().KickCheck = true
            loadstring(game:HttpGet('https://raw.githubusercontent.com/sizerdev01/keyload/refs/heads/main/staffv2'))()
        else
            getgenv().KickCheck = false
        end
    end
})


-- Loop para checar a cada 5 segundos, apenas se ativado
task.spawn(function()
    while true do
        if checkActive then
            checkStaffTeam()
        end
        task.wait(5)
    end
end)


local Butkton = otoTab:CreateButton({
   Name = "farm planta UI",
   Callback = function()
   -- Criando a UI
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local ToggleButton = Instance.new("TextButton")
ToggleButton.Parent = ScreenGui
ToggleButton.Size = UDim2.new(0, 200, 0, 50)
ToggleButton.Position = UDim2.new(0.5, -100, 0.1, 0)
ToggleButton.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
ToggleButton.TextColor3 = Color3.fromRGB(255, 255, 255)
ToggleButton.Font = Enum.Font.SourceSansBold
ToggleButton.TextSize = 20
ToggleButton.Text = "Ativar Farm"

local farming = false  -- VariÃ¡vel para controlar o farm

-- FunÃ§Ã£o para teletransportar para um "Stem" aleatÃ³rio
local function teleportarJogadorAleatoriamente()
    local stems = {}

    for _, plantaIlegal in pairs(game.Workspace:GetDescendants()) do
        if plantaIlegal.Name == "PlantaIlegal" then
            local stem = plantaIlegal:FindFirstChild("Stem")
            if stem then
                table.insert(stems, stem)
            end
        end
    end

    if #stems > 0 then
        local stemAleatorio = stems[math.random(1, #stems)]
        if stemAleatorio and game.Players.LocalPlayer.Character then
            local humanoide = game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
            if humanoide then
                humanoide.CFrame = stemAleatorio.CFrame
            end
        end
    else
        warn("Nenhum 'Stem' encontrado.")
    end
end

-- Simula a tecla "E" para interagir
local function segurarTeclaE()
    local virtualInputManager = game:GetService("VirtualInputManager")
    local interactionKey = "E"
    
    for _ = 1, 17 do  -- MantÃ©m pressionado por 17 segundos
        virtualInputManager:SendKeyEvent(true, interactionKey, false, game)
        wait(1)
    end

    virtualInputManager:SendKeyEvent(false, interactionKey, false, game)
end

-- Loop do farm
local function farmLoop()
    while farming do
        teleportarJogadorAleatoriamente()
        segurarTeclaE()
        wait(1)
    end
end

-- Alternar o farm ao clicar no botÃ£o
ToggleButton.MouseButton1Click:Connect(function()
    farming = not farming  -- Inverte o estado do farm

    if farming then
        ToggleButton.Text = "Desativar Farm"
        farmLoop()
    else
        ToggleButton.Text = "Ativar Farm"
    end
end)
   end,
})

local Section = otoTab:CreateSection("AUTO CL CONFIG")
-- Verifica se getgenv estÃ¡ disponÃ­vel
if getgenv == nil then
    error("getgenv nÃ£o estÃ¡ definido neste ambiente.")
end

-- ConfiguraÃ§Ã£o inicial do getgenv
getgenv().KickOnLowHealth = false -- Ativar/desativar o auto kick
getgenv().HealthThreshold = 10    -- Vida mÃ­nima antes de ser expulso

-- FunÃ§Ã£o para monitorar a vida do jogador
local function monitorHealth()
    local player = game.Players.LocalPlayer
    local character = player.Character
    if character and character:FindFirstChild("Humanoid") then
        local humanoid = character.Humanoid
        humanoid.HealthChanged:Connect(function(health)
            if health <= getgenv().HealthThreshold and getgenv().KickOnLowHealth then
                player:Kick("Auto cl pq tua vida tava abaixo de " .. getgenv().HealthThreshold)
            end
        end)
    end
end

game.Players.LocalPlayer.CharacterAdded:Connect(function()
    monitorHealth()
end)

if game.Players.LocalPlayer.Character then
    monitorHealth()
end

-- CriaÃ§Ã£o do Toggle para ativar/desativar o auto kick
local Toggle = otoTab:CreateToggle({
   Name = "auto CL",
   CurrentValue = getgenv().KickOnLowHealth,
   Flag = "AutoKickToggle",
   Callback = function(Value)
       getgenv().KickOnLowHealth = Value
   end,
})

-- CriaÃ§Ã£o do Slider para ajustar o limite de vida
local Slider = otoTab:CreateSlider({
   Name = "kick quando vida =",
   Range = {0, 100},
   Increment = 1,
   Suffix = " HP",
   CurrentValue = getgenv().HealthThreshold,
   Flag = "HealthThresholdSlider",
   Callback = function(Value)
       getgenv().HealthThreshold = Value
   end,
})

getgenv().Key = Enum.KeyCode.E
getgenv().Enabled = getgenv().Enabled or false
loadstring(game:HttpGet('https://raw.githubusercontent.com/sizerdev01/keyload/refs/heads/main/revistarkkj'))()
