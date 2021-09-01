# Grub theme
## Doki Doki Literature Club

### Instalation

First, you have to clone the theme on your local machine in the `/boot/grub/themes` folder
*be aware to permitions*

```BASH
$ cd /boot/grub/
$ git clone https://github.com/Allan-POINT/Grub-Theme.git
```

Then you have to edit the `/etc/default/grub` file and past thoses lines at the end of the file :

```
#Customisation
GRUB_BACKGROUND="/boot/grub/Grub-Theme/monika/images/monika.jpg"
GRUB_THEME="/boot/grub/Grub-Theme/monika/theme.txt"
```

To check if all is working, do this :
```
$ grub-mkconfig
```
if you find the lines above in the output of the command, it's OK

`Found theme: /boot/grub/themes/monika/theme.txt`
and
`Found background image: /boot/grub/Grub-Theme/monika/images/monika.jpg`

Then, you can aplly the changment to GRUB
```
$ mv /boot/grub/grub.cfg /boot/grub/grub.cfg.bak
$ grub-mkconfig >> /boot/grub/grub.cfg
$ update-grub2
```
if the commend `update-grub2` is not found, you can try `update-grub`

Finaly, restart your computer to see the result
