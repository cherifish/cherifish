local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Key System", HidePremium = false, SaveConfig = true})

OrionLib:MakeNotification({
    Name = "Logged In!",
    Content = "You Logged In!",
    Image = "rbxassetid://4483345998",
    Time = 5
})

_G.Key = "Anwdiafawfijwahfawhf92139"
_G.KeyInput = "string"

function Hub()

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "owen Hub | Money Race ", HidePremium = false, SaveConfig = true, ConfigFolder = "owen"})

local Tab = Window:MakeTab({
	Name = "Main 🏠",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local TabTwo = Window:MakeTab({
	Name = "Eggs 🥚",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local TabFour = Window:MakeTab({
    Name = "Misc 🎲",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})
    
    local Section = TabFour:AddSection({
    Name = "Cre: owen"
})
local Section = TabFour:AddSection({
    Name = "discord.gg/RbMeKAHg"
})


local Section = Tab:AddSection({
	Name = "Farm Script"
})

Tab:AddButton({
	Name = "Win Farm - No Car Equipped",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/ToraIsMe/ToraIsMe/main/0MoneyRace"))()
  	end    
})

local Section = Tab:AddSection({
	Name = "Anti Afk"
})

Tab:AddButton({
    Name = "Anti Afk",
    Callback = function()
wait(0.5)local ba=Instance.new("ScreenGui")
local ca=Instance.new("TextLabel")local da=Instance.new("Frame")
local _b=Instance.new("TextLabel")local ab=Instance.new("TextLabel")ba.Parent=game.CoreGui
ba.ZIndexBehavior=Enum.ZIndexBehavior.Sibling;ca.Parent=ba;ca.Active=true
ca.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ca.Draggable=true
ca.Position=UDim2.new(0.698610067,0,0.098096624,0)ca.Size=UDim2.new(0,370,0,52)
ca.Font=Enum.Font.SourceSansSemibold;ca.Text="Anti AFK Script"ca.TextColor3=Color3.new(0,1,1)
ca.TextSize=22;da.Parent=ca
da.BackgroundColor3=Color3.new(0.196078,0.196078,0.196078)da.Position=UDim2.new(0,0,1.0192306,0)
da.Size=UDim2.new(0,370,0,107)_b.Parent=da
_b.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)_b.Position=UDim2.new(0,0,0.800455689,0)
_b.Size=UDim2.new(0,370,0,21)_b.Font=Enum.Font.Arial;_b.Text="Made by TungNoPro "
_b.TextColor3=Color3.new(0,1,1)_b.TextSize=20;ab.Parent=da
ab.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ab.Position=UDim2.new(0,0,0.158377,0)
ab.Size=UDim2.new(0,370,0,44)ab.Font=Enum.Font.ArialBold;ab.Text="Status: Active"
ab.TextColor3=Color3.new(0,1,1)ab.TextSize=20;local bb=game:service'VirtualUser'
game:service'Players'.LocalPlayer.Idled:connect(function()
bb:CaptureController()bb:ClickButton2(Vector2.new())
ab.Text="Roblox tried to kick u but i kicked him instead"wait(2)ab.Text="Status : Active"end)
            end
        })

local Section = TabTwo:AddSection({
	Name = "Auto Hatch Egg - Fast, Remove Animation"
})

 _G.autoHatch = true
    _G.selectEgg = "Starter"

    function autoHatch()
        while _G.autoHatch == true do
game:GetService("ReplicatedStorage").RemoteEvents.EggOpened:InvokeServer(_G.selectEgg,"Single")
            wait(0)
        end
    end
TabTwo:AddToggle({
Name = "Auto Hatch",
    Default = false,
    Callback = function(Value)
                _G.autoHatch = Value
                    autoHatch()
                    end
        })

TabTwo:AddDropdown({
	Name = "Choose Eggs",
	Default = "Starter",
	Options = {"Starter", "Candy", "Cyber", "Desert", "Magma", "Ocean", "Swag"},
	Callback = function(Value)
		_G.selectEgg = Value
    print(_G.selectEgg)
	end    
})

 local Section = TabTwo:AddSection({
    Name = "Click Toggle Auto Hatch Slowly Or Else Get Bug(Rejoin)"
})

end

function CorrectKeyNotification()
OrionLib:MakeNotification({
    Name = "Correct Key!",
    Content = "You have entered correct key!",
    Image = "rbxassetid://4483345998",
    Time = 2
})
end

function IncorrectKeyNotification()
OrionLib:MakeNotification({
    Name = "Inorrect Key!",
    Content = "You have entered incorrect key!",
    Image = "rbxassetid://4483345998",
    Time = 2
})
end

local Tab = Window:MakeTab({
    Name = "Key",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

Tab:AddTextbox({
    Name = "Enter Key",
    Default = "",
    TextDisappear = true,
    Callback = function(Value)
        _G.KeyInput = Value
    end      
})

Tab:AddButton({
    Name = "Check Key",
    Callback = function()
if _G.KeyInput == _G.Key then
 CorrectKeyNotification()
Hub()
 else
 IncorrectKeyNotification()
      end   
end
})
local Section = Tab:AddSection({
    Name = "Key in: discord.gg/RbMeKAHg"
})
