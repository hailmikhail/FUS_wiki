[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

# Wabbajack Troubleshooting

There are a lot of different scenarios where Wabbajack will produce an error. I recommend re-running Wabbajack before posting anything. Wabbajack will continue where it left off so you lose no progress.

In general, if there are connection issues or stuff like "Got a 521 from ...." or "Build server is down", sometimes you just need to wait it out. Maybe restart the process or possibly the whole PC, but don'T worry, you won't lose your progress!

**"Unable to download openvr_api.dll"**: 

Verify your files through Steam via following these steps:

- Close Wabbajack
- Open your Steam Library tab
- Right-click the game title that you are modding
- Select Properties
- Select Local Files
- Select Verify Integrity of Local Files
- Launch Wabbajack and rerun the installer

**"Missing nexusapikey"**:

This can happen if the nexus is unavailable. Check if you can reach it in your browser.

**"Could not download x"**:

If a mod updated and the old files got deleted, it is impossible to download them. In this case just wait till I update the Modlist.

**"x is not a whitelisted download"**:

This can happen when we update the modlist. Check if a new update is available and wait if there is none. Sorry for the inconvenience.

**"Wabbajack could not find my game folder"**:

Wabbajack will not work with a pirated version of the game. If you own the game on Steam, but get this error, go back to the [beginning](#first-time-installation) and make sure everything is set up correctly.

**"Windows is reporting that a virus has been detected"**:

Windows 10 has started to auto quarantine the usvfs_proxy_x86.exe file from the latest version of Mod Organizer 2 saying a threat was detected . This is a known false postive confirmed by the MO2 Devs. You can fix this by adding an exemption for MO2 Folder to your Antivirus. Example for windows defender can be found [here](https://www.thewindowsclub.com/exclude-a-folder-from-windows-security-scan).