# Welcome to grub2 default kernel how to

> Be ensure you made backups of these listed files
- /boot/grub2/grub.cfg
- /boot/grub2/grubenv
- /etc/default/grub

> List all available kernel versions
```
awk -F\' '$1=="menuentry " {print $2}' /boot/grub2/grub.cfg
```

> Change =N to **saved**
```
grep -i default /etc/default/grub
```

> Just for information
```
grub2-editenv list
```

> Set as you need. 0 is first element
```
grub2-set-default N
```

> Make grub2 config
```
grub2-mkconfig -o /boot/grub2/grub.cfg
```

