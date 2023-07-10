---
layout: page
title: Installation
menubar: ote_docs_menu
show_sidebar: false
toc: false
hero_height: is-small
---

Installing OSINT Template Engine involves a series of simple steps which must be completed in the correct
sequence for the installation to be successful.

_**NOTE:** `vX.X.X` refers to the version number e.g. `v1.0.0`_

## **To Download**
The installers and portable executable files are available on the OTE's Github repository [release page](https://github.com/3nock/OTE/releases) or official website [download page](https://SpiderSuite.github.io/download/).

OTE currently supports Windows and Linux operating systems with x64 architecture. 

On the release page there are two types of download packages for each of the two systems i.e. `installers` and `portable executable`.

- Installers

Installers will install OTE and its dependencies in default choosen location on your machine. 

The installers are `OTE_vX.X.X_win64_installer.exe` for windows and `OTE_vX.X.X_linux_installer.run` for linux.

- Portable executables

Portable executables do not need any installation; you simply download and use directly. 

The portable executables are `OTE_vX.X.X_win64.zip` for Windows and `OTE_vX.X.X_linux.AppImage` and `OTE_vX.X.X_linux.tar.gz` for Linux

## **To Install**
Please Note: OTE is a Graphical User Interface application so all of the steps in this guide refer to the OTE GUI.

* **For Windows Portable Executables:**

Download and extract `OTE_vX.X.X_win64.zip` archive and place it at your choosen location, extract the archive then run OTE.exe simply by double clicking on the program.

* **For Linux Portable Executable:**

Download `OTE_vX.X.X_linux.AppImage` and place it at your chosen location, then run it simply by `double clicking` 

or 

using command line with the command:

```bash
./OTE_vX.X.X_linux.AppImage
```

OR

Download `OTE_vX.X.X_linux.tar.gz` archive and place it at your choosen location.
 
Extract the archive on desired location (you can use GUI option or command line: 

```bash
tar –xzf OTE_vX.X.X_linux.tar.gz
```
Then run it simply by double clicking on the `OTE/OTE` 

or 

using command line with the command 

```bash
./OTE/OTE
```

* **For Windows Installer:**

Download `OTE_vX.X.X_win64_installer.exe` then run the installer, then fill in the required information such as installation location and shortcut names procedually until you finish the installation procedure.

* **For Linux Installer:**

Download `OTE_vX.X.X_linux_installer.run` then run the installer using the command line :

```bash
./OTE_vX.X.X_linux_installer.run
```
Then fill in the required information such as installation location and shortcut names precedually until you finish the installation procedure.

_**NOTE:**_

In most windows environment OTE will run on the first try but case of SipderSuite fails to run on the first try on windows, this could be an indication that your machine does not contain the required MSVC-redistributable package. 

Don’t worry, OTE comes packaged with the required MSVC-redistributable package in case of this. 

Simply Install the MSVC-redistributable package which comes with OTE (OTE/vcredist_x64.exe)

Also In case OTE fails to connect to the internet and shows SSL errors, install the OpenSSL package which comes packaged with OTE (OTE/Win64 OpenSSL v1.1.1n Light.msi).

## **To Uninstall**
To uninstall OTE for portable OTE, just delete the OTE folder and you are done.  For installed OTE run the uninstaller located in the OTE installation directory (OTE/maintanance_tool.exe).
