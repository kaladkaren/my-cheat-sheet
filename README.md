# my-cheat-sheet
"If you can't solve it, just google it."

## Table of contents
1. **PHP**
    + [Saving Session](#saving-session)
    + 
2. **XAMPP**
    + [Get PHP Version](#get-php-version)
    + [Adding MCrypt Extension](#adding-mcrypt-extension)
3. SSL
    + [Get SSL Private Key from pfx file](#get-SSL-Private-Key-from-pfx-file)
    
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

Step 4: Paste the following phrase in the php.ini file.

        _extension=mcrypt_
        
Step 5: Now restart the XAMPP server to see the effects. You can also go to the PHPInfo(by clicking on admin in XAMPP) page to verify the installation.


### Get SSL Private Key from pfx file
NOTE: Open command line first and go to directory where your pfx file located.

1. Take the file you exported (e.g. certname.pfx) and copy it to a system where you have OpenSSL installed. Note: the *.pfx file is in PKCS#12 format and includes both the certificate and the private key.
2. Run the following command to export the private key: 

    _openssl pkcs12 -in certname.pfx -nocerts -out key.pem -nodes_

3. Run the following command to export the certificate: 

    _openssl pkcs12 -in certname.pfx -nokeys -out cert.pem_
    
4. Run the following command to remove the passphrase from the private key: openssl rsa -in key.pem -out server.key 

If cant export the private key, visit this site to enable then do the 1 to 4 steps above:
https://support.globalsign.com/digital-certificates/digital-certificate-installation/personalsign-installation-step-2-locate-install-your-certificate

