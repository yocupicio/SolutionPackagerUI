# SolutionPackagerUI
The SolutionPackagerUI is a windows application tool that lets you pack and unpack a solution zip file.

## Usage

### Download Latest version of Microsoft.CrmSdk.CoreTools using PowerShell

```powershell

##
##Create sdk directory (Change to your preferred directory)
New-Item -ItemType Directory -Force -Path C:\sdk
Set-Location -Path C:\sdk
##


$sourceNugetExe = "https://dist.nuget.org/win-x86-commandline/latest/nuget.exe"
$targetNugetExe = ".\nuget.exe"
#Remove-Item .\Tools -Force -Recurse -ErrorAction Ignore
Invoke-WebRequest $sourceNugetExe -OutFile $targetNugetExe
Set-Alias nuget $targetNugetExe -Scope Global -Verbose

##
##Download CoreTools
##
./nuget install  Microsoft.CrmSdk.CoreTools -O .\Tools
md .\Tools\CoreTools
$coreToolsFolder = Get-ChildItem ./Tools | Where-Object {$_.Name -match 'Microsoft.CrmSdk.CoreTools.'}
move .\Tools\$coreToolsFolder\content\bin\coretools\*.* .\Tools\CoreTools
Remove-Item .\Tools\$coreToolsFolder -Force -Recurse


##
##Remove NuGet.exe
##
Remove-Item nuget.exe
```

### Download SolutionPackagerUI.exe using PowerShell

```powershell
$sourceSolutionPackagerUIExe = "https://github.com/yocupicio/SolutionPackagerUI/raw/master/SolutionPackagerUI.exe"
$targetSolutionPackagerUIExe = ".\SolutionPackagerUI.exe"
Invoke-WebRequest $sourceSolutionPackagerUIExe -OutFile $targetSolutionPackagerUIExe
Set-Alias nuget $targetSolutionPackagerUIExe -Scope Global -Verbose
```