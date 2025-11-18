# win_terminal
Shared windows terminal settings, for better vim expirience. Settings.json needs to be located here:

winget install --id Microsoft.PowerShell --source winget
I really hate this, but anaconda keep installing on different locations. This is not the prefered one, but I am landing here out of despair.
winget install -e --id Anaconda.Miniconda3 --location %userprofile%\Miniconda3

%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json
move %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings_backup.json
mklink /H "%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json %userprofile%.config\win_terminal\settings.json
TODO: Test this command
git clone https://github.com/kjaern/win_terminal.git %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState

cp %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalStateBackup
rmdir -Force -Recurse -Confirm:$false %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState
git clone https://github.com/kjaern/win_terminal.git %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState
echo done


# Guess this dumpster fire can be a start of general full windows setup
winget install --id Microsoft.PowerToys --disable-interactivity --source winget


TODO: create a hard link to powershell.json in Split-Path $PROFILE.CurrentUserCurrentHost in github

