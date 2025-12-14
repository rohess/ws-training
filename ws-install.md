# HowTo install Wireshark
## Windows & MacOS
Download Wireshark installer from https://www.wireshark.org/download.html
Install it, saying yes to everything except USB capture
## Linux (Ubuntu)

(for other distros modify as  applicable)
In most distros its in the standard repos, but often not very recent
For Ubuntu you will get currently (2025) Version 4.2 - this is enough for first steps.

You definitely want version 4.X, as the UI changed a lot from 3.X
It pays to run the latest stable, as nice features are coming in frequently.
```
sudo add-apt-repository ppa:wireshark-dev/stable
sudo apt update
sudo apt install wireshark
sudo apt show wireshark
```
Detailed: https://www.geeksforgeeks.org/how-to-install-and-use-wireshark-on-ubuntu-linux/

### Newer versions on Linux
You build it from source. Its moderatly difficult.

Currently (12/2025) you will get Version 4.7

I did run two scripts for this:

Prep script for dev env from:

https://github.com/wireshark/wireshark/blob/master/tools/debian-setup.sh

some 3rd party build script

https://gist.github.com/syneart/2d30c075c140624b1e150c8ea318a978

run via:

```
wet -O - https://gist.githubusercontent.com/syneart/2d30c075c140624b1e150c8ea318a978/raw/build_wireshark.sh | sh
```
