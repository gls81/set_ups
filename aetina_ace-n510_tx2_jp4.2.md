## Guide for installing the Nvidia JetPack 4.2 on the Aetina Ace-n510 with Jetson TX2. ##

Using Nvidia SDK Manager choose TX2 and Jetpack 4.2.

**Step 1 - Install L4T and SDK packages**
Use the [Nvidia SDK Manager](https://developer.nvidia.com/nvsdk-manager) to install the update. In the SDK Manager select  ~/$USER/Downloads/Nvidia as default.
Once the files have downloaded SDK Manager creates the OS Image in ~/Nvidia/ 


**Step 1a - Only Required if Using the Aetina N510 TX-2**
It is imprtant that you do connect TX2 and coomence flashing until the specific patches downloaded from Aetina have been copied over the corresponding files in the OS Image.
Once copying is completed put the TX2 into recovery mode and allow the SDK manager to flash the TX2 and then install the revelvant software packages as prompted by the SDK Manager.

**Step 2 - Patch the Kernel**
Clone the scripts from [this Github repo](https://github.com/Tengyun-Mo/buildLibrealsense2TX2). Note that this installs Realsense SDK 2.20.0. At the time of writing 2.28.0 is the most current version of the SDK and is the version I installed on our TX-2. To instal your desired version edit the LIBREALSENSE_VERSION parameter in both buildPatchedKernel.sh and installLibrealsense.sh. Then simply follow the guide provided by the author on GitHub.
