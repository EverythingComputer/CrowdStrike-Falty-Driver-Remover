Here is the Code:
@echo off
title Crowd Strike BSOD Remover
echo This fixes the BSOD caused from the falty Crowdstrike Update
echo Make sure your drive is unlocked from bit locker
pause
takeown /a /f C:\Windows\System32\drivers\CrowdStrike\C-00000291.sys
icacls C:\Windows\System32\drivers\CrowdStrike\C-00000291.sys /grant administrators:f
del C:\Windows\System32\drivers\CrowdStrike\C-00000291.sys
echo x=msgbox ("The Driver may have been removed. The Computer will restart in 15 Seconds" ,0, "Done") >>C:\Note.vbs
Start C:\Note.vbs
shutdown -r -f -t=15
exit

The bat was converted to a exe
