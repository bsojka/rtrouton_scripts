This Absolute Manage custom information item checks to see if a Mac is running 10.7 or higher. If the Mac in question is running 10.7 or higher, the EA reports on whether or not the Mac's boot volume is encrypted with Apple's FileVault 2 encryption and gives the encryption or decryption status. 

See "Absolute_Manage_Custom_Info_Item_Setup.png" for a screenshot of how the Custom Information Item should be configured.

Credit to Patrick Gallagher of Emory University for adapting my FileVault 2 status script as this Absolute Manage custom information item.

Output produced by this script:

This custom information item is designed to check the FileVault 2 encryption status of Macs running Mac OS X 10.7.x and higher.

It first checks to make sure the version of Mac OS X begins with "10". If it is not, the following message is displayed without quotes:

"Unknown Version Of Mac OS X"

Next, it checks to see if the OS on the Mac is 10.7 or higher. If it is not, the following message is displayed without quotes:

"FileVault 2 Encryption Not Available For This Version Of Mac OS X"

If the Mac is running 10.7 or higher, but the boot volume is not a CoreStorage volume, the following message is displayed without quotes:

"FileVault 2 Encryption Not Enabled"


If the Mac is running 10.7 or higher and the boot volume is a CoreStorage volume, the Extension Attribute checks to see if the machine is encrypted, encrypting, or decrypting.

If not encrypted, the following message is displayed without quotes:

"FileVault 2 Encryption Not Enabled"

If encrypted, the following message is displayed without quotes:

"FileVault 2 Encryption Complete"

If encrypting, the following message is displayed without quotes:

"FileVault 2 Encryption Proceeding." 

How much has been encrypted of of the total amount of space is also displayed. 
If the amount of encryption is for some reason not known, the following message
is displayed without quotes: 

"FileVault 2 Encryption Status Unknown. Please check."

If decrypting, the following message is displayed without quotes:

"FileVault 2 Decryption Proceeding" 

How much has been decrypted of of the total amount of space is also displayed

If fully decrypted, the following message is displayed without quotes:

"FileVault 2 Decryption Complete"