This is a script for taking screenshots at interval. I created it in 2015 year. The script is based on this [post](https://www.sysadmins.lv/blog-ru/delaem-skrinshoty-sredstvami-powershell.aspx) 

- 1 - path - folder fpr screenshots
- 2 - Interval - interval beetwen (sec)
- 3 - ScreenFormat - file format (jpg (doesn't work),png)
- 4 - File - parameter source (inline or file)

**Default:**

- **Path**: %systemdrive%
- **Interval**: 10 sec
- **ScreenFormat**: png

**Example exe:**

- screen.exe -Arguments -Path "C:\new folder" -Interval 15 -ScreenFormat "jpg"

**Example ps1:**

- powershell.exe -ExecutionPolicy Bypass -NoProfile -File "screen.ps1" -Path "C:\" -Interval 15 -ScreenFormat "jpg"
- powershell.exe -ExecutionPolicy Bypass -NoProfile -File "screen.ps1" -Path "C:\new folder" -Interval 15 -ScreenFormat "jpg"

Exe file without console. Quality is not regulated.

**Required for installation:**
- Powershell
- .NET Framework v4.0

Check your execultionpolicy

**File description:**
- screen.exe - compiled exe from ps1 using PowerGUI Script Editor (меню Tools > Compile Script).

	PS2EXE compilation command:

	PS C:\> ps2exe.ps1 -inputFile C:\screen.ps1 C:\screen.exe -sta -noConsole -noOutput -noError
- screen.ps1 - orginal script 
- screen_debug.exe - with confole
- setup.ps1 - script for install or unistall
- setup.bat - run setup.ps1
- screen.ini - file settings

C:\SCREENSHOTER>screen.exe -Arguments -Path "\\\\192.168.9.15\store\SCREEN\technical" -Interval 15 -ScreenFormat "jpg"
