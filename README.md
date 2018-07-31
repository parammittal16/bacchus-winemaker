# bacchus-winemaker
Presets for the Bacchus utility

## Contributing

Please read the JSON section below for an explanation of what all of the fields mean and how they should be populated. If you choose to contribute I ask that you please also post your findings to the WineHQ AppDB. Not everyone is aware of or wants to use Bacchus, and they shouldn't be required to in order to benefit. That being said, please actually test your presets. Do not just copy something from WineHQ and assume it will work as intended.

Please comply with all applicable laws when making contributions. Your contributions should not be targeted towards pirated copies of software or explicitly enable some other criminal activity. For example, BitTorrent clients are fine since they have many legitimate uses, however a modified, illicit copy of Photoshop would not be permitted.

Please keep all discussions and commit messages limited to what is relevant to the project.

## JSON

### Name
The name that will be used for the prefix. This should be the name of the application.

### EXE
The name of the executable to run in order to start the application.

### Path
The path to the directory containing the executable. This is likely somewhere in Program Files or Program Files (x86). We assume the user selected the default options in the installer.

### Type
The type of install process. There are three options:
1. setup - This is used when the user has to specify a setup or installer executable to run.
2. dir - This is used when the application is already contained in a directory and that directory simply needs to be copied to the prefix.
3. single - This is used when the application is a self-contained executable that needs to be copied to the prefix.

### Arch
The required architecture. This can be either win32 or win64. We may enforce a requirement that one be selected over the other if there is no difference in order to better support systems that lack multiarch. I am not personally familiar enough with multiarch to say one way or the other at this time. If you have experience please let me know!

### Win
The required Windows version. This will likely be either winxp or win7.

### Locale
The required locale. Please leave this blank if there are no locale requirements.

### Winetricks
A space delimited list of packages required via winetricks.

### Version
The version of the software. This field does not serve any functional purpose but is included for troubleshooting purposes.
