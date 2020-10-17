# donyaOS installation guide

## Install

Just only use compressed package `donyaOS-build.tar.xz`

Suppose we have another dist hard disk `sdb` to install donyaOS on it
Create a 100 MB partition in it.

## Format it

`sudo mkfs.ext4 /dev/sdb1`

## Mount new created `sdb1`

`sudo mkdir "$base_dir"/donya_release/`
`sudo mount /dev/sdb1 "$base_dir"/donya/`

## Extract donyaOS inside it

`sudo tar xJf ${base_dir}/donyaOS-build.tar.xz -C "$base_dir"/donya/`

## Install grub in MBR

`sudo grub-install --root-directory="$base_dir"/donya/ /dev/sdb`

## Run with qemu

`sudo qemu-system-x86_64 /dev/sdb`

## Build from source

`./run`

---

## download dependancy with

`wget -nc -i packages-list.txt -P packages/`
