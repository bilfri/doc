---
title: Flasher l'ISO YunoHost
template: docs
taxonomy:
    category: docs
routes:
  default: '/burn_or_copy_iso'
---

Maintenant que vous avez téléchargé l’image ISO de YunoHost, vous devez la mettre sur un support physique. Classiquement, il s'agit d'une **Clé USB** ou d'une **Carte SD**.

![](image://sdcard.jpg?resize=100)
![](image://micro-sd-card.jpg?resize=100)
![](image://usb_key.png?resize=150)
![](image://cd.jpg?resize=100)

---

### (Recommandé) Avec Etcher

Téléchargez <a href="https://etcher.io/" target="_blank">Etcher</a> pour votre système d'exploitation et installez-le.

![](image://etcher.gif)

Branchez votre clef USB, selectionnez l'ISO YunoHost puis cliquez sur 'Flash'

### Avec UNetbootin

Téléchargez <a href="https://unetbootin.github.io/">UNetbootin</a> pour votre système d'exploitation et installez-le.

![](image://unetbootin.png)

Branchez votre clef USB, selectionnez l'ISO YunoHost puis cliquez sur 'OK'

### Avec `dd`

Si vous êtes familier avec la ligne de commande, il est possible de flasher la clef USB ou carte SD avec `dd`.  Vous pouvez identifier le nom du périphérique avec `fdisk -l` ou `lsblk`. Une carte SD s'apelle typiquement `/dev/mmcblk0`. ATTENTION à faire attention de prendre le bon nom !

```bash
# Remplacer /dev/mmcblk0 par le nom de votre périphérique
dd if=/chemin/de/yunohost.iso of=/dev/mmcblk0
```

### CD/DVD

Pour les anciens matériels, il vous faut peut-être utiliser un CD/DVD. Le logiciel à utiliser est différent suivant votre système d’exploitation.

* Sur Windows, utilisez [ImgBurn](http://www.imgburn.com/) pour écrire l’image sur le disque

* Sur macOS, utilisez [Disk Utility](http://support.apple.com/kb/ph7025)

* Sur GNU/Linux, vous avez plusieurs choix, tels que [Brasero](https://wiki.gnome.org/Apps/Brasero) ou [K3b](http://www.k3b.org/)