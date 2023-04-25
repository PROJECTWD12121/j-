loadstring(game:HttpGet('https://raw.githubusercontent.com/GS21Official/-ToolsScript/main/!Tools%20script%20page'))()

game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == '!1v1' then
        -- Teleport the entire character's body to the desired location
        local teleportLocation = Vector3.new(208, 38, 200017)
        game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(teleportLocation))
    end
end)

game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == '!banktop' then
        -- Teleport the entire character's body to the desired location
        local teleportLocation = Vector3.new(-478, 39, -285)
        game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(teleportLocation))
    end
end)

game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == '!DB' then
        -- Teleport the entire character's body to the desired location
        local teleportLocation = Vector3.new(-1043, 22, -261)
        game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(teleportLocation))
    end
end)

-- Function to teleport local player's character to the specified player
local function teleportToPlayer(playerName)
    local player = nil

    -- Find player by username or display name
    for _, p in ipairs(game.Players:GetPlayers()) do
        if p.Name:lower():find(playerName:lower()) or p.DisplayName:lower():find(playerName:lower()) then
            player = p
            break
        end
    end

    -- Teleport local player's character to player if found, otherwise display error message
    if player then
        local character = game.Players.LocalPlayer.Character
        if character then
            local targetCharacter = player.Character
            if targetCharacter then
                character:SetPrimaryPartCFrame(targetCharacter:GetPrimaryPartCFrame())
            else
                print('Target player does not have a character.')
            end
        else
            print('Local player does not have a character.')
        end
    else
        print('Player not found:', playerName)
    end
end

-- Function to listen for commands
local function onChatted(msg)
    local cmd, target = msg:match("^(%S+)%s+(.+)$")

    if cmd == "!goto" then
        -- Check if the target player name is a display name
        if game.Players:FindFirstChild(target) then
            target = game.Players[target].DisplayName
        end

        teleportToPlayer(target)
    end
end

-- Connect the onChatted function to the Roblox chat event
game.Players.LocalPlayer.Chatted:Connect(onChatted)

game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == '!key' then
        -- Teleport the entire character's body to the desired location
        local teleportLocation = Vector3.new(-271, 22, -240)
        game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(teleportLocation))
    end
end)

game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == '!food shop' then
        -- Teleport the entire character's body to the desired location
        local teleportLocation = Vector3.new(-338, 24, -297)
        game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(teleportLocation))
    end
end)

game.Players.LocalPlayer.Chatted:Connect(function(msg)
    if msg == '!rpg' then
        -- Teleport the entire character's body to the desired location
        local teleportLocation = Vector3.new(111, -27, -276)
        game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(teleportLocation))
    end
end)
