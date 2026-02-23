A Steam Session tutorial files by ItsMeBro using Advanced Steam Sessions plugins

Youtube: https://www.youtube.com/@ItsMeBro</br>
Discord: https://discord.com/invite/Gr9sPP2</br>
Patreon: https://www.patreon.com/c/ItsMeBro


Dependencies: Plugins</br>
Advanced Sessions</br>
Advanced Steam Sessions</br>
Steam Online Subsystem</br>
Steam Sockets

How to use:

1. Download code
2. Paste Steam folder inside your content folder.
3. Paste code from the bottom into the bottom of DefaultEngine.ini
4. Enable Plugins
5. Add SteamSeshComp to your gameplay controller (Example: BP_FirstPersonController)
6. On Begin Play, Inside the controller, set controller ref for the component and initialize the component.

In the image you can see steps 3 and 4

<img width="1897" height="868" alt="image" src="https://github.com/user-attachments/assets/e525b0d0-8ef4-4958-8d67-51a8a5b3e876" />


[/Script/Engine.GameEngine]
!NetDriverDefinitions=ClearArray
+NetDriverDefinitions=(DefName="GameNetDriver",DriverClassName="/Script/SteamSockets.SteamSocketsNetDriver",DriverClassNameFallback="/Script/SteamSockets.SteamNetSocketsNetDriver")

[OnlineSubsystem]
DefaultPlatformService=Steam

[OnlineSubsystemSteam]
bEnabled=true
SteamDevAppId=480
bInitServerOnClient=true

[/Script/OnlineSubsystemSteam.SteamNetDriver]
NetConnectionClassName="OnlineSubsystemSteam.SteamNetConnection"
