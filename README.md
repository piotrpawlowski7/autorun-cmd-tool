## autorun-cmd-tool

Small tool for CLI commands.

## How does it work?

Create a file to store your macros (DOSKEYs).
"C:\bat\macros.doskey"
```
ls=dir $* $T
ip=ipconfig $T
desk=cd C:\Users\User\Desktop\ $T
pcode=cd C:\Users\User\code $T
gst=git status $T
gc=git commit $T
gco=git checkout $T
gl=gitpull $T
gpom=git pull origin master $T
gp=git push $T
gd=git diff $T
gb=git branch $T
up=cd.. $T
ex=exit $T
np=notepad $T
dota2=E:\STEAM\steamapps\common\"dota 2 beta"\game\bin\win64\dota2.exe $T
overwatch=E:\BATTLENET\Overwatch\"Overwatch Launcher".exe $T
diablo=E:\BATTLENET\"Diablo III"\"Diablo III Launcher".exe $T
chrome=C:\"Program Files (x86)"\Google\Chrome\Application\Chrome.exe $T
rgb=C:\"Program Files (x86)"\GIGABYTE\RGBFusion\RGBFusion.exe
```
Go to the registry editor.
```
HKEY_LOCAL_MACHINE\Software\Microsoft\Command Processor\
```
Right-click and add a new "String Value" sub-key. Name it Autorun.
Right-click -> New -> String Value

Right-click it and Modify the Value data.
Right-click -> Modify -> Value data -> DOSKEY /MACROFILE="C:\bat\macros.doskey"
Good to go.

If u dont have admin persmissions, use this way:
```
==> reg add "HKCU\Software\Microsoft\Command Processor" /v Autorun /d "doskey /macrofile=\"c:\bat\macros.doskey\"" /f
The operation completed successfully.

==> reg query "HKCU\Software\Microsoft\Command Processor" /v Autorun

HKEY_CURRENT_USER\Software\Microsoft\Command Processor
    Autorun    REG_SZ    doskey /macrofile="c:\bat\macros.doskey"
```
