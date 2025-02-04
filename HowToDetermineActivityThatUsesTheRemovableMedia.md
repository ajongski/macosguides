# How To Determine Activity That Uses The Removable Media

## The Problem:
Cannot eject the removable media such as flash drive or memory card because the MacOS system says that it is being used by a program. The system does not explictly tell what that program is.

## Experienced on:
Apple Macbook Pro 14 M1 Pro

## Summary of the Fix
1. Determine the name of the removable media
2. Determine the PID of the activity related to the removable media
3. Kill the activity corresding to the PID
4. Remove the removable media

## Procedure
1. Open the Terminal
2. In the type ```df``` and press enter. You will see the list of the volumes, the one that has no ```/dev/``` is most likely your removable media. You can also confirm by looking at its name through the ```Finder```
3. Once you get the name of the removable media, type in the terminal ```lsof /Volumes/[name of your removable media without brackets]```. It will show the acivity using your removable media. Take note of its PID.
4. Open the ```Activity Monitor``` app, look for the activity corresponding to the PID found in ```Step 3```. Once found, highlight it and click the ```x``` (stop) button.
5. Remove the removable media
