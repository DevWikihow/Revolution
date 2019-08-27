**How to insert the module?**
1. Select your script 
https://i.imgur.com/nL5VOqz.png
2. Click Insert on the plugin
https://i.imgur.com/AVvJRRh.png
3. The Module will have been inserted
https://i.imgur.com/jrqFsZZ.png

**I can't insert the module**

Take it here as a free model 
https://roblox.com/library/3636674984/Revolution

**I can't even insert that GRRRRRRRRRRR**

Try running this in the cmd bar:
```
game:GetService("InsertService"):LoadAsset(3636674984).Parent = workspace
```
**Where can I find the documentation?**
Right here: https://devforum.roblox.com/t/revolution-documentation/339243

**I want to give an idea, how can I do so?**
Right here: https://devforum.roblox.com/t/which-functions-should-i-add-to-my-modulescript/311606

**How can I use this???**

Easily! Here's a little example:

```
local players = game:GetService("Players") --Players service
local M = require(script.Revolution) --The module
local L = M.L --Leaderstats module
local D2 = M.D2 --datastore2 module

players.PlayerAdded:Connect(function(plr)
	local D = D2("Coins",plr)
	local stats = L.CreateLeaderstats(plr)
	L.MakeStat(plr,"NumberValue",D:Get(10),"Coins")
	while wait(5) do
		L.IncrementStat(plr,"Coins",10)
		D:Increment(10)
	end
end)
```
Here I create leaderstats and using Kampfkarren's datastore2, which is built into Revolution, I save the leaderstats & load them.
