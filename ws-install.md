# HowTo install Wireshark
## Windows & MacOS
Download Wireshark installer from https://www.wireshark.org/download.html
Install it, saying yes to everything except USB capture.
## Linux 

In most distros its in the standard repos, but sometimes not very recent

For Ubuntu 26.04 you will get currently (11/2026) Version 4.6.9 - latest stable.

```
sudo apt install wireshark
sudo apt show wireshark
```
*Recommended:* install nightly builds from https://www.wireshark.org/download/automated/

This gives you v.5.1rc - Lots of useful changes and fixes (Linux users - build from source - the build system is quite nice)

I will use Wireshark 5 today

