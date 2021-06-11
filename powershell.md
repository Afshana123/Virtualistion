# Windows Powershell

`Set-Location` - set your location

`get-command` - will give a list of every command in powershell

`get-service` - which will find the services in the system. If you want to filter it out you can do this too e.g `get-service "vm*"`

`get-hotfix` - this is the update for the powershell itself so if there is a bug in powershell, it will give you a list of things with a desccription of whether it's an update or security update 

if you want to install the hotfix then you write in the command line `get-hotfix -id HotFixID` - make sure you copy and paste the specific hotfix ID key which will be listed for you to see

If you want to print something on the screen 
`Write-Host "Welcome to Sparta"` - this will display the message 

Powershell is a scripting lanaguage 

If you want to define a variable:
`$value = READ-HOST`
Then enter in your value 

If you want to read the value you do: `write-host $value`

`get-childitem Env:` - to get all the environment variables 




