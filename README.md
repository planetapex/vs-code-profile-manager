<p align="center">
  <a href="" rel="noopener">
<img src='https://dummyimage.com/200x200/000000/FFFFFF.png?text=planetAPEX' width=200px height=200px  alt=''style="border-radius:50%" /></a>
</p>

<h2 align="center">
VS Code Profile Manager <!-- omit in toc --> </h2>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/planetapex/vs-code-profile-manager.svg)](https://github.com/planetapex/vs-code-profile-manager/issues)

![GitHub Pull Requests](https://img.shields.io/github/issues-pr/planetapex/vs-code-profile-manager.svg)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> 

## 🧐 About <a name = "about"></a> <!-- omit in toc --> 

This a small utility to manage Visual Studio Code Profiles for extensions. Currently VS Code maintains Extensions at a User or Workspace Level.

_**The Problem Statement**_
Some users asked if the extensions can be enable/disbaled for a specific project. So I tried to solve these.

> https://github.com/alefragnani/vscode-project-manager/issues/281
> https://github.com/microsoft/vscode/issues/81950
> https://github.com/Microsoft/vscode/issues/40109

> Throughtout the documentation I refer to the **"VS Code Original Shortcut"** as the one which comes with installation when VS code is installed.

For each workspace the user needs to Enable and Disable Extension , which can be Cumbersome.

To make things easier and centrally organized, you do not need to keep separate configuration of your settings. This makes backing up of settings (which includes extensions installed, information easier, by using extension you would be already familiar with, like, 

[Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

> User settings are configured and Extensions installed from the original shortcut, So that, original setup is not disturbed and easier to maintain a backup of the settings and extension list from a centralized point.

> Any Changes made to the configuration(settings.json ) will automatically be reflected.

Here are few points to keep in mind

* To keep settings , usually many developers , use extension like [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) to keep their settings backup.
* You need to to use the original VS code shortcut to Make changes to your settings and install any new extension. 
* Configure your extensions as detailed in the instructions of the Extension or using the Setting.json if necessary.
* Once you have Installed and configured your extensions, you can use the VS Code Profile Manager to add it to your profile

   VS Code Profile Manager will use the user settings.json and same installed extension.

<br> 

## 📝 Table of Contents <!-- omit in toc --> 

- [1. 🏗 Installation of VS Code Profile Manager](#1--installation-of-vs-code-profile-manager)
- [2. 🗄️ Backup of Your Configuration](#2-️-backup-of-your-configuration)
- [3. 🏁 Getting Started  <a name = "getting_started"></a>](#3--getting-started--)
- [4. ⚙️ Setting up Configuration Directories](#4-️-setting-up-configuration-directories)
  - [4.1. 2.1 🔧 Visual Studio Code Installation Folder](#41-21--visual-studio-code-installation-folder)
  - [4.2. 🔧 Profiles Base Folder](#42--profiles-base-folder)
  - [4.3. 🔧 Theme Selector](#43--theme-selector)
- [5. 🗃 Profiles Pane](#5--profiles-pane)
- [6. :twisted_rightwards_arrows: Extension List Window (Adding & Removing Extensions from your Profile)](#6-twisted_rightwards_arrows-extension-list-window-adding--removing-extensions-from-your-profile)
  - [6.1. Names Inconsistency [Rare Cases]](#61-names-inconsistency-rare-cases)
  - [6.2. Shortcut Keys](#62-shortcut-keys)
  - [6.3. Saving the profile](#63-saving-the-profile)
- [7. 🚴Running the Profile](#7-running-the-profile)
- [8. ⛏️ Built Using <a name = "built_using"></a>](#8-️-built-using-)
- [9. ✍️ Authors <a name = "authors"></a>](#9-️-authors-)
  - [9.1. ✍️ Social Links](#91-️-social-links)

## 1. 🏗 Installation of VS Code Profile Manager

* Download the MSI from
  + releases
  + as
* Run the installation
* The Installer will Install the application in Program Files\planetAPEX\VS Code Profile Manager Folder
* A Shortcut will be created on the desktop

## 2. 🗄️ Backup of Your Configuration

There is a profileMgr. SQLite file in the Program Files\planetAPEX\VS Code Profile Manager Folder. 
If you need to backup all your setting you can backup this file, which contains your profiles and extensions list.

## 3. 🏁 Getting Started  <a name = "getting_started"></a>

You have the following:

* Configuration Directories
* Profiles
* Extensions List

> All Configurations can be saved, so that on next run, you do not need to specify.

## 4. ⚙️ Setting up Configuration Directories

In order for the profile manager to work, it needs two directories the 

* Visual Studio Code Installation Folder
* Profile Base Folder

![configurationDirectories](/assets/configurationDirectories.png)

### 4.1. 2.1 🔧 Visual Studio Code Installation Folder

This is the folder where Visual Studio Code is installed, where code.exe exist.
It will detect the default folder for Visual Studio Code. However, in rare case , if it can not, you will have to identify the specific folder.

- 

I tried to solve the directory for:

* x86 installation of Visual Studio Code
* x64 installation of Visual Studio Code
* Chocolatey installation of Visual Studio Code

### 4.2. 🔧 Profiles Base Folder

This is the folder where you need to keep the profiles and their shortcuts.

> Probably, Some folder like Profiles in the D: drive.

### 4.3. 🔧 Theme Selector

There is also an option for Theme selector

## 5. 🗃 Profiles Pane

Create a new Profile, and click the edit to add extensions.

![ProfilesPane](/assets/ProfilesPane.png)

> Valid profile name consist of Alphabets and Digits only

You can delete your profile by clicking the delete button.

> Deletion of the profile has no effect on the configurations and extensions that are installed in the original VS Code.

## 6. :twisted_rightwards_arrows: Extension List Window (Adding & Removing Extensions from your Profile)

> The list only contains the extensions already installed in your system.
> As mentioned in [About](#about) you have to install your extension via the VS Code original shortuct

![ExtensionListWindow](/assets/ExtensionListWindow_gt0sjogrs.png)

My ***Quick Workflow*** is, 

* Start Searching extension in the combo box
* Select the desired extension with the up and down arrow keys, and hit enter
* This will select the Extension in the List box
* Now, you can press Ctrl+➡️ OR Ctrl+⬅️  arrow key to move into the other list box
* And, bring the cursor back to the Combo box to repeat the process for other extensions.

> You can select multiple extensions and move it.

### 6.1. Names Inconsistency [Rare Cases]

The names mentioned in the list box of the Extensions, are extracted from the cryptic names got from the Unique Identifier of the extensions, Like:

**cyberbiont.vscode-open-in-typora**

AFAIK, there was on other way around it to get it from the system. If someone is able to provide other way, please contact me.

Sometimes, there is inconsistency in the name of the extension, 
 E.g. The General Name ***"Open in Typora"*** , 
 However, the Unique Identifier of the extension is like:

**cyberbiont.vscode-open-in-typora**

 Now the name in the list box will be _***vscode Open in typora***_

So kindly check it in the VS Code extension List or [Microsoft Market place](https://marketplace.visualstudio.com/)

### 6.2. Shortcut Keys

These shortcut will work when a respective List box is in focus.

``` 

Ctrl+➡️	Will move the selected extensions to Right Listbox
Ctrl+⬅️	Will move the selected extensions to Left Listbox
Ctrl+Enter	Will Save the Form
```

### 6.3. Saving the profile

Saving the profile will create 2 shortcuts  

* One in the Profiles Folder
* Other on the Desktop

## 7. 🚴Running the Profile

Just double click the Shortcut and you are good to go.

## 8. ⛏️ Built Using <a name = "built_using"></a>

* [Powershell](https://docs.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7.1) - Scripting Language
* [DotNet v3](https://dotnet.microsoft.com/download/dotnet-framework) - Components
* [sqlite](https://www.sqlite.org/index.html)
* INI Confiuration

  
  

## 9. ✍️ Authors <a name = "authors"></a>

* M. Yasir Ali Shah[@planetapex](https://github.com/planetapex) - Idea & Initial work

### 9.1. ✍️ Social Links

* [My Personal Blog](https://apexfusion.blogspot.com/)
* [Oracle APEX Plugins](https://apex.oracle.com/pls/apex/f?p=83009:1::::::)
* [LinkedIn](https://www.linkedin.com/in/myasiralishah)
* [Github](https://github.com/planetapex)
* [Twitter](https://twitter.com/m_yasir_ali)
* [Facebook](https://www.facebook.com/yasir.alishah.75)
* [Email](mailto:yasirali.wizerp@gmail.com)
* [About Me](http://apexfusion.blogspot.com/p/about-me.html#info)
