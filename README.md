# UUplugin-install-AX6

## Description

This is a modified install script  of UU game booster for `Redmi AX6 (RA69)` .

It maybe work on other Xiaomi stock OS based on openwrt . 

The original script is here . [网易UU加速器——玩出超快感，全球加速72小时免费体验 (163.com)](https://uu.163.com/router/direction.html)

## Before Download

You should gain ssh access of your router ,which can be found easily on the Internet .

## Usage

1. Download the script 

   ```shell
   wget https://raw.githubusercontent.com/kaedeair/UUplugin-install-AX6/main/install.sh -O install.sh
   ```

2. execute the script

   ```shell
   /bin/sh install.sh openwrt $(uname -m)
   ```

   It will print `sn=<your mac>` , if successful .

   The log path is `/tmp/install.log` and  `/tmp/monitor.log` .

3. install kmod-tun

   ```shell
   opkg update
   opkg install kmod-tun
   ```

   It is up-to-date usually on stock OS.

## How it works

I found the folder `/usr` is read-only , but  `/data` is writeable.

Therefore , I replace all the path  in the script .