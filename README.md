# Post-installation Tools for Ubuntu
After installing ubuntu, we have to set-up various tools but we can't find them in one place.

## Dual Boot Setup
If you are willing to set up dual boot in your pc or laptop, you can follow this tutorials from youtube( if you are new).  
- If your pc's bios system is UEFI: Click [UEFI/GPT](https://www.youtube.com/watch?v=iSGJkg33aJg)  
- If your pc's bios system is Legacy: Click [Legacy/MBR](https://www.youtube.com/watch?v=YymM8n8gNZY)
### Some basic tools
Sometimes many tools can be setup by using this. Not everytime but sometimes it helps a lot.  
Curl: 
```bash
sudo apt install curl
```
Snap:
```bash
sudo apt install snap
```

## Visual Studio Code setup
Go to the [VS code](https://code.visualstudio.com/Download) official webpage and download the latest version of VS code with ***.deb*** extension.
then copy and paste these commands in your terminal. before proceed to the terminal, make sure that your are in that directory where the vscode 
file downloaded.  

```bash
sudo dpkg -i code_1.66.2-1649664567_amd64.deb
```
Sometimes there is an issue with dpkg. No need to worry. Every problem has a solution. dpkg error can be solved. If you face any problem like...

```bash
dpkg: unrecoverable fatal error, aborting:
reading files list for package 'linux-headers-3.16.0-31': Input/output error
E: Sub-process /usr/bin/dpkg returned an error code (2)
A package failed to install.  Trying to recover:
```
or,

```bash
dpkg: unrecoverable fatal error, aborting:
E: Sub-process /usr/bin/dpkg returned an error code (2)
A package failed to install.  Trying to recover:
```
just try some commands using your terminal.

1st solution:
```bash
sudo dpkg --configure -a
```
2nd solution:
```bash
sudo apt-get -f install
```
then try to reinstall the package.
if u still have the error after run `sudo dpkg --configure -a` #remove the file where u have the error after going to the 
location `cd location` `rm -rf file-name`[for eg. 0004] #then try again `sudo apt-get -f install` Hope it will work.  
