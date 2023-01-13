Pub installs executables into C:\Users\Zaman Sheikh\AppData\Local\Pub\Cache\bin, which is not on your path.
You can fix that by adding that directory to your system's "Path" environment variable.
A web search for "configure windows path" will show you how.

how to fix that?
To add the directory where Pub installs executables to your system's "Path" environment variable on Windows, follow these steps:

Press the Windows key + R to open the Run dialog box.
Type "sysdm.cpl" and press Enter to open the System Properties dialog box.
Click on the "Advanced" tab, and then click on the "Environment Variables" button.
Under "System variables," scroll down and select "Path," and then click on the "Edit" button.
Click on the "New" button and enter the directory where Pub installs executables, which is "C:\Users\Zaman Sheikh\AppData\Local\Pub\Cache\bin"
Click "OK" on all open windows to save the changes.
Close and reopen any open command prompt or terminal windows for the changes to take effect.
Alternatively, a web search for "configure windows path" will give you more detailed instructions and alternative methods for editing the Path environment variable.




ZAMAN SHEIKH
> firebase logout
firebase : File C:\Users\Zaman 
Sheikh\AppData\Roaming\npm\firebase.ps1 cannot be loaded because 
running scripts is disabled on this system. For more information, 
see about_Execution_Policies at 
https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ firebase logout
+ ~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityExc  
   eption
    + FullyQualifiedErrorId : UnauthorizedAccess

how to fix that?
This error message is indicating that the execution of PowerShell scripts is currently disabled on your system, which is preventing the firebase command from running. To fix this, you will need to change the execution policy on your system to allow scripts to run.

You can change the execution policy by running the following command in a PowerShell window as an administrator:

Copy code
Set-ExecutionPolicy RemoteSigned
This command sets the execution policy to "RemoteSigned," which means that scripts that you have written yourself will be able to run, but scripts downloaded from the internet will need to be digitally signed by a trusted publisher before they can run.

Alternatively, you can set the execution policy to "Unrestricted" if you want to run all scripts, including downloaded from internet.

Copy code
Set-ExecutionPolicy Unrestricted
After running the above command, you should be able to run the firebase logout command without any issues.

Note that if you are not the administrator of the machine, you will have to ask your administrator to change the execution policy for you.
