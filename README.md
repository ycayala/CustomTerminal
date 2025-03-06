# CustomTerminal

https://learn.microsoft.com/en-us/windows/terminal/tutorials/custom-prompt-setup
#instalar fuentes necesarias
https://www.nerdfonts.com/font-downloads

#Instalar Oh My Posh para PowerShell
winget install JanDeDobbeleer.OhMyPosh
#opcional
winget install oh-my-posh

#Elija y aplique un tema de solicitud de PowerShell
notepad $PROFILE
#agregar las siguinetes lineas en notepad
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\paradox.omp.json" | Invoke-Expression
#guardar y salir


#ver todos los temas
Get-PoshThemes

#desbloquear ejecucion de scripts en power shell
Set-ExecutionPolicy -ExecutionPolicy Unrestricted

#agregar iconos necesarios, requiere admin powershell
Install-Module -Name Terminal-Icons -Repository PSGallery

#aplicar iconos
Import-Module -Name Terminal-Icons
