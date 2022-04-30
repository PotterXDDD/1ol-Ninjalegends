local DiscordLib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/discord%20lib.txt")() local win = DiscordLib:Window("1ol : Ninja Legend") local serv = win:Server("Main", "rbxassetid://7040391851") local Tab1 = serv:Channel("AutoFarm") Tab1:Toggle("Auto-Farm",false, function(v) _G.AutoFarm = v while _G.AutoFarm do wait() game:GetService("Players").LocalPlayer.ninjaEvent:FireServer("swingKatana") end end)

Tab1:Toggle("Auto-Sell",false, function(v) _G.AutoSell = v while _G.AutoSell do wait() if game:GetService("Players").LocalPlayer.PlayerGui.gameGui.maxNinjitsuMenu.Visible == true then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(71.43441772460938, 18.315448760986328, -48.1461067199707) end end end)

Tab1:Seperator()

local Weaponlist = {} local Weapon = nil

for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do table.insert(Weaponlist,v.Name) end

Tab1:Dropdown("Select Weapon",Weaponlist, function(currentOption) Weapon = currentOption end)

Tab1:Toggle("Auto Equip",false, function(a) AutoEquiped = a end)

spawn(function() while wait() do if AutoEquiped then pcall(function() game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon)) end) end end end) Tab1:Seperator()

Tab1:Toggle("Collect Coin And Yin",false, function(c) _G.AutoCollect = c while _G.AutoCollect do wait(1) for i,v in pairs(game:GetService("Workspace").spawnedCoins.Valley:GetChildren()) do game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab1:Seperator()

Tab1:Toggle("Buy All Sword",false, function(omg) _G.BuyAllSword = omg while _G.BuyAllSword do wait()
game:GetService("Players").LocalPlayer.ninjaEvent:FireServer("buyAllSwords") end end)

Tab1:Toggle("Auto Buy Belt",false, function(xd) _G.AutoBuyBelt = xd while _G.AutoBuyBelt do wait() game:GetService("Players").LocalPlayer.ninjaEvent:FireServer("buyAllBelts") end end)

-- page 2 local Tab2 = serv:Channel("Teleport") Tab2:Button("Island 1", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Enchanted Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 2", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Astral Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 3", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Mystical Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 4", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Space Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 5", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Tundra Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 6", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Eternal Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 7", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Sandstorm" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 8", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Thunderstorm" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 9", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Ancient Inferno Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 10", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Midnight Shadow Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 11", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Mythical Souls Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 12", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Winter Wonder Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 13", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Golden Master Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 14", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Dragon Legend Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 15", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Cybernetic Legends Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 16", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Skystorm Ultraus Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 17", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Chaos Legends Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 18", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Soul Fusion Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 19", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Dark Elements Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 20", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Inner Peace Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)

Tab2:Button("Island 21", function() DiscordLib:Notification("Notification", "Teleported!", "Okay!") for i,v in pairs(game:GetService("Workspace").islandUnlockParts:GetDescendants()) do if v.Name == "Blazing Vortex Island" then game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame end end end)
