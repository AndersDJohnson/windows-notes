# windows
Windows notes

## Apps
* [Process Explorer]
* [Process Hacker]
* ClipX: Clipboard manager
* AltDrag: Drag windows like Linux
* StrokeIt: Mouse gestures
* PowerMenu: Windows always-on-top, transparency, CPU priority, etc.
* grepWin: File search GUI
* NetWorx: network speed monitor
* SumatraPDF: PDF reader
* SpeedFan: Fan speed and tempurature monitoring
* Caffeine: Prevent screen saver / hiberate
* ImgBurn: Burn and image discs
* Ext2Mgr: Manage Linux partitions
* Pidgin: Instant messaging (IM) client (see [pidgin_notes.md](https://gist.github.com/AndersDJohnson/c47b13465a27bc013359))
* Fiddler: Web debugging proxy
* [clumsy](https://jagt.github.io/clumsy/index.html): network simulation (throttling, etc.)
* [NirSoft Utils](http://www.nirsoft.net/utils/)

## Tips

### Disable "Libraries"
* [http://www.howtogeek.com/howto/21462/](http://www.howtogeek.com/howto/21462/)
* [http://www.askvg.com/how-to-disable-libraries-feature-in-windows-7/](http://www.askvg.com/how-to-disable-libraries-feature-in-windows-7/)

## PowerShell Prompt Here
* http://www.hanselman.com/blog/IntroducingPowerShellPromptHere.aspx

## Symlinks (in PowerShell)

### Directories
```
cmd /c mklink /d "C:\Path\To\Source\Folder" "C:\Path\To\Destination\Folder"
```
### Files
```
cmd /c mklink "C:\Path\To\Source\File.txt" "C:\Path\To\Destination\File.txt"
```


## Which process listening on port?
There's a native GUI for Windows:
`resmon.exe`
(or Start > All Programs > Accessories > System Tools > Resource Monitor)

Then tab "Network", then "Listening Ports" accordian.

(http://stackoverflow.com/a/23718720)

## Which process has file open?

Use [Handle], [Process Explorer], or [Process Hacker].


## Cleanup
* [Autorun Disk Cleanup Tool](http://www.makeuseof.com/tag/automatically-windows-7-clean-obsolete-files/) ([cleanmgr.exe](http://support.microsoft.com/kb/253597))

## Commands

Get system architecture:
```
wmic os get osarchitecture
```



[Process Explorer]: http://technet.microsoft.com/en-us/sysinternals/bb896653.aspx
[Process Hacker]: http://processhacker.sourceforge.net/
[Handle]: https://technet.microsoft.com/en-us/sysinternals/bb896655.aspx
