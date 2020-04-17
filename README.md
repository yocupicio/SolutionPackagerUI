# SolutionPackager
Solution Packager is a tool to automate Dynamics 365 Solution Build & Deploy. 
This tool comes with Dynamics 365 Software Development Toolkit (SDK). 
This tool can decompose a Microsoft Dynamics 365 compressed solution file into multiple XML files and other files, 
so that these files can be easily managed by a source control system. 
This tool also can compress back into a solution file.

# SolutionPackagerUI
The SolutionPackagerUI is a windows application tool that lets you pack and unpack a Dynamics 365 solution .zip file using SolutionPackager SDK.

## Requirement
To use SolutionPackagerUI, first you need to download the latest Dynamics 365 SDK assemblies. 
The SDK assemblies can be downloaded from NuGet. 
Follow the steps [here](https://docs.microsoft.com/en-us/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).

## Installation
Download [SolutionPackagerUI.exe](https://raw.githubusercontent.com/yocupicio/SolutionPackagerUI/master/SolutionPackagerUI.exe) to your "devtools" directory under tools\CoreTools directory.
Example:
 C:\devtools\Tools\CoreTools
 
## Usage
The following sections show you how to run the tool and how to use it with managed and un-managed solutions.

To Extract, Browse for compressed solution file and then click Extract button.
 ![extract](https://raw.githubusercontent.com/yocupicio/SolutionPackagerUI/master/images/extract.png)

To Pack, type the folder where the solution was extracted or navigate to the directory using Browse button.
Enter the location where the .zip file will be saved.
Click Pack button.
 ![pack](https://raw.githubusercontent.com/yocupicio/SolutionPackagerUI/master/images/pack.png)
