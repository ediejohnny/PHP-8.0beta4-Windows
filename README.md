![Image of PHP](https://www.php.net/images/logos/php-logo.svg)

# PHP-8.0beta4-Windows
PHP 8.0 Beta 4 compiled with Visual Studio C++ 2019 using Windows 10 Education (x64)

# Configured options:
--enable-snapshot-build

I used this option because it enables everything it can (all extensions, etc).

# Compile by yourself
Before start compiling PHP, you need to install Visual Studio C++ 2019 and Windows 10 SDK (look at the Utils folder).

* __Step 1:__ create a folder in your C: called "php8" or whatever name you want, but I'll consider "php8" in this tutorial;

* __Step 2:__ open the "Developer PowerShell for VS 2019", usually it's located at Start -> Visual Studio 2019;

* __Step 3:__ extract the PHP SDK (look at Utils folder) inside the C:\php8;

* __Step 4:__ into the Developer PowerShell, navigate to that extracted folder of PHP SDK, if you done it right, it'll be located at C:\php8\php-sdk-binary-tools-master;

* __Step 5:__ navigate to the bin folder, so you are at the C:\php8\php-sdk-binary-tools-master\bin now;

* __Step 6:__ execute the command ".\phpsdk_setvars.bat";

* __Step 7:__ go back one folder using "cd .." command;

* __Step 8:__ execute the command ".\phpsdk-vs16-x86.bat" or ".\phpsdk-vs16-x64.bat";

* __Step 9:__ now you'll be on a different command line. Navigate to the folder where you have PHP source files, I recommend you extract the source to the C:\php8 folder, so probably you have the sources at "C:\php8\php-8.0.0beta4". If you want to use my "Source" folder, put it at the C:\php8 folder and you can navigate to "C:\php8\Source";

__NOTE__: this new command line will not show what folder you are, just a dollar sign ($), so if you don't know what folder you are, execute the "dir" command.

  * __Step 9.1__: you are now using the PHP-SDK console and you can execute all of its command everywhere, so it's time to update your external libs. It's necessary to build Apache DLL, download missing extensions and update everything to the last version. Execute the command "phpsdk_deps -u".

* __Step 10__: execute the command "buildconf";

* __Step 11__: execute the command "configure --help" to see all the options you can configure your PHP;

* __Step 12__: execute the command "configure";

* __Step 13__: execute the command "nmake";

...and you're done. Your compiled version of PHP will be at the folder "Release_TS" inside the PHP sources folder if you choose x86 at the Step 8. If you choose x64, the binaries will be at the "x64" folder instead.
