# Microsoft Windows Tools

-----------------------------------------
## Attach Spotify to music key on keyboard (Windows 10)
1. Open Regedit.exe
```Note: Editing Registry Can potentially cause system issue
I suggest you backup the registry before you edit anything in it
to do this simply do File >> Export.
Save it somewhere where you will remember where you put it.
This Edit shouldnt break anything however theres always a chance.
```
2. Goto HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\AppKey\16
```Note This is the key for your media key/music key on the keyboard
if you wish to change any other keys you may. Here are what which one corresponds to:
  15. Mail Key
  16. Media/Music Key
  17. Windows Explorer Key
  18. Calculator Key
  7. Webpage/Home Key (Not to be confused with HOME key)
```
3. From here you can choose what you'd like to use there are two Keys you can use:
  1. Association: This corresponds with Protocols such as: mailto and http
  2. ShellExecute: This run an exe program in this case spotify.exe

4. If you'd like to use association:
    1. If it is there already good. all you need to do is right-click >> Modify...
       If it is not already it should be ShellExecute, Do the following:
          1. Do right-click >> Delete, then right-click in the blank area with Name, Type, and Data
          2. Select New >> String Value
          3. In the first field(Under Name) type `Association`
          4. Press Enter
    2. Under Value data insert `spotify`
    3. Click `OK`
    4. Test it out. If it does not work (this did not work for me) try the next method
    
 5. If that did not work for you or you want to use ShellExecute Do the following:
    1. If it is there already good. all you need to do is right-click >> Modify...
       If it is not already it should be Association, Do the following:
        1. Do right-click >> Delete, then right-click in the blank area with Name, Type, and Data
        2. Select New >> String Value
        3. In the first field(Under Name) type `ShellExecute`
        4. Press Enter
    2. Under Value data insert `spotify.exe`
    3. Click `OK`
    4. Test it out. Hopefully this works out for you. I used the spotify app from the windows app store and this work fine
    
 6. If there are any issues feel free to make a new issue on this github.
 
----------------------------------
  
