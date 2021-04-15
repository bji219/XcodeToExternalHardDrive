# Xcode To External Hard Drive
My workaround for downloading and installing Xcode on an External Hard Drive to save space on my main HD.

Steps:

1. Create a new user for your mac.
2. Set the new user's home directory to be your external hard drive.
3. Enable downloads and apps from anywhere using the command: sudo spctl --master-disable
4. Log out of the normal user account. 
5. Log in as the new user and download the desired version of Xcode from https://developer.apple.com/download/more/?=xcode
6. Unzip the file using the terminal command: xip -x /path/to/xip_File/Xcode_*version*.xip

Note: While unzipping, temporary files still took up some space on my main hard drive. This means you need at least 35 gigs or so of free space to unzip Xcode. Using this method will save around 10-12 gigs of storage initially because the .xip file will always be on the external HD. Once the unzipping is complete, those 35 gigs of space will be free again. 
