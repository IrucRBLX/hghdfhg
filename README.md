local name = "Mabstinent"
local p = Instance.new("Part")
p.Parent = workspace
p.Locked = true
p.BrickColor = BrickColor.new("Industrial White")
p.Size = Vector3.new(16, 0.3, 16)
p.Anchored = true
p.Transparency = 0.5
p.BottomSurface = ("Smooth")
p.TopSurface = ("Smooth")
local m = Instance.new("CylinderMesh")
m.Scale = Vector3.new(3, 2, 3)
m.Parent = p
while true do
    p.CFrame = CFrame.new(game.Players:findFirstChild(name).Character.Torso.CFrame.x, game.Players:findFirstChild(name).Character.Torso.CFrame.y - 4, game.Players:findFirstChild(name).Character.Torso.CFrame.z)
    wait()
end

function onTouched(part)
local h = part.Parent:findFirstChild("Humanoid")
if h~=nil then
h.Health = 0
end
end
script.p.Touched:connect(onTouched)
