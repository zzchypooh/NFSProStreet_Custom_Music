This project is the simplest way that I currently know to add custom music files to NFS Prostreet to replace the in game files 
hope you all enjoy
be sure to bring any issues you find to me either by email or by the issues tab
I have more testing to do regarding interactive race moments


:: Step 1: Decoding

copy ffmpg from \Pro Street Custom Music\Workspace Folder\Tools to \Pro Street Custom Music\Music Goes Here folder

Open game directory

Open SOUND folder

Open PFDATA folder and look for ps_music.mpf and ps_music.mus

copy to \Pro Street Custom Music\Workspace Folder

Open Workspace Folder and run Open_sesame.bat to decompile the .mpf file into a file map(pf_music_decomp.txt) and extract its constituant .sns(audio) and .snr(header) files

:: 64-bit MPFmaster in the folder by default, swap for 32-bit files if necessary

:: after reading .sns and .snr files cmd will show a long string of failure to open file, ignore this. Encoding will begin soon after

.sns files are also automatically turned into .wav files and placed into respective folder

:: they are mostly unimportant, but check to see that they have data and can play music


:: Step 2: Converting

at this point there should be 2,683 of each file type

.wav/.sns files 1-37 are the files that contain the EATrax songs

now find 1-37 songs you would like to add to the game to replace the existing songs in

ensure they are in .mp3 or .wav format

:: they will be turned into .mp3 files either way 

place these songs in the "Music Goes Here" folder and run the Renamer and Converter.bat

::do not subfolder the songs, place them directly into the "Music Goes Here" folder

a folder will have been made with all your songs turned into .sns files

take these files and overwrite the .sns files in \Pro Street Custom Music\Workspace Folder\samples

now go to the Workspace Folder and run Close_sesame.bat

you will see new .mpf and .mus files to copy to the game directory's PFDATA folder

so long as your .mus file is smaller then 300MB it will run and music will play on launch



::Step 3: Integration

now copy the contents of the CustomJukebox folder into the main game directory

open C:\Program Files (x86)\Electronic Arts\Need for Speed ProStreet\CustomPlaylists

you will find StockPlaylist.ini

open this then open the game

navigate to the EATrax jukebox and play each song to make sure they all sound fine

::make sure audio detail is set to high in the game settings

each track and its information will have to be manually changed with the .ini file otherwise it will show the names of the tracks you replaced
otherwise, you now have custom music in Pro Street

Enjoy :P


:: MPFmaster and CustomJukebox by xan1242 https://github.com/xan1242/NFS_CustomJukebox https://github.com/xan1242/MPFmaster
:: EALayer3 by driftyz700 https://github.com/driftyz700/ealayer3-nfsw
:: vgmstream https://github.com/vgmstream/vgmstream
:: ffmpeg https://ffmpeg.org/download.html#build-windows
