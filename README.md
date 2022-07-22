
# Fully Automate IOS Update Tool with Netmiko

With this python code, intended to automatically update IOS (f.e. 2960X) and IOS-XE (f.e. Cat9300L) based devices (incl. up to 4 Stacks) using the Netmiko framework. The script is able to perform the update on multiple devices in parallel. This makes it possible to run an OS update on many devices at once and ensures that the update process is automated and therefore always runs the same.

Illustrate the following concepts :

- Fully automate Update process of IOS on given IOS-based Switch
- Including 2960x-Stacks or 9300L-Stacks (tested with up to 4)
- Process handling happend parallel by threating
- Including MD5-Check after copy of Software to Switch to ensure integrity
- Stacks supported as well
- New feature, support of Cisco IOS-XE Device like Cat9300L
- When update finished, reload device

## Installation

Please use Netmiko at least 2.4.2 ---> `pip install netmiko`

Netmiko has the following requirements (which pip will install for you)

    Netmiko >= 2.4.2
    Paramiko >= 2.4.3
    scp >= 0.13.2
    pyserial
    textfsm

Python version must be at least v3.6

I also added you `requirements.txt`, where you can find all dependencies

## How to use

Modifiy the variable `<devices = read_devices('path-to-devices_file')>`

After done so, you need to update the devices_file with the needed information of the switches you want to update.

Use `<IP-Address>,<device-type (f.e. cisco-ios or cisco-xe)>,<hostname>`

When this files are prepared, run the main script and put in the asked infos:

* Filename (file needs to be located in same file as script)
* Username
* Password

.[sample](./sample.png)