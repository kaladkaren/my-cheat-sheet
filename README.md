# my-cheat-sheet
"If you can't solve it, just google it."

## Table of contents
1. **PHP**
    + [Saving Session](#saving-session)
    + 
2. **XAMPP**
    + [Get PHP Version](#get-php-version)
    + [Adding MCrypt Extension](#adding-mcrypt-extension)
    
### Get PHP Version
- Open command prompt.
- Locate directory using cd C:/Xampp/php.
- Type command php -v.
- You will get your php version details.

### Adding MCrypt Extension
Step 1: Open XAMPP click on the Config button and open php.ini in your editor.

Step 2: Search for the following phrase in the php.ini file.
        _;extension=php_mcrypt.dll_
        
Step 3: If not found, you can follow the below steps to install mcrypt.

#### Installing and Enabling MCrypt extension in XAMPP
Step 1: Download the suitable version of mcrypt package for your system using the official website. https://pecl.php.net/package/mcrypt/1.0.3/windows

Step 2: A zip file will be downloaded. Now extract the zip file and then paste the ” php_mcrypt.dll ” file in the following directory.
        _C:\xampp\php\ext_
        
Step 3: Open XAMPP, and click on the Config button then open php.ini in your editor.

Step 4: Paste the following phrase in the php.ini file like as shown in the picture.
        _extension=
        
Step 5: Now restart the XAMPP server to see the effects. You can also go to the PHPInfo(by clicking on admin in XAMPP) page to verify the installation.
