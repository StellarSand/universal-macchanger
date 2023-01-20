# macchanger-py

**macchanger** tool allows you to change the MAC address of a network interface on Linux, macOS and Windows systems.

Changing the MAC address can be useful in various situations, such as hiding your device's identity on a network, or bypassing MAC address filters.



## Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Check interfaces & current MAC](#check-interfaces--current-mac)
- [Usage](#usage)
- [Contributing](#contributing)



## Prerequisites
- [Python3](https://www.python.org/downloads/)



## Installation
**1. Clone this repo:**
```
git clone https://github.com/the-weird-aquarian/macchanger-py.git
```

**2. Move into the project directory:**
```
cd macchanger-py
```

**3. Give executable permissions to the script (Not required for Windows):**
```
chmod +x macchanger
```



## Check interfaces & current MAC
You can check all the interfaces & their current MAC address using terminal/cmd:
- Linux: `ip a`
- Windows: `ipconfig \all`
- macOS: `networksetup -listallhardwareports`



## Usage
```
python3 macchanger -i <interface> -m <MAC>
```

Random MAC address can be set using:
```
python3 macchanger -i <interface> -r
```

**Examples:**
```
python3 macchanger -i wlan0 -m 00:11:22:33:44:55
```

```
python3 macchanger -i "Wireless Network Adapter" -r
```



## Contributing
Pull requests can be submitted [here](https://github.com/the-weird-aquarian/macchanger-py/pulls). Any contribution to the project will be highly appreciated.