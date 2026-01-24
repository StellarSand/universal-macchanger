# universal-macchanger

Spoof the MAC address of network interfaces on GNU/Linux, macOS and Windows systems.

Inspired by [GNU MAC Changer](https://salsa.debian.org/debian/macchanger/), this project extends the functionality beyond GNU/Linux, making it compatible across all platforms.
<br>Spoofing the MAC address can be useful in various situations, such as hiding your device's identity on a network, or bypassing MAC‑based network restrictions.



## Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Available options](#available-options)
- [Check interfaces & current MAC](#check-interfaces--current-mac)
- [Usage](#usage)
- [Issues](#issues)
- [Contributing](#contributing)
- [Credits](#credits)
- [License](#license)



## Features
- Set a specific MAC address on any network interface
- Set a fully random MAC address
- Set a MAC address of a specific vendor
- Set a random MAC address from any known vendor
- Display or search through a list of ~6,200 known vendors



## Prerequisites
- [Python3](https://www.python.org/downloads/)



## Installation
1. Clone this repo:
    ```
    git clone https://github.com/StellarSand/universal-macchanger.git
    ```

2. Move into the project directory:
    ```
    cd universal-macchanger
    ```

3. Give executable permissions to the script (Not required for Windows):
    ```
    chmod +x macchanger
    ```



## Available options
```
-h, --help              Show this help message and exit
-i, --interface         Interface name
-m, --mac               Set a MAC address manually
-r, --random            Set a random MAC address
-l, --list              Show all known vendors list
-s, --search            Search from known vendors list
-v, --vendor            Set MAC address based on index from vendors list
-rv, --randomvendor     Set a random MAC address from any known vendor
```



## Check interfaces & current MAC
You can check all the interfaces & their current MAC addresses using terminal/cmd:
- GNU/Linux: `ip a`
- Windows: `ipconfig \all`
- macOS: `networksetup -listallhardwareports`



## Usage
- Set a MAC address manually:
    ```
    python3 macchanger -i <interface> -m <MAC>
    ```
    **Example**:
    ```
    python3 macchanger -i wlan0 -m 00:11:22:33:44:55
    ```

- Set a random MAC address:
    ```
    python3 macchanger -i <interface> -r
    ```
    **Example**:
    ```
    python3 macchanger -i "Wireless Network Adapter" -r
    ```

- Search for a specific vendor:
    ```
    python3 macchanger -s <vendor>
    ```
    **Example**:
    ```
    python3 macchanger -s Cisco 
    ```

- Set MAC address based on index from vendors list:
    ```
    python3 macchanger -s <vendor>
    python3 macchanger -i <interface> -v <index>
    ```
    **Example**:
    ```
    python3 macchanger -s Cisco
    python3 macchanger -i eth0 -v W15
    ```

- Set a random MAC address from any known vendor:
    ```
    python3 macchanger -i <interface> -rv
    ```
    **Example**:
    ```
    python3 macchanger -i wlan0 -rv
    ```



## Issues
If you find bugs or have suggestions, please report it to the [issue tracker](https://github.com/StellarSand/universal-macchanger/issues). 
- Please search for existing issues before opening a new one. Any duplicates will be closed.



## Contributing
Pull requests can be submitted [here](https://github.com/StellarSand/universal-macchanger/pulls).



## Credits
- [GNU MAC Changer](https://salsa.debian.org/debian/macchanger/) for the known vendors list.



## License
This project is licensed under the terms of [GPL v3.0 license](https://github.com/StellarSand/universal-macchanger/blob/main/LICENSE).
