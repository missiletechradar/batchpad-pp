ThatGuyVR's original script: https://github.com/Thatguyvr15/Batchpad/releases/tag/Batchpad

**In case you can't run batch files without running them as admin after installing this, or vbs files (which is the case because of a program bug, run these commands in CMD as admin:*

fix bat and cmd file not running:

reg add "HKEY_CLASSES_ROOT\batfile\shell\open\command" /ve /t REG_EXPAND_SZ /d "\"%%SystemRoot%%\System32\cmd.exe\" /c \"%%1\" %%*" /f

reg add "HKEY_CLASSES_ROOT\batfile\shell\runas\command" /ve /t REG_EXPAND_SZ /d "\"%%SystemRoot%%\System32\cmd.exe\" /c \"%%1\" %%*" /f

reg add "HKEY_CLASSES_ROOT\cmdfile\shell\open\command" /ve /t REG_EXPAND_SZ /d "\"%%SystemRoot%%\System32\cmd.exe\" /c \"%%1\" %%*" /f

reg add "HKEY_CLASSES_ROOT\cmdfile\shell\runas\command" /ve /t REG_EXPAND_SZ /d "\"%%SystemRoot%%\System32\cmd.exe\" /c \"%%1\" %%*" /f

fix vbs not running:

reg add "HKCR\vbsfile\Shell\Open\Command" /ve /d "\"%SystemRoot%\System32\WScript.exe\" \"%1\" %*" /f & reg add "HKCR\.vbs" /ve /d "vbsfile" /f

Because of an instalation bug in Batchpad++, this issue can be triggered at the registry level, and this simple command can fix it.

# This is a fork of ThatGuyVR's Batchpad text editor. This program includes the following features:

 - Ability to change color scheme
 - Editing specific lines
 - List lines with numbers from saved document or unsaved {temp.txt] file
 - Improved user interface with tabs and more user-friendly

 - Unique commands and help page ($hl, $cl) that prevent the user from 
   accidentally triggering them while typing.

 - Ability to edit existing documents directly
 - Context menu option to edit documents directly

This screenshot shows how Batchpad++'s user interface looks like with the default color scheme on the help page:

<img width="987" height="516" alt="image" src="https://github.com/user-attachments/assets/68b7fa75-32e2-4501-8ce0-df32cc67effa" />

**Note: The commands and syntax system were changed from $edit to #edit (example). This is because the dollar sign can interfere with bash or powershell syntax**

While editing a new document:

<img width="986" height="522" alt="image" src="https://github.com/user-attachments/assets/288b168c-5669-4af7-b924-d4f7cb3b887a" />

This is the Batchpad++ setup wizard, which installs the software but also allows you to make modifications if you change your mind regarding certain things, or uninstall the software altogether.

<img width="628" height="628" alt="image" src="https://github.com/user-attachments/assets/b062380c-da87-4ab1-a8c0-2a35392aab54" />

Example of regular document editing:

<img width="974" height="366" alt="image" src="https://github.com/user-attachments/assets/4137dd8f-e04a-485a-896e-1dfd63b4df4c" />

**Line editing**:

Before editing line 2:
<img width="993" height="520" alt="image" src="https://github.com/user-attachments/assets/af7e00ed-aa76-45a1-b359-d6c5e790cc23" />

After editing line 2:

<img width="1330" height="407" alt="image" src="https://github.com/user-attachments/assets/c87db3b9-16d5-49a2-b523-e6acada56fce" />

Usage:

- Download the batchpad++ zip file  extract it and run [setup.exe]. Follow the on-screen instructions to finish installation properly.
- After the program has been installed, there will be a shortcut included on your desktop. Double click it to open the text editor and start editing documents.
- A context menu option for editing plaintext-style files has also been included, such as .txt, .vbs, .bat or .cmd files.
- Type $hl and you will get instructions on commands and how to use the software properly.

**The source code is included in the same zip file as the software release itself**
