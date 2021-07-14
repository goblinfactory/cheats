# 1 liner cheats
random cut and paste cheats that I need from time to time 

## Dark grey powershell prompt

> function prompt { write-host $PWD -foregroundcolor darkgray;  " >> "; }



## shorter VScode terminal prompt

> function prompt { $pd = new-object System.IO.FileInfo $PWD;  write-host  "$((''+$PWD).replace($HOME, '').replace($pd.Name, ''))"  -ForegroundColor darkgray -nonewline; write-host $pd.Name -ForegroundColor green; return '> '; }



```powershell
function prompt { 
        $pd = new-object System.IO.FileInfo $PWD
        write-host  "$((''+$PWD).replace($HOME, '').replace($pd.Name, ''))"  -ForegroundColor darkgray -nonewline
        write-host  $pd.Name -ForegroundColor green
        return '> '
}
```
