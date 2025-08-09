local player = game.Players.LocalPlayer
local humanoid = nil

player.CharacterAdded:Connect(function(character)
    humanoid = character:WaitForChild("Humanoid")
    humanoid.JumpPower = 150 -- padrão é 50, aqui é o pulo alto
end)

-- Caso o personagem já esteja no jogo quando o script rodar
if player.Character then
    humanoid = player.Character:WaitForChild("Humanoid")
    humanoid.JumpPower = 150
end
