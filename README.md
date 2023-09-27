local BananaPeel = getconnections or get_signal_cons
if BananaPeel then
    for i,v in pairs(BananaPeel(LocalPlayer.Idled)) do
        if v["Disable"] then
            v["Disable"](v)
        elseif v["Disconnect"] then
            v["Disconnect"](v)
        end
    end
end
 
local Folder = Instance.new("Folder")
Folder.Parent = workspace
Folder.Name = "PathFindPartsFolder"
 
if LocalPlayer.PlayerGui.MainUI.Initiator.Main_Game.RemoteListener.Modules:FindFirstChild("BananaPeel") then
    LocalPlayer.PlayerGui.MainUI.Initiator.Main_Game.RemoteListener.Modules.BananaPeel.Name = "NoTouch" -- Fuck you BananaPeel
end
