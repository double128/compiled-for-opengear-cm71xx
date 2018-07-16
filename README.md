# Stuff I've compiled for the Opengear CM71xx
A selection of random software I compiled for the Opengear CM71xx running uClinux. It's a bit annoying compiling stuff for this device so I figured I'd upload the final compiled products here. 

Unless stated otherwise in the individual folders, everything gets installed to /bin. You must have the CDK to install these files properly. In the CDK, you must place these files in the appropriate folders in the /romfs folder. Then, you can make the image and upload it to the device. 

These files are compiled with the arm-linux-gnueabi-20140823-tools toolchain available for download at Opengear's website. I have not tested these files with any other Opengear/ARM devices because I am only working with a CM71xx at the moment. These files were configured with settings set by the CDK's maketool, so I do not think these files would work on devices besides the CM71xx.

Also, I have not done any testing with screen (it did work, I just ended up not needing it because picocom suited my needs better), but I am certain that the contents of the folder "terminfo" gets placed in the /etc/terminfo folder in romfs. I also did not do much testing with pam-script as it turned out I didn't need it. 

I can confirm that su and picocom work as intended and have been a lifesaver for me in regards to working with the Opengear CM71xx. 

su was compiled from source from BusyBox and was compiled as static so I did not require the BusyBox libraries. The CM71xx's filesystem already has a BusyBox bin file that I did not want to overwrite in fear of messing up the pre-configured BusyBox settings. So, it is much better to compile the BusyBox applets as individual binaries so that they do not rely on BusyBox itself. 

As an additional note, su was configured to not have --help commands. If this is an issue, bring it up to me and I can compile it with said configurations.

Please feel free to suggest things for me to compile if you are using this device and struggling to get things working. I pretty much know this device like the back of my hand at this point.
