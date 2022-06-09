local IDS = {31231241}

game.Players.PlayedAdded:Connect(function(player)
    if not table.find(IDS,player.UserId) then --If the UserID value is not in the table this returns nil. In Lua nil equals false.
        player:Kick("You are not whitelisted on this server.")
    end
end)
