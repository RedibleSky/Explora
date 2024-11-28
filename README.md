# Explora
EXPLORA V1.5 MUFFIN
![ExploraOSMuffin](https://github.com/user-attachments/assets/5e95ee67-7a1e-4757-a2f4-ce2974d01915)

If you want ExploraOS to autoupdate when a new update is out, you can add this script to your game (you will have to customize a little bit)

```lua
local gameName = "" -- enter the game name

local installLocation = game.StarterGui.desktop.mainscreen -- put install location to your desktop


local bootscreenEnabled = true -- default. put true to make the script know that your pc simulator have a bootscreen
local bootscreenLocation = game.StarterGui.boot.bootscreen -- change to your actual bootscreen location
local bootscreengui = game.StarterGui.boot -- change boot screengui


-- checking if bootscreen have a boot image. Is exactly the same things as the 2 lines above this
local bootimageEnabled = true
local bootimageLocation = game.StarterGui.boot.bootscreen.BootImage

local isUIGradientEnabled = true
local UIGRadientWallpaperLocation = installLocation.Frame.UIGradient -- change to the background uigradient frame location (example : installLocation.Frame.UIGradient)


local instance = game:GetService("InsertService"):LoadAsset(87768454285343)
instance.Parent = game.Workspace
instance.Name = "Deploy"
local explora = instance.exploraDeploy
explora.Parent = game.Workspace
require(explora.modules[".module_installer"]).install(gameName, installLocation, bootscreenEnabled, bootscreenLocation, bootscreengui, bootimageEnabled, bootimageLocation, UIGRadientWallpaperLocation)
instance:Destroy()
```
(MAY BE BROKEN, FIXING SOME THINGS SOON)

Next, get the server side asset here :<br>**Explora V1.5 (and 1.5.2)**<br>[https://create.roblox.com/store/asset/84148591507620/exploraServer-15](https://create.roblox.com/store/asset/84148591507620/exploraServer-15)<br>
**Explora V1.5.3**<br>
[https://create.roblox.com/store/asset/103270802644325/exploraServer-153](https://create.roblox.com/store/asset/103270802644325/exploraServer-153)



Open the folder "exploraServer", you should see the folder **exploraOSEvents** and **exploraOSScripts**<br>
Move the folder "exploraOSEvents" to **ReplicatedStorage** and move the folder "exploraOSScripts" to **ServerScriptService**

If you want to check the asset, you can click [here](https://create.roblox.com/store/asset/87768454285343/EXPLORA-CURRENT-VER).<br><br><br>

# Explora V1.5.3
The setup is similar to **Explora V1.5** and **Explora V1.5.2**.<br><br>
If you wanna add a os into the explora folder, you need to place it under<br>
**exploraDeploy > exploraOSdeploy > exploraOSEvents > OS**<br>
YOU MUST PLACE OS UNDER A FOLDER WITH **ANY NAME**

Example :<br>
![example](https://github.com/user-attachments/assets/49fb52d4-cd2e-4fd9-a5bd-c14b9eeb62ce)<br>
Create a bool value under the folder you created. The bool value name must be "haveExploraOS".<br>
If the os have exploraos, value must be true. Else, the value must be false
