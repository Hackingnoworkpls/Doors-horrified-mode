-- Achievement
local Achievements = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors/Custom%20Achievements/Source.lua"))()

-- Creates and displays your custom achievement
Achievements.Get({
    Title = "horrified v1",
    Desc = "",
    Reason = 'V1',
    Image = "https://github.com/ha2ke3oer/VPNWORK/blob/main/static-assets-upload8893301385814255192.png?raw=true",
})

--[=[
@class txt
This is my First Class
--]=]

print(os.date("%B"))

print("Loading")
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------

local HardCore = {
    Title = "The Pain Just Begain", -- Made by MuhammadGames and Volta
    Desc = "Join a Match of HardCore For the First Time.",
    Reason = "You executed the HardCore script.",
    Image = "https://github.com/MuhXd/Models/blob/main/HardCoreDoors.png?raw=true",
    id = 1,
}

local DepthW = {
    Title = "Finally Free",
    Desc = "Encounter Depth",
    Reason = "Survive Depth",
    Image = "https://github.com/MuhXd/DoorSuff/blob/main/DoorsModes/Png.png?raw=true",
    id = 2,
}

local Depth = {
    Title = "The Entity Is Still Freezing",
    Desc = "It's So Cold",
    Reason = "Dont Survive Depth",
    Image = "https://github.com/MuhXd/DoorSuff/blob/main/DoorsModes/Png.png?raw=true",
    id = 3,
}

local Smiles = {
    Title = "Income The Frowners",
    Desc = "Stop Smiling",
    Reason = "Encounter and Survive Smiler",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 4,
}

local SmilesDie = {
    Title = "Smile to Fail",
    Desc = "Don't Smile",
    Reason = "Encounter And Dont Survive Smiler",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 5,
}

local NightmareRush ={
    Title = "Rush From Your Nightmares",
    Desc = "Don't Be fooled",
    Reason = "Encounter And Survive Nightmare Rush",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 6,
}

local NightmareAmbush ={
    Title = "Ambush But Even Harder",
    Desc = "Don't Be fooled",
    Reason = "Encounter And Survive Nightmare Ambush",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 7,
}

local NightmareAmbush ={
    Title = "Ambush But Even Harder",
    Desc = "Don't Be fooled",
    Reason = "Encounter And Survive Nightmare Ambush",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 8,
}


-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------






-- loadstring(game:HttpGet("https://raw.githubusercontent.com/MuhXd/DoorSuff/main/Whitelist/NewKeySystem.lua"))()



caa = 0
tween = game:GetService("TweenService")
local TestMultplayer = true
if game:GetService("ReplicatedStorage"):FindFirstChild("Inrooms") then
    warn("You have Already Loaded")

    return true
end
local Test = Instance.new("Part")
Test.Name = "Inrooms"
Test.Parent = game:GetService("ReplicatedStorage")
Test = 1

local SelfModules = {
    Functions = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Functions.lua"))(),
}






------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------







local ModName = "HardCore"
local foldername = "AchievementsSaves   By Muhammadgames,Helped by RegularVynixu"
local Slipt = string.split(foldername,"|")
local valid2 = isfolder(foldername)
if not valid2 then
    makefolder(foldername)
end

local fileName = ModName.."Save's.txt"
local filePath = foldername.. "/".. fileName
local valid = isfile(filePath)

local Achievements = loadstring(game:HttpGet("https://raw.githubusercontent.com/MuhXd/Models/main/RegularVynixu's%20Achievement%20Modifyer"))()

function AchievementsGet(Achievement)
    local read = readfile(filePath)  
    local read2 = tostring(read)
    local read2 = string.split(read,"|")
    FOUND = true
    Find = ""
    for i,v in pairs(Achievement) do
        if i == "id" then
            Find=Find.." "..v
        end
    end

    for i,v in pairs(read2) do
        if v == Find then
            FOUND = true
        end
    end -- Desc
    if FOUND == false then
        Achievements.Get(Achievement)
        Write = ""
        for i,v in pairs(Achievement) do
            if i == "id" then
                Write=Write.." "..v
            end
        end
        appendfile(filePath,Write.."|")
    end
end
-- Creates and displays your custom achievement
-- readfile(<string> path)  
if not valid then
    writefile(filePath, "Helped by RegularVynixu|")
end

AchievementsGet(HardCore)
--[[
------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------ 
Start of real Code!
DON'T SHOW ABOVE!
.............     .       .
.     .     .     .       . 
.     .     .     .       .
.     .     .     .       . 
.     .     .     .       . 
.     .     .     .       . 
.     .     .     .       .
.     .     .     .........
--]]












if game:GetService("ReplicatedStorage"):FindFirstChild("Guis") then

else
    Visable = Instance.new("Folder")
    Visable.Name = "Guis"
    Visable.Parent = game.ReplicatedStorage

