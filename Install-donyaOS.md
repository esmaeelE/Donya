# donyaOS Guide

[This is only draft version of installation guide take care what are you doing]

## How to install donyaOS

# donyaOS team highly recommend that only test this version of donyaOS inside test box machine like 
virtulaize GNU/Linux distro, like debian in a Virtulbox application to reduce risk of data loss.

## Prerequests

### What you need before install

1. Inside virtualbox create a debian 10 headless machine and install default applications.
2. Create a new partition in `/dev/sdb1` in size of 100 MB.

Now you can start the process of installation.

### Step by Step installation process

After download donyaOS repository 

1. Download the necessary packages with "downloader.sh" scrip
`downloader.sh` get required packages for building donyaOS from source and place then in packages directory 
It isn't download them if exists before, so you can place each one you have instead of redownload them.
This feature good for anyone like me that have not reliable internet.

2. Run this command to generate one script for Create installer script

`cat scripts/step[1..5].sh > run.sh`
`chmod +x run.sh`

4. Now run generated script to build and install donyaOS

`./run.sh`


