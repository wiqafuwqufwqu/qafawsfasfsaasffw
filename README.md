-- Canonical way to get a service
local Players = game:GetService("Players")

-- Use UserIds instead; usernames can change, UserIds cannot
local WHITELIST = {"fwq"}

Players.PlayerAdded:Connect(function (player)
    if not table.find(WHITELIST, player.Name) then
        player:Kick()
    end
end)
