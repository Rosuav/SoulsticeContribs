Random notes. How to hack Soulstice to not need FMOD:

1. Open Soulstice.uproject in SciTE and change "true" to "false" in FMOD's Enabled state
2. Load up Unreal Editor and look for blueprint compilation errors. TODO: Enumerate them.
   - Content/Characters/EvaCharacterBP - walking animation(?)
   - Content/Maps/SoulsticeSchool and _2: Open Level Blueprint, open/close bedroom door
   - Village ambience?
   - Fountain?


Alternatively, download "FMOD Studio for Unreal Engine 4 (4.11)" from
http://www.fmod.org/download/ and unzip it into Plugins/ in the project dir.
(Plugins might not exist. Create it.)
Then download "FMOD Studio Programmer’s API and Low Level Programmer API" from
the same page. Maybe.

cd ~/Documents/Unreal\ Projects/
mkdir Soulstice
cd Soulstice
unzip ......stuff.from.google.drive.zip
mkdir Plugins
cd Plugins
unzip ~/Downloads/fmodstudio10803ue4.11linux.zip

Open up the project, tell Unreal not to bother converting (if prompted).
Rebuild the FMOD stuff. (Compilation work.)

To make packaging work properly:

1. File, Package Project, Packaging Settings
2. Build Configuration: Shipping [may or may not be important]
3. Packaging section, expand "Advanced"
4. Additional Non-Asset Directories to Package: Add "FMOD"

Then package, saving to ~/tmp/Soulstice

To run the resulting file:

~/tmp/Soulstice/LinuxNoEditor/Soulstice/Binaries/Linux$ ./Soulstice-Linux-Shipping
