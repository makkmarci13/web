# flags
<h4 class="fw-light">Highly-specific options that don't deserve their own configuration option.</h4><br/>

### **What are flags?**
Flags allow for enabling/disabling possibly advanced features that don't have their own option in your [conf.yml](?page=documentation/confyml) file. Multiple flags must be seperated with comma's.

<br/>

### **Flags**

##### Feature-specifc flags
`ignorePlaceholders`\
Skip applying placeholders. This improves installation speed for extensions with a lot of files, but is generally not recommended.

`forceLegacyPlaceholders` <tag type="new" content="beta-A428"/></tag>\
Force Blueprint to apply legacy placeholders instead of the new ones on extensions with a higher target version than alpha or indev.

<br/>

##### Advanced flags
`hasInstallScript`\
Right before the installation completes, extensions with this flag will be able to run a shell script. This script must be called "install.sh" and be in the root of your data directory.

`hasRemovalScript`\
Right before starting the extension removal process, extensions with this flag will be able to run a shell script to undo some changes Blueprint isn't able to. This script must be called "remove.sh" and be in the root of your data directory.

`hasExportScript`\
In the middle of the export process, extensions with this flag will be able to run a shell script to automate additional changes for distribution. This script must be called "export.sh" and be in the root of your data directory.

<br/>

##### Developer flags
`developerIgnoreInstallScript`\
Ignore the custom extension installation script when installing your extension through developer commands.

`developerIgnoreRebuild`\
Skip rebuilding panel assets when installing your extension through developer commands.

`developerForceMigrate` <tag type="new" content="beta-A428"/></tag>\
Forcefully migrate the database non-interactively when installing your extension through developer commands.

`developerKeepApplicationCache` <tag type="new" content="beta-CB38"/></tag>\
Prevents Blueprint from flushing the application's cache when building extensions through developer commands.