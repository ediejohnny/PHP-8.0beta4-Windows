# PHP-8.0beta4-Windows
PHP 8.0 Beta 4 compiled with Visual Studio C++ 2019 using Windows 10 Education (x64)

Configured options:
--enable-pdo --with-pdo-mysql --with-pdo-pgsql --with-curl --enable-apache2-4handler

# Compile by yourself
Before start compiling PHP, you need to install Visual Studio C++ 2019 and Windows 10 SDK (look at the Utils folder).

Step 1: create a folder in your C: called "php8" or whatever name you want, but I'll consider "php8" in this tutorial;
Step 2: open the "Developer PowerShell for VS 2019", usually it's located at Start -> Visual Studio 2019;
Step 3: extract the PHP SDK (look at Utils folder) inside the C:\php8;
Step 4: into the Developer PowerShell, navigate to that extracted folder of PHP SDK, if you done it right, it'll be located at C:\php8\php-sdk-binary-tools-master;
Step 5: navigate to the bin folder, so you are at the C:\php8\php-sdk-binary-tools-master\bin now;
Step 6: execute the command ".\phpsdk_setvars.bat";
Step 7: go back one folder using "cd .." command;
Step 8: execute the command ".\phpsdk-vs16-x86.bat" or ".\phpsdk-vs16-x64.bat";
Step 9: now you'll be on a different command line. Navigate to the folder where you have PHP source files, I recommend you extract the source to the C:\php8 folder, so probably you have the sources at "C:\php8\php-8.0.0beta4". If you want to use my "Source" folder, put it at the C:\php8 folder and you can navigate to "C:\php8\Source";

!NOTE: this new command line will not show what folder you are, so just execute the command "dir" to know you are at the correct path.

Step 10: execute the command "buildconf";
Step 11: execute the command "configure --help" to see all the options you can configure your PHP;
Step 12: execute the command "configure";
Step 13: execute the command "nmake";

...and you're done. Your compiled version of PHP will be at the folder "Release_TS" inside the PHP sources folder if you choose x86 at the Step 8. If you choose x64, the binaries will be at the "x64" folder instead.
