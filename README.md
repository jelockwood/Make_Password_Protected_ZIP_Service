# Make_Password_Protected_ZIP_Service
Make Password Protected ZIP

This is an Apple Automator Service. It executes an AppleScript which presents the user a series of dialog boxes which take the user through the process of creating a password protected ZIP file. The script calls the built-in zip tool but unlike the built-in Apple 'Compress' service this script gives the ability to set a password protection on the resulting Zip file.

This was based on a previous scrip I found in a user forum but has been heavily improved and many issues fixed. This version supports ziping a single file, or an entire folder of files.

Under newer versions of macOS you will likely have to give the automator service permission to work i.e. permission to access files and folders.

To use it, you install it as an automator service as normal. It will then show up in the Finder's services sub-menu. This is accessed by right-clicking on the file or folder you wish to make a password protected ZIP of and then selecting the service from the sub-menu.

<img width="639" alt="Screenshot 2023-11-29 at 11 49 47" src="https://github.com/jelockwood/Make_Password_Protected_ZIP_Service/assets/4300786/9e0de17e-5560-4196-b226-4fed6dc164a2">


The original version of this script automatically excluded any of the infamous ```.DS_Store``` files it found. The latest version of this script now also automatically excludes any files found beginning with ~$ i.e. ~$* or as a 'real' example ```~$My Spreadsheet.xlsx```

It seems Microsoft Office creates invisible temporary files beginning with these characters. Being invisible when you look in the source directory you do not see them, however after the directory is converted to a ZIP file and later expanded back to a directory, these invisible files become visible and **do** confuse users into thinking they are 'real' files.
