## Set Wireshark Config Dir
Get Wireshark to pick up another Config Dir, which is used for profiles etc.
I use a OneDrive location as path to share between machines.

Generally: set env variable **WIRESHARK_CONFIG_DIR**

MacOS - to get it working also for the GUI app

1.
```
sudo vim /Library/LaunchAgents/wireshark-environment.plist
```
2.
add the following code. 
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>my.environment.variables</string>
    <key>ProgramArguments</key>
    <array>
        <string>launchctl</string>
        <string>setenv</string>
        <string>WIRESHARK_CONFIG_DIR</string>
        <string>/Users/roberthe/Library/CloudStorage/OneDrive-GoToTechnologiesUSALLC/Wireshark/</string>
    </array>
    <key>RunAtLoad</key>
    <true/>
</dict>
</plist>
```
3.
```
sudo launchctl load /Library/LaunchAgents/wireshark-environment.plist
```
4. 
Log out and in again, afterwards you can verify with
```
launchctl getenv WIRESHARK_CONFIG_DIR
```


