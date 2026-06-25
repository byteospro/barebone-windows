# HOW TO INSTALL WINDOWS 95 BAREBONE ON YOUR VM OR AN OLD MACHINE

step 1 - install the WIN95_INSTALLMEDIA_BAREBONE_BOOTABLE.zip file on your computer

step 2 - extract it (you are in it right now)

step 3 - open "README_FIRST.txt" (you are in it right now)

step 4 (for a vm) - create a new vm with your desired settings , and mount the virtual iso file on the cd drive.

step 4 (for an old machine) - burn the virtual iso onto a cd/dvd RW disk , insert it into the pc.

step 5 - do this one by one - 
|- fdisk (NOTE - RUNNING FDISK MIGHT DESTROY DATA , CONTINUE WITH CAUTION)
|-- press "Y" and hit Enter on the keyboard (only if you have disk more than 512mb)
|--- press "1" and hit enter on keyboard
|---- again press "1" and hit enter on keyboard
|----- press "1" and hit enter on your keyboard (only if you want to give full size to the C: drive or else , press "N" and hit enter on your keyboard and manually resize partitions yourself)
|------ press "Esc" key on your keyboard and hit enter
|------- then restart your vm or the pc and do these - (before that prioritize the cd/dvd drive or the virtual iso on a vm to boot from it and do these)
|-------- format c: /s
|--------- press "Y" and hit enter on the keyboard (NOTE - THIS WILL ERASE ALL OF THE DATA)
|---------- now give the name of volume label and hit enter or just hit enter for no label
|----------- [your disk letter for the cd/dvd drive] with an ":"
|------------ cd WIN95
|------------- setup /is /iq /id /iv

step 6 - go through the setup! (also read the "WARNING" section just below this if you encounter errors related to them or post it on the issues page on GitHub if it's other things.)

WARNING - YOU MIGHT SEE THINGS WHILE BOOTING OR THE SECOND PART OF SETUP WHICH SAYS FILE NOT FOUND IF YOU ARE IN BOOT JUST PRESS ANY KEY UNTIL IT STARTS TO BOOT OR IF YOU ARE IN THE SECOND PART OF THE SETUP THEN PRESS ON SKIP FILE UNTIL IT PROCEEDS.

---------------------------------------------------------------------

if you still want to make it more small , then - (everything is optional here)

choose compact installation when it asks it.

do not select any of the adapters to analyze or installing the drivers might take up more space

when it prompts to install components , choose let me customize the list (or something else) and check out everything

when it prompts to make a starup disk , DON'T.

WARNING - IF IT SAYS FILE NOT FOUND IN THE FIRST SETUP PHASE , JUST CLICK "SKIP FILES"

WARNING - IF IT GIVES YOU SOME WAARNINGS AFTE WHEN BOOTING IN DESKTOP , JUST CLICK OK.