end
function Gui(Name,Amount1,TextSent)
    if game:GetService("Players").localPlayer.PlayerGui.MainUI.Statistics.Frame:FindFirstChild("!"..Name.."!") then
        game:GetService("Players").localPlayer.PlayerGui.MainUI.Statistics.Frame["!"..Name.."!"]:Destroy()
    end

    Visable = Instance.new("BoolValue")
    Visable.Value = true
    Visable.Name = Name
    Visable.Parent = game.ReplicatedStorage.Guis

    game.Players.localPlayer.PlayerGui.MainUI.Statistics.LocksOpened.Visible = true
    LocksOpened = game.Players.localPlayer.PlayerGui.MainUI.Statistics.LocksOpened:Clone()
    game.Players.localPlayer.PlayerGui.MainUI.Statistics.LocksOpened.Visible = false
    LocksOpened.Parent = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame

    LocksOpened.Visible = game.ReplicatedStorage.Guis:FindFirstChild(Name).Value

    local Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].UICorner:Clone()
    Grad.Parent = LocksOpened
    Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].UIGradient:Clone()
    Grad.Parent = LocksOpened
    Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].Amount:Clone()
    Grad.Parent = LocksOpened
    Grad.Text = Amount1
    Grad.Position = Grad.Position - UDim2.new(0.035,0,0,0)
    Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].Icon:Clone()
    Grad.Parent = LocksOpened
    Grad.Position = Grad.Position - UDim2.new(0.035,0,0,0)

    LocksOpened.CloseButton.Position = LocksOpened.CloseButton.Position - UDim2.new(0.021,0,0,0)
    LocksOpened.CloseButton.ImageColor3 =  Color3.new(0.0313725, 0.854902, 1)
    LocksOpened.TextColor3 = Color3.new(0.0313725, 0.854902, 1)
    LocksOpened.TextScaled = false
    LocksOpened.Name = "!"..Name.."!"
    LocksOpened.TextSize = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].TextSize + 16
    LocksOpened.Size = LocksOpened.Parent["Leftover Gold"].Size
    LocksOpened.BackgroundColor3 = Color3.new(0.0196078, 0.552941, 0.647059)
    LocksOpened.BackgroundTransparency = 0.5

    LocksOpened.Text = TextSent



    game.ReplicatedStorage.Guis:FindFirstChild(Name).changed:connect(function()

        LocksOpened.Visible = game.ReplicatedStorage.Guis:FindFirstChild(Name).Value
    end)
end







local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()


-- Run the created entity
local Message = function(Message,Enable,N)
    local msg = Instance.new("Message")  
    msg.Parent = game.Workspace     
    msg.Text = Message
    if Enable ~= true then
        task.wait(0.1)
        msg:Destroy()
    end
end

-- Message("Thank you For Loading MultplayerBeta 1.2")

for ii,vv in pairs(game:GetService("Players"):GetChildren()) do
    PlayersIngame = ii
end -- Gets All Players
if TestMultplayer == true then
    PlayersIngame = 10 -- TestMultplayer
end

if PlayersIngame > 1 then -- if more then one then waits for link
    if game:GetService("ReplicatedStorage").GameData.LatestRoom.Value > 0 then
        print("Loaded After door 1! Please wait for everyone to die")
        game.StarterGui:SetCore("ChatMakeSystemMessage", {
            Text = "Load Before Door 1",
            Color = Color3.fromRGB(255, 0, 0),
            Font = Enum.Font.SourceSansBold,
            TextSize = 18,
        })

        firesignal(game.ReplicatedStorage.Bricks.DeathHint.OnClientEvent, {"You didn't Load it Before Door 1!","Please Wait for the next round"})
        game.ReplicatedStorage.GameStats["Player_".. game.Players.LocalPlayer.Name].Total.DeathCause.Value = "Not Loading Before Door 1"
        game.Players.LocalPlayer.Character.Humanoid.Health = -100
        return false
    end


    game.StarterGui:SetCore("ChatMakeSystemMessage", {
        Text = "interminable rooms ON! By PrIme A-60 (a600399)",
        Color = Color3.fromRGB(255, 0, 0),
        Font = Enum.Font.SourceSansBold,
        TextSize = 18,
    })

    Gui("interminable rooms","+1000","interminable rooms (Doesn't add Nobs)")

    print("Loaded, Wating to Link to Multplayer") -- waiting to link

game:GetService("ReplicatedStorage").GameData.LatestRoom.Changed:Connect(function(v)
    L = game:GetService("Workspace").CurrentRooms[v].PathfindNodes:Clone()
    L.Parent = game:GetService("Workspace").CurrentRooms[v]
    L.Name = 'PathfindNodes'
end)
    
    c=1

    repeat task.wait()

        if c < 10 then
            -- Message("MultplayerV1.2B",true,"Welcome")
            c=10
        end
        --  msg:Destroy()
        --Kill=true
    until game:GetService("ReplicatedStorage").GameData.LatestRoom.Value > 0
    print("Linked to Clients") -- linked
    
    game.StarterGui:SetCore("ChatMakeSystemMessage", {
        Text = "Linked To Clients",
        Color = Color3.fromRGB(0, 255, 0),
        Font = Enum.Font.SourceSansBold,
        TextSize = 18,
    })



    Singleplayer = false -- Runs more Then 1 Player Code
