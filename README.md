## autorun-cmd-tool

Small tool for CLI commands.

## How does it work?

Create a file to store your macros (DOSKEYs).
"C:\bat\macros.doskey"

ls=dir $* $T
up=cd.. $T
ex=exit $T
np=notepad $T
dota2=E:\STEAM\steamapps\common\"dota 2 beta"\game\bin\win64\dota2.exe

Go to the registry editor.

HKEY_LOCAL_MACHINE\Software\Microsoft\Command Processor\
Right-click and add a new "String Value" sub-key. Name it Autorun.
Right-click -> New -> String Value

Right-click it and Modify the Value data.
Right-click -> Modify -> Value data -> DOSKEY /MACROFILE="C:\bat\macros.doskey"
Good to go.
