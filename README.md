Roll20 API Scripts
==================

This repository is the collection of all the community-contributed API scripts that are available for use on Roll20.

Contributing
============

If you want to help improve an existing API script, just clone this repository, make your changes, and submit a pull request. If you would like to contribute a new script for the community to use, just clone this repository and create a new folder with the name of the script which matches the name in your package.json file. Optionally you can add a help.txt file with any instructions you want to include as well as any other files you feel will be helpful to the end user. Once everything is in the new folder send a pull request. If you have any questions or aren't familiar with Github or git in general, feel free to drop us a line at team@roll20.net and we can help you get set up.

**Creating a package.json File**

When you are ready to submit your script for **public use**, create a `package.json` file in your script's folder (see the Cookbook folder for an example package.json file). The file has the following fields:

* `name`: The name of the API script (e.g. `Cookbook`)
* `version`: The version number of the API script (e.g. `12.1.3`)
* `description`: A short, less than 100 character, explination of the script and it's use.
* `authors`: A simple string telling who contributed toward the sheet (e.g. `Riley Dutton,Steve Koontz`)
* `roll20userid`: A simple string telling the Roll20 User ID's of the authors (e.g. `1` or `45672,145678`). Just used so we know who to credit internally, won't be shown publicly on the site.
* `scripts`: A list of the API scripts (e.g. `cookbook.js`) 
* `dependencies`: A list of other API scripts and API objects this set requires to function (e.g. `mykitchen.js`) 
* `conflicts`: A list of other API scripts this set is known to conflict with (e.g. `recipes.js`) 
* `license`: Roll20's API repository is working under a MIT license (e.g. `MIT`)

After we have reviewed your package and approve it, we will merge in your changes to the root directory which will make it available to everyone. If we reject your sheet, we will comment on your Github commit and let you know what changes need to be made before it can be accepted. 

**PLEASE VERIFY YOUR PACKAGE.JSON IS VALID JSON at http://jsonlint.com before you submit it!**

Update the Wiki
===============

After making any changes to a script or adding a new one, it is imortant to include those changes with the Roll20 wiki at (https://wiki.roll20.net/API:Script_Index).

Guidelines
==========

Here are a few guidelines that you should follow when contributing API scripts for the community:

**Be Clear and Concise**

Community API scripts should be built from the ground up with the intention of sharing with others. The script's name should be a good indicator of what the script does and how it should be used. A script named "MkLtObjMvr-Dst" is likely to confuse, where a script named "Light Switch" is descriptive, clear, and does a good job of hinting at it's intended use.

Try to use short and descriptive function and variable names. Problematic names like "x1", "fe2", and "xbqne" are practically meaningless. Names like "incrementorForMainLoopWhichSpansFromTenToTwenty" are verbose. Aim for variable and function names that are meaningful but simple, such as "card_val" or "limitStr".

**Make Your Script Accessible**

Please take every effort to format your code in a traditional manner and present the script in a legible state. Leaving comments on the intended use of functions and code blocks can be very useful to future contributors.

Near the top of your script should be a comment providing the script's name, version number, the last time it was updated, and a short breakdown of the scripts intended use. In the breakdown should be included the script's description, syntax, and configuration options. It is important to add configurable elements near the top of the script in an easily demarcated area with comments on how those elements can or should be customized. 

**Limit Your Script's Footprint**

Include namespaces for your functions and variables, to avoid potential conflicts with other authors. Placing your functions and variables inside a unique namespace to your script protects both it, the user, and other community scripts.

Do your best to limit what your script is manipulating at any given moment to achieve it's desired result. Add API "!" triggers to turn on and off your script's functionality. It is a safe practice to have your script disabled by default. Avoid functions that keep aggresive control and manipulation of objects whenever possible.

License
=======

All of the code of the API scripts in this repository is released under the MIT license (see LICENSE file for details). If you contribute a new script or help improve an existing script, you agree that your contribution is released under the MIT License as well.