else
    print("Loaded in print Multiplayer") -- loaded in 1 player
    repeat task.wait()

    until game:GetService("ReplicatedStorage").GameData.LatestRoom.Value > 0
    print("Started")
    Singleplayer = true -- Runs One player Code
end
Testa = 10
getgenv().death = false
Be=false
Many=1
JobId = game:GetService("ReplicatedStorage").GameData.GameStarted.Value
Lowest = string.len(game:GetService("ReplicatedStorage").GameData.GameStarted.Value)
Lowest = tonumber(Lowest)
Stop=Lowest
RanWait2=""
function Aten()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(40)
        wait(50)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 10 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(20)
            end
        local entity = Creator.createEntity({
            CustomName = "C 60", -- Custom name of your entity
            Model = "rbxassetid://12289478026/", -- Can be GitHub file or rbxassetid
            Speed = 1000, -- Percentage, 100 = default Rush speed
            DelayTime = 5,
            KillRange= 1000,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = false,
            FlickerLights = {
                true, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 3,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        0, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        5263560566, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(50, 115, 108), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to C 60"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atin()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(260)
        wait(270)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 20 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(50)
            end
        local entity = Creator.createEntity({
            CustomName = "A 60 blue", -- Custom name of your entity
            Model = "13979811694", -- Can be GitHub file or rbxassetid
            Speed = 6000, -- Percentage, 100 = default Rush speed
            DelayTime = 5,
            KillRange= 3000,-- Time before starting cycles (seconds)
            HeightOffset = 4,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = false,
            FlickerLights = {
                false, -- Enabled
                1, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 3,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        5263560566, -- SoundId
                        { Volume = 5 }, -- Sound properties
                    },
                    Sound2 = {
                        5263560566, -- SoundId
                        { Volume = 5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(50, 115, 108), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A 60 blue"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atyn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(110)
        wait(120)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 20 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(70)
            end
        local entity = Creator.createEntity({
            CustomName = "Smile", -- Custom name of your entity
            Model = "14352169429", -- Can be GitHub file or rbxassetid
            Speed = 1000, -- Percentage, 100 = default Rush speed
            DelayTime = 3,
            KillRange= 100,-- Time before starting cycles (seconds)
            HeightOffset = 4,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                true, -- Enabled
                3, -- Time (seconds)
            },
            Cycles = {
                Min = 5,
                Max = 5,
                WaitTime = 3,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "https://tr.rbxcdn.com/f0f798ca806ed372984f3b70d1b1432f/420/420/Image/Png", -- Image1 url
                    Image2 = "https://tr.rbxcdn.com/f0f798ca806ed372984f3b70d1b1432f/420/420/Image/Png", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        0, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Sound2 = {
                        5263560566, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(50, 115, 108), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 2,
                        Max = 8,
                    },
                },
            },
            CustomDialog = {"You died to smile"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Athn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(210)
        wait(220)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(130)
            end
        local entity = Creator.createEntity({
            CustomName = "careful ", -- Custom name of your entity
            Model = "10921624589", -- Can be GitHub file or rbxassetid
            Speed = 6000, -- Percentage, 100 = default Rush speed
            DelayTime = 5,
            KillRange= 10000,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                true, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 0,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                true, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "https://create.roblox.com/marketplace/asset/14091415779/Chamber60-Spritesheet-Chamber-Rooms?keyword=A-60+rooms&pageNumber=1&pagePosition=", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to careful "}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atkn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(340)
        wait(350)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(330)
            end
        local entity = Creator.createEntity({
            CustomName = "watcher", -- Custom name of your entity
            Model = "10999490102", -- Can be GitHub file or rbxassetid
            Speed = 10, -- Percentage, 100 = default Rush speed
            DelayTime = 1,
            KillRange= 10,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                false, -- Enabled
                10, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "https://create.roblox.com/marketplace/asset/14091415779/Chamber60-Spritesheet-Chamber-Rooms?keyword=A-60+rooms&pageNumber=1&pagePosition=", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to wather"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0

     




















pcall(function()
local AtenPas = coroutine.wrap(Aten)
AtenPas()
end)
pcall(function()
local AtynPas = coroutine.wrap(Atyn)
AtynPas()
end)
pcall(function()
local AthnPas = coroutine.wrap(Athn)
AthnPas()
end)
pcall(function()
local AtinPas = coroutine.wrap(Atin)
AtinPas()
end)
pcall(function()
local AtknPas = coroutine.wrap(Atkn)
AtknPas()
end)
