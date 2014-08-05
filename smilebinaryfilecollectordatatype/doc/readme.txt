smile binaryFile information collector datatype for eZ Publish 4.5
version 1 beta

Written by Smile Maroc,Copyright (C)
http://www.smile.ma/

@author:mojeb@smile.fr

What is smile binaryFile collector datatype?
--------------------------

allow you to use the binary File datatype as information collector.


License
-------

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; version 2 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.


Requirements
------------
- eZ Publish 4.5.0+
- jquery 1.8


Tested with
-----------
4.5.0


Installation
------------

1. Copy the extension to the /extension folder, so that 
you have /extension/smilebinaryfilecollectordatatype/* structure.

2. Enable the extension (either via administration panel or directly with 
settings files):
[ExtensionSettings]
ActiveExtensions[]=smilebinaryfilecollectordatatype

3. Configure smilebinaryfile.ini.append.php file according to your preferences.

4.add or uncomment this line below in config.php file :

define( 'EZP_AUTOLOAD_ALLOW_KERNEL_OVERRIDE', true );

5. this extension override the kernel class kernel/classes/ezinformationcollection.php by

extension/smilebinaryfilecollectordatatype/kernel/classes/ezinformationcollection.php 

to use the override class you must be generate the autoloads with -o option :

php bin/php/ezpgenerateautoloads.php -o 


6. Apply the smilecollectionbinaryfile table to your database with the included sql file:
<eZP root>/extension/smilebinaryfilecollectordatatype/sql/mysql/sql.sql
Using either phpmyadmin (easiest) or shell/console commands.


7. Now you can use smilebinaryFile datatype as information collector like any other datatype when editing classes.

8. Clear cache.

