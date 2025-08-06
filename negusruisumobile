-- version negus 1.1
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local attackBtn = game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui"):WaitForChild("gameUI"):WaitForChild("mobileButtons"):WaitForChild("attack")
local ReplicatedStorage = cloneref(game:GetService("ReplicatedStorage"))

-- Replace 'hitbox' with the correct part if needed (e.g., HumanoidRootPart)
local teleportPart = character:WaitForChild("hitbox")

task.spawn(function()
	while true do
		task.wait(0.1) 
		if attackBtn and attackBtn.Visible then
			attackBtn:Activate()
		end
	end
end)

--auto start
game:GetService("ReplicatedStorage"):WaitForChild("network"):WaitForChild("RemoteFunction"):WaitForChild("playerRequest_readyUp"):InvokeServer()

--auto collect
local cour = task.spawn(function()
            while task.wait(1/2) do
                for i,v in pairs(workspace.placeFolders.items:GetChildren()) do
                    if v then
                        ReplicatedStorage.network.RemoteFunction.pickUpItemRequest:InvokeServer(v)
                    end
                end
            end
        end)
--tp
local targetPosition = Vector3.new(-314.33441162109375, -105.5562744140625, 558.3173828125)

teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(-314.33441162109375, -105.5562744140625, 558.3173828125)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(-330.1209411621094, -105.5578842163086, 586.6276245117188)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(-326.0479431152344, -105.5578842163086, 584.2651977539062)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(-354.4789123535156, -105.80604553222656, 562.0234985351562)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(-335.9320068359375, -105.5728988647461, 558.1990356445312)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(-336.4647216796875, -105.87250518798828, 566.780517578125)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(189.90953063964844, -3.788501739501953, 108.84291076660156)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(331.0973205566406, 1.929663896560669, 406.6504821777344)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(334.1731872558594, 3.393198013305664, 395.3982849121094)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(321.3743896484375, 3.235802173614502, 418.2917175292969)
teleportPart.Position = targetPosition

task.wait(1)
targetPosition = Vector3.new(170.8604736328125, -31.178327560424805, 859.8301391601562)
teleportPart.Position = targetPosition

task.wait(1)

task.spawn(function()
    repeat
        task.wait(1)
    until workspace:FindFirstChild("placeFolders")
        and workspace.placeFolders:FindFirstChild("rooms")
        and workspace.placeFolders.rooms:FindFirstChild("1")
        and workspace.placeFolders.rooms["1"]:FindFirstChild("warp")

    local warp = workspace.placeFolders.rooms["1"].warp

    game:GetService("ReplicatedStorage").network.RemoteEvent.playerRequest_activateEscapeRope:FireServer(warp)
end)

task.wait(1)
game:GetService("ReplicatedStorage"):WaitForChild("network"):WaitForChild("RemoteFunction"):WaitForChild("playerRequest_respawnMyCharacter"):InvokeServer()

game:GetService("ReplicatedStorage"):WaitForChild("network"):WaitForChild("RemoteFunction"):WaitForChild("playerRequest_replayDungeon"):InvokeServer()
