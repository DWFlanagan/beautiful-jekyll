---
layout: post
title: Keeping Microsoft Teams alive with launchd
image: 
tags: [OS X]
---

Microsoft Teams quits randomly on Mac without restarting.

On OS X, you can use launchd to keep an application running as described [here](https://superuser.com/questions/135344/how-to-use-launchd-to-ensure-an-application-is-running).

I created a file called `com.microsoft.teams.plist` in `~/Library/LaunchAgents/ `with the contents:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
        <key>KeepAlive</key>
        <true/>
        <key>Label</key>
        <string>org.quicksilver</string>
        <key>ProgramArguments</key>
        <array>
                <string>/Applications/Microsoft Teams.app/Contents/MacOS/Teams</string>
        </array>
</dict>
</plist>
```

Now when Teams quits randomly `launchd` starts it back up again.

