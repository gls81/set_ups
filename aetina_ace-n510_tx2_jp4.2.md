Guide for installing the Nvidia JetPack 4.2 on the Aetina Ace-n510 with Jetson TX2.

Using Nvidia SDK Manager choose TX2 and Jetpack 4.2
Continue, initally SDK Maanger will download all the relevant files and store these in ~/$USER/Downloads/Nvidia as default.
Once the files have downloaded SDK Manager creates the OS Image in ~/Nvidia/ 
It is imprtant that you do connect TX2 and coomence flashing until the specific patches downloaded from Aetina have been copied over the corresponding files in the OS Image.
Once copying is completed put the TX2 into recovery mode and allow the SDK manager to flash the TX2 and then install the revelvant software packages as prompted by the SDK Manager.
