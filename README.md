local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()

local Window = Library.CreateLib("ZX Hub", "DarkTheme")

local Tab = Window:NewTab("Main")

local Section = Tab:NewSection("Auto Equip")

local Weaponlist = {}

local Weapon = nil

for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do

    table.insert(Weaponlist,v.Name)

end

Section:NewDropdown("select weapon", " ", Weaponlist, function(currentOption)

    Weapon = currentOption

end)

Section:NewToggle("Auto Equip", " ", function(a)

AutoEquiped = a

end)

spawn(function()

while wait() do

if AutoEquiped then

pcall(function()

game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))

end)

end

end

end)

local Tab = Window:NewTab("ไก่ตันละมั้ง")

local noSection = Tab:NewSection("เริ่ม")

Section:NewButton("ButtonText", "ButtonInfo", function()

    loadstring(game:HttpGet("https://raw.githubusercontent.com/GooD1020/Exon_x_hub_kaitan/main/README.md"))()

end)

Section:NewButton("ButtonText", "ButtonInfo", function()

    syn.set_thread_identity(5)

local ReplicatedStorage = game:GetService("ReplicatedStorage")

local Player = game:GetService("Players").LocalPlayer

local ArgsTransform = {

    Character = game.Players.LocalPlayer.Character,

    CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame,

    Color1 = Color3.fromRGB(102, 255, 153),

    Color2 = Color3.fromRGB(102, 255, 153),

    Color3 = Color3.fromRGB(102, 255, 153),

}

Player.Character.Humanoid:LoadAnimation(ReplicatedStorage.Util.Anims.Storage["2"].RaceTransform):Play()

delay(1, function()

    pcall(function() require(ReplicatedStorage.Effect.Container.RaceTransformation.Main)(ArgsTransform) end)

end)

local ReplicatedStorage = game:GetService("ReplicatedStorage")

local Player = game:GetService("Players").LocalPlayer

local ArgsDash = {

    Character = Player.Character,

    Duration = .25,

    CFrame = Player.Character.HumanoidRootPart.CFrame,

}

local old; old = hookmetamethod(game, "__namecall", newcclosure(function(self, ...)

    if self.Name == "CommE" then

        local args = {...}

        if args[1] == "Dodge" then

            coroutine.wrap(function() require(ReplicatedStorage.Effect.Container.Shared.LightningTP)(ArgsDash) end)()

        end

    end

    

    return old(self, ...)

end))

local ReplicatedStorage = game:GetService("ReplicatedStorage")

local Player = game:GetService("Players").LocalPlayer

local ArgsDash = {

    Character = Player.Character,

    Duration = .25,

    CFrame = Player.Character.HumanoidRootPart.CFrame,

}

local old; old = hookmetamethod(game, "__namecall", newcclosure(function(self, ...)

    if self.Name == "CommE" then

        local args = {...}

        if args[1] == "Dodge" then

            coroutine.wrap(function() require(ReplicatedStorage.Effect.Container.Shared.LightningTP)(ArgsDash) end)()

        end

    end

    

    return old(self, ...)

end))
