# NadOS (Défis personnel)

## NadOS est un kernel compilé avec les outils busybox, l'idée m'est venu en voyant le dépôt de TEDDAC/BorvOS

Mon but étant de mieux comprendre le noyaux linux et le chargement d'un système d'exploitation en général

-----------------------
## Sources
- https://github.com/TEDDAC/BorvOS --> Inspiration
- https://busybox.net/ --> 1.33.2
- https://kernel.org/ --> 6.0.9
-----------------------

## Arborescence du projet
- `boot`: dossier contenant les fichiers nécessaires au démmarrage
- `nados.iso`: fichier ISO bootable contenant le projet compilé
- `rootbuild.tar`: fichier compressé contenant la racine du système

## Boot avec qemu
```
$ qemu-system-x86_64 -m 2048 -kernel ./kernel -initrd ./ramdisk -nographic -append "console=ttyS0"
```
---------------------

## demo
![demo qemu](./demo/virtualbox_iso_demo.png)