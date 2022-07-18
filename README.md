# certificate-password-recovery

How to use the Utility
Open the EXE found in CertificatePasswordRecovery\CertificatePasswordRecovery\bin\Release
1-MainRecoveryUI.png
While it looks like there are a lot of options, they are all explained below

Configure the Settings:
Max Generated Characters specifies how many characters you want to generate. It will go from 1 character up to (and including) the maximum specified here
 
Starting String lets you decide where you want to start your generated password. For example: If you enter aaa in this field then your sequence will go aaa,aab,aac,etc...
 
Prefix String is useful in cases where you remember the first few characters of your password. No need to waste time 'guessing' those if you already know them. For example if you know that your password starts with pass, enter 'pass' in the prefix box.
 
Suffix String is helpful when you remember the last few characters of your password. 
 
In the Symbol Sequence box you can specify a comma-separated list of characters you want to be present in the password search. It can be arbitrarily ordered.

Note: For reliable results, leave the space at the beginning of the symbol sequence!
Note 2: The more characters you can remove from this list, the quicker your search will go.

Path To Cert lets you pick the keystore or certificate you want to use when guessing passwords
 
Path to Log File lets you pick the path to the logfile where attempts are logged

Note: The utility will crash if given a non-existant folder path. It will create the txt file automatically, but not the folder structure up to it.
 
Log Level lets you pick how to log. Explanation of settings:
Off will not log anything. Be careful with this setting: It means the only notification you'll receive is a pop-up dialog when the password is found. Nothing is written out to disk
 
Success Only will log the start of the process, then write the password out to the file when it is found. All non-valid passwords are ignored
 
Every 10,000 + Success will log every 10,000th password along with the Succesful password. This is useful if you want to track the progess of the password guessing.

Note: Don't open the file directly. Instead, copy it then open. Otherwise the file could be locked when the Utility tries to write-out
 
Everything will log every password attempt to the log file. This is the Slowest setting as writing to disk is fairly slow. Use this option if you want to find out what password combinations are being tested.
 
The Help / about link will take you to this page
 



 
Notes about the Recovery tool:
It Will not find spaces at the beginning or end of a password unless manually entered in the prefix / suffix boxes
 
To specify a comma as a sequence symbol you must enter 'comma' (without the quote marks). This is becuase I split the string on comma and need another way to represent that character
 
If characters are entered in the 'starting string' box that are not present in the symbol sequence, you will be alerted. This could negatively affect the pasword search
 
A space is the first character in the default sequence. This allows the password cracker to easily handle passwords that are up to the max length, while not starting at the max length
Note: For best results it is highly recommended to leave the space as the first character in the sequence!
