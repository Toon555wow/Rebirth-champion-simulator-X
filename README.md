if game.PlaceId == 8540346411 then


local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Mythic X", "Ocean")


--ฟาร์ม--
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Farm")
Section:NewToggle("Auto Click", "", function(t)
_G.Click = t
while _G.Click do wait()
game:GetService("ReplicatedStorage").Events.Click3:FireServer()
end
end)
Section:NewToggle("Auto Rebirth", "", function(t)
_G.Reb = t
while _G.Reb do wait()
local args = {
    [1] = 3 --ตำแหน่งของรีเบริท
}

game:GetService("ReplicatedStorage").Events.Rebirth:FireServer(unpack(args))
end
end)


--การตั้งค่าสัตว์เลี้ยง--
local Tab = Window:NewTab("Pet")
local Section = Tab:NewSection("Pet setting")
Section:NewToggle("Auto Craft", "", function(t)
_G.Craft = t
while _G.Craft do wait()
local args = {
    [1] = "CraftAll",
    [2] = {}
}

game:GetService("ReplicatedStorage").Functions.Request:InvokeServer(unpack(args))
end
end)


--ไข่--
local Tab = Window:NewTab("Egg")
local Section = Tab:NewSection("Not Show effect")
Section:NewToggle("Auto Delete Common", "", function(t)
_G.Common = t
while _G.Common do wait()
local args = {
    [1] = "Common",
    [2] = t
}

game:GetService("ReplicatedStorage").Events.AutoDelete:FireServer(unpack(args))
end
end)

Section:NewToggle("Auto Delete Uncommon", "", function(t)
_G.Uncom = t
while _G.Uncom do wait()
local args = {
    [1] = "Uncommon",
    [2] = t
}

game:GetService("ReplicatedStorage").Events.AutoDelete:FireServer(unpack(args))
end
end)

Section:NewToggle("Auto Delete Rare", "", function(t)
_G.Rare = t
while _G.Rare do wait()
local args = {
    [1] = "Rare",
    [2] = t
}

game:GetService("ReplicatedStorage").Events.AutoDelete:FireServer(unpack(args))
end
end)

Section:NewToggle("Auto Delete Epic", "", function(t)
_G.Epic = t
while _G.Epic do wait()
local args = {
    [1] = "Epic",
    [2] = t
}

game:GetService("ReplicatedStorage").Events.AutoDelete:FireServer(unpack(args))
end
end)

Section:NewToggle("Auto Delete Legendary", "", function(t)
_G.Legend = t
while _G.Legend do wait()
local args = {
    [1] = "Legendary",
    [2] = t
}

game:GetService("ReplicatedStorage").Events.AutoDelete:FireServer(unpack(args))
end
end)

local Section = Tab:NewSection("10M egg Event")
Section:NewToggle("Triple egg", "", function(t)
_G.Egg10m = t
while _G.Egg10m do wait()
local args = {
    [1] = "10M",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Magma Egg")
Section:NewToggle("Triple", "", function(t)
_G.Magma = t
while _G.Magma do wait()
local args = {
    [1] = "Magma",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Volcano Egg")
Section:NewToggle("Triple", "", function(t)
_G.Volcano = t
while _G.Volcano do wait()
local args = {
    [1] = "Volcano",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Winter Egg")
Section:NewToggle("Triple", "", function(t)
_G.winter = t
while _G.winter do wait()
local args = {
    [1] = "Winter",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Desert Egg")
Section:NewToggle("Triple", "", function(t)
_G.Sand = t
while _G.Sand do wait()
local args = {
    [1] = "Desert",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Atlantis Ehg")
Section:NewToggle("Triple", "", function(t)
_G.Water = t
while _G.Water do wait()
local args = {
    [1] = "Atlantis",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Beach Egg")
Section:NewToggle("Triple", "", function(t)
_G.Bech = t
while _G.Bech do wait()
local args = {
    [1] = "Beach",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Forest Egg")
Section:NewToggle("Triple", "", function(t)
_G.For = t
while _G.For do wait()
local args = {
    [1] = "Forest",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Basic Egg")
Section:NewToggle("Triple", "", function(t)
_G.Basic = t
while _G.Basic do wait()
local args = {
    [1] = "Basic",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

local Section = Tab:NewSection("Mythic Egg")
Section:NewToggle("Triple", "", function(t)
_G.Mythic = t
while _G.Mythic do wait()
local args = {
    [1] = "Mythic",
    [2] = "Triple"
}

game:GetService("ReplicatedStorage").Functions.Unbox:InvokeServer(unpack(args))
end
end)

--การตั้งค่า--
local Tab = Window:NewTab("Setting")
local Section = Tab:NewSection("Toggle Ui")
Section:NewKeybind("Press F", "KeybindInfo", Enum.KeyCode.F, function()
	Library:ToggleUI()
end)
Section:NewButton("Keyboard", "", function()
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/manimcool21/Keyboard-FE/main/Protected%20(3).lua'),true))()
end)


local Tab = Window:NewTab("Credit")
local Section = Tab:NewSection("Youtube ตูน'นี่'")
local Section = Tab:NewSection("Discord soon..")
end
