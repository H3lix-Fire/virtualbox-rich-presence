# VirtualBox Rich Presence

[![pypresence](https://img.shields.io/badge/using-pypresence-00bb88.svg?style=for-the-badge&logo=discord&logoWidth=20)](https://github.com/qwertyquerty/pypresence)

## Notice

This project was originally created by vidhanio, all I did was fix a bug that made the id of the machine state appear 1 above it's actual state. This is likely due to lists starting at 0, and the id system starting at 1. All I did was modify the return value of the id to be properly set. This project will not be recieving any updates from me, but will remain open for pull requests, issues, etc.

## Installation

First, clone the repository.

```cmd
git clone https://www.github.com/H3lix-Fire/virtualbox-rich-presence
```

Then go to the [VirtualBox downloads page](https://www.virtualbox.org/wiki/Downloads) and download the VirtualBox SDK.

After downloading it, extract the `VirtualBoxSDK-x.x.x-xxxxxx.zip` file and run the installer.

```cmd
cd installer
```

```cmd
python vboxapisetup.py install
```

Then, install the required modules.

```cmd
cd virtualbox-rich-presence
```

```cmd
pip install -r requirements.txt
```

## Config

The [config](config.example.ini) allows you to change what is displayed on your rich presence.

### Available Values

- `{machine name}`: Name of the machine in VirtualBox (e.g. "My Windows Machine")
- `{os name}`: Name of OS. (e.g. "Microsoft Windows")
- `{os version name}`: Name of OS version. (e.g. "Windows 8")
- `{os version image}`: Image key of OS version. (e.g. "windows_8")
- `{architecture}`: OS architecture (e.g. "64")
- `{architecture image}`: Image key of OS architecture (e.g. "64")
- `{icon}`: Image key of VirtualBox Icon.

## Usage

Make a copy of [`config.example.ini`](config.example.ini) and remove the `.example`, then [edit it](#config) if you want.

Run `main.py`.
