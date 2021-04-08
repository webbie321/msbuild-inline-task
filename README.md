# msbuild-inline-task

Author: Casey Smith, Twitter: @subTee

Modified by: Webbie, Twitter: @WebbieSec

License: BSD 3-Clause


---

@Webbie: 

I made some modifications to the original "executes PowerShellCommands.xml" file by Casey Smith.
Original: https://github.com/3gstudent/msbuild-inline-task/blob/master/executes%20PowerShellCommands.xml


My issue with the original version is that we create a new runspace with every command entered. This implies that whatever you run doesn't impact the following commands.

So I moved things around to have everything run in the same runspace. 

Also used Powershell instances rather than working explicitly with a pipeline (just my preference).


Didn't test too much yet, but it seems to work so far.

```
C:\Windows\Microsoft.Net\Framework\v4.0.30319\msbuild.exe c:/users/public/powershell.csproj
```
