# Xcode To External Hard Drive
My workaround for downloading and installing Xcode on an External Hard Drive to save space on my main HD.

## Steps:

1. Create a new user for your mac.
- Go to "System Preferences > Users & Groups" and click the "+" button to create a new user. 

# ![alt text](https://github.com/bji219/XcodeToExternalHardDrive/blob/main/Screen%20Shot%202021-04-14%20at%208.19.08%20PM.png)

3. Set the new user's home directory to be your external hard drive.
- Right click on the new user and choose "Advanced Options"
- Change their Home Directory to "/Volumes/*ExternalHardDriveName*"

# ![alt text](https://github.com/bji219/XcodeToExternalHardDrive/blob/main/Screen%20Shot%202021-04-14%20at%208.17.24%20PM.png)

5. Enable downloads and apps from anywhere using the command:

```
sudo spctl --master-disable
```

- The result should be somethign like this:

# ![alt text](https://github.com/bji219/XcodeToExternalHardDrive/blob/main/Screen%20Shot%202021-04-14%20at%208.13.51%20PM.png)

5. Log out of the normal user account. 
6. Log in as the new user and download the desired version of Xcode from https://developer.apple.com/download/more/?=xcode
- Note: Check your OS version before downloading the latest Xcode as it may not be compatible. 
8. Unzip the file using the terminal command:

```
xip -x /path/to/xip_File/Xcode_*version*.xip
```

Note: While unzipping, temporary files still took up some space on my main hard drive. This means you need at least 35 gigs or so of free space to unzip Xcode. Using this method will save around 10-12 gigs of storage initially because the .xip file will always be on the external HD. Once the unzipping is complete, those 35 gigs of space will be free again. 

## And that's it!
