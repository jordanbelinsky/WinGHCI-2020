# WinGHCI-2020
A recompiled version of the no-longer supported WinGHCI program for Haskell platform development.

For my class CISC 360 - Programming Paradigms, for the first half of the semester we were required to do Haskell compiling, and were recommended WinGHCI as an option for Windows-based development environments.

Unfortunately, WinGHCI has been left unsupported for many years, but by downloading the original source code and recompiling it in Visual Studio 2019, I was able to get a working executable, so long as chocolatey has already been used to install the haskell platform.

These files follow the installation instructions provided by Ryan Johnson (thanks Ryan!): https://ryanjohnson.website/install-guide-for-winghci-2522/

This repo provides the final executable file for those who do not want to recompile it themselves using Visual Studio 2019!

## Steps for Installation:
### Configure chocolatey
1. Run command prompt (cmd.exe) with administrator priveleges.
2. Paste the following and hit enter:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
3. If no errors, type **choco** to verify installation success!

### Install Haskell Platform
1. Run command prompt (cmd.exe) with administrator priveleges.
2. Paste and run the following **two** commands:
```
choco install haskell-dev
```
```
refreshenv
```
3. Haskell Platform is now successfully installed!

### Install WinGHCI
Lastly, is the simplest step. Download the WinGHCI.exe from this repo, and place it wherever you prefer to access it from on your PC. You can now double click to run it, and you are good to go!

Best of luck with Haskell functional programming!
