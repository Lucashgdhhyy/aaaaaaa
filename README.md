local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
OrionLib:MakeNotification({
	Name = "Checando Https",
	Content = "Demora um pouco",
	Image = "rbxassetid://4483345998",
	Time = 8
})
wait(4)

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
OrionLib:MakeNotification({
	Name = "Https Encontrado! Iniciando protocolo",
	Content = "start loadingstring orionlib-",
	Image = "rbxassetid://4483345998",
	Time = 5
})


wait(5)

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Player = game.Players.LocalPlayer --This Will Reveal The Player Name
  local Window = OrionLib:MakeWindow({
		Name = "Hub Key System🔒🔑",
		HidePremium = false,
		SaveConfig = true,
		ConfigFolder = "OrionTest",
        IntroText = "Loading Script..."       
}) --This Will Load The Script Hub

function MakeScriptHub()
                loadstring(game:HttpGet("https://raw.githubusercontent.com/Lucashgdhhyy/AAA/main/README.md"))() 
end

OrionLib:MakeNotification({
	Name = "Logado!",
	Content = "Precisa de key"..Player.Name..".",
	Image = "rbxassetid://4483345998",
	Time = 5
}) --Notification

getgenv().Key = "FAzure" --Put The Correct Key Here
getgenv().KeyInput = "string" --Require For The Key To Work

local Tab = Window:MakeTab({
	Name = "Key",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
}) --Making A Tab

Tab:AddTextbox({
	Name = "Key",
	Default = "Enter Key.",
	TextDisappear = true,
	Callback = function(Value)
		getgenv().KeyInput = Value
	end	  
}) --You Will Enter The Key Here

Tab:AddButton({
    Name = "Cheque Key",
    Callback = function()
        if getgenv().KeyInput == getgenv().Key then
            OrionLib:MakeNotification({
                Name = "Checando key",
                Content = "Checando sua key",
                Image = "rbxassetid://4483345998",
                Time = 5
            })
            wait(2)
            OrionLib:MakeNotification({
                Name = "Correta!",
                Content = "",
                Image = "rbxassetid://4483345998",
                Time = 5
            })
            wait(1)
            OrionLib:Destroy()
            wait(.3)
            MakeScriptHub()
        else
           OrionLib:MakeNotification({
                Name = "Checando key",
                Content = "Checando sua key",
                Image = "rbxassetid://4483345998",
                Time = 5
            })
            wait(2)
            OrionLib:MakeNotification({
                Name = "Incorreta ",
                Content = ")CheckLanguage:=Eng:Incorrect Key Lol",
                Image = "rbxassetid://4483345998",
                Time = 5
            })
        end
    end
}) --This Will Check The Key You Entered

local Tab = Window:MakeTab({
	Name = "Pegue Keyless",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
}) --Making A Tab


Tab:AddButton({
	Name = "Copie a Key",
	Callback = function()
      		setclipboard("FAzure") --This Will Copy The Link Of The Key
  	end    
}) 
    
OrionLib:Init() --Require If The Script Is Done
