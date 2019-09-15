# Nachos 3.4  
This is a operating system course lab.  
  
## Install  
Nachos 3.4 runs on 32-bits machine, so you should get Ubuntu 32-bits to run this project.  
Extract nachos-3.4.tar, and  
```
cd nachos-3.4/code
make
cd threads
make depend
make nachos
```  
OK! If there is no error, you have finished installing.  
  
## Debug with vscode  
Now you need to install [vscode 32-bits](https://code.visualstudio.com/updates/v1_35).  
**NOTE**: There is no support for vscode which is 32-bits version after May 2019. So the link above is the latest version.  
Run  
```
sudo dpkg -i code_1.38.1-1568209190_amd64.deb
```  
after you finish download, and open nachos-3.4 with vscode.  
Then you should create a directory named `.vscode` and a file named `launch.json` in it.  
`launch.json:`  
```
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "(gdb) MYLaunch",
            "type": "cppdbg",
            "request": "launch",
	    // You can change this line to run other nachos in other directory.
            "program": "${workspaceFolder}/code/threads/nachos",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": false,
            "MIMode": "gdb",
            "setupCommands": [
                {
                    "description": "Enable pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ]
        }
    ]
}
```
Now you can press `F5` to debug!  
**NOTE**: Every time you change a line, you should re-make the project before debuging.
