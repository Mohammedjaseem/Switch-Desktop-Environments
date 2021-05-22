# Switch-Desktop-Environments

----
## XFCE Desktop ##
----
### How to install XFCE Desktop Environment in Kali Linux:
Command:

```apt-get install kali-defaults kali-root-login desktop-base xfce4 xfce4-places-plugin xfce4-goodies```

### How to remove XFCE in Kali Linux:
Command:

```
 apt-get remove xfce4 xfce4-places-plugin xfce4-goodies
```
----
## KDE Desktop ##
----
### How to install KDE Plasma Desktop Environment in Kali Linux:
Command:

```
 apt-get install kali-defaults kali-root-login desktop-base kde-plasma-desktop
```
### How to install Standard Debian selected packages and frameworks in Kali Linux:
Command:
```
 apt-get install kali-defaults kali-root-login desktop-base kde-standard
```
### How to install KDE Full Install in Kali Linux:
Command:
```
 apt-get install kali-defaults kali-root-login desktop-base kde-full
```
### How to remove KDE on Kali Linux:
Command:
```
 apt-get remove kde-plasma-desktop kde-standard
```
----
## LXDE Desktop ##
----
#### How to install LXDE Desktop Environment in Kali Linux:
Command:
```
 apt-get install lxde-core lxde kali-defaults kali-root-login desktop-base
```
#### How to remove LXDE on Kali Linux:
Command:
```
 apt-get remove lxde-core lxde
```
----
## GNOME Desktop ##
----
#### How to install GNOME on Kali Linux:
Command:
```
 apt-get install gnome-core kali-defaults kali-root-login desktop-base
```
#### How to remove GNOME on Kali Linux:
Command:
```
 apt-get remove gnome-core
```
----
## Cinnamon Desktop ##
----
#### How to install Cinnamon Desktop Environment in Kali Linux:
Command:
```
 apt-get install kali-defaults kali-root-login desktop-base cinnamon
```
#### How to remove Cinnamon Desktop Environment in Kali Linux:
Command:
```
 apt-get remove cinnamon
```
----
## MATE Desktop ##
----
#### How to install MATE Desktop Environment in Kali Linux:
#### This installs the base packages
Command:
```
 apt-get install kali-defaults kali-root-login desktop-base mate-core
```
#### Or this to install mate-core and more extras
Command:
```
 apt-get install kali-defaults kali-root-login desktop-base mate-desktop-environment
```
#### Or this to install mate-core + mate-desktop-environment and even more extras.
Command:
```
 apt-get install kali-defaults kali-root-login desktop-base mate-desktop-environment-extra
```
#### How to remove MATE Desktop Environment in Kali Linux:
Command:
```
 apt-get remove mate-core
```
Now the only problem is MATE doesn't show the nice Kali Linux Menu. Fix posted by Silver Moon

To fix this edit the following file.
Command:
```
 leafpad /etc/xdg/menus/mate-applications.menu
```
In the file go down to the section named Internet and add the following line
HTML Code:
```
<!-- Kali Linux Menu -->
<MergeFile type="path">applications-merged/kali-applications.menu</MergeFile>
```
So it should look something like this
HTML Code:

```
 <!-- Internet -->
  <Menu>
    <Name>Internet</Name>
    <Directory>mate-network.directory</Directory>
    <Include>
      <And>
        <Category>Network</Category>
      </And>
    </Include>
  </Menu>   <!-- End Internet -->
<!-- Kali Linux  -->    
  <MergeFile type="path">applications-merged/kali-applications.menu</MergeFile>
```
