# windows-notes
Windows notes.

## Apps
* Windows Sysinternals Suite
  * [Process Explorer]
  * [Handle]
  * [PsFile] 
* [Process Hacker] (a fork of Process Explorer)
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
* [Git for Windows](https://git-scm.com/)
  * [Windows Credential Store for Git](http://gitcredentialstore.codeplex.com/)

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

## Which files changed recently in a directory?
```
dir c:\windows\ /aa /s /O-D
```
http://superuser.com/a/545554

## Which process listening on port?
There's a native GUI for Windows:
`resmon.exe`
(or Start > All Programs > Accessories > System Tools > Resource Monitor)

Then tab "Network", then "Listening Ports" accordian.

(http://stackoverflow.com/a/23718720)

## Which process has file open/locked?

```
openfiles
```
See [https://technet.microsoft.com/en-us/library/bb490961.aspx].

Use [Handle], [Process Explorer], [Process Hacker], or [PsFile] (supports network drives).


## Cleanup
* [Autorun Disk Cleanup Tool](http://www.makeuseof.com/tag/automatically-windows-7-clean-obsolete-files/) ([cleanmgr.exe](http://support.microsoft.com/kb/253597))

## Commands

* http://www.sprint.net.au/~terbut/usefulbox/msdoscmds.htm

### List processes

```
tasklist
```
```
tasklist /FI "IMAGENAME  eq explorer.exe"
```
```
get-process
```
```
wmic process list
```

### Get system architecture
```
wmic os get osarchitecture
```

### Touch file timestamp

PowerShell:
```
$(Get-Item $FILENAME).LastWriteTime = $(Get-Date)
```
MS-DOS:
```
copy %FILENAME% /B+ ,,/Y
```
(http://stackoverflow.com/a/7249328)


[Process Explorer]: http://technet.microsoft.com/en-us/sysinternals/bb896653.aspx
[Process Hacker]: http://processhacker.sourceforge.net/
[Handle]: https://technet.microsoft.com/en-us/sysinternals/bb896655.aspx
[PsFile]: https://technet.microsoft.com/en-us/sysinternals/bb897552.aspx
