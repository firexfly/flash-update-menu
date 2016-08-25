# flash-update-menu
Update all software on Debian 8

flash-update-menu is a script which allows a user to update all their software from a menu. The script is intended for Debian  GNU/Linux; the purpose is to make sure that family members, not familiar with Linux are able to keep their software up to date. Originally the main problem was that the Debian package `flashplugin-nonfree` is not always updated quickly after new versions of flash player are released. This script therefore gets the latest version direct from Adobe.

When the script also grew to include a way to keep the rest of the software on the system up to date, it was necessary to make it menu driven.

## Installation:
`mkdir ${HOME}/.update_menu`<br>
`cd ${HOME}/.update_menu`<br>
`git clone https://github.com/firexfly/flash-update-menu.git`<br>
`mv flash-update-menu/* .`<br>
`rmdir flash-update-menu`

#### Optional
Create a .desktop:<br>
`cd #To the location you want your .desktop to be.`<br>
`touch flash-update-menu.desktop`<br>
Populate the file with the following lines (editing them for your own system):

[Desktop Entry]<br>
Type=Application<br>
Name=flash-update-menu.desktop<br>
Exec=/path/to/flash-update-menu<br>
Path=/path/to/.update_menu<br>
Icon=/path/to/logo.jpg #Debian have some open use logos [here](https://www.debian.org/logos/)<br>
Terminal=true

---

## Use:

Either<br>
	1 Double click flash-update-menu.desktop<br>
	2 `./flash-update-menu.desktop`<br>
	3 `${HOME}/.update_menu/flash-update-menu`

This will present you with the main menu as follows:

>Menu<br>
>    1. Update/install Flash Player<br>
>    2. Update software (recommended)<br>
>    3. dist-upgrade (see help for warnings)<br>
>    0. EXIT
>
>h for help
>
>What would you like to do?

Simply type in the option for the action you would like to carry out and follow the on-screen prompts.
Read help.txt for further assistance.
