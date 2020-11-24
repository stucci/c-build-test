### msvc
command file path: `C:\Program Files (x86)\Microsoft Visual Studio\2017\BuildTools\VC\Tools\MSVC\14.16.27023\bin\Hostx86\x86`

* preprocess
```powershell
cl /EP /P main.c
# -> main.i
```

* compile and assemble
```powershell
cl /c /FA main.c
# -> main.asm and main.obj
```

* link
```powershell
link main.obj
# -> main.exe
link /DLL main.obj
# -> main.dll
```

##### other

* all
```powershell
cl main.c
# -> main.obj and main.exe
```

* create library
```powershell
lib main.obj
# -> main.lib
```

* only assemble
```powershell
ml /c main.asm
# -> main.obj
```
