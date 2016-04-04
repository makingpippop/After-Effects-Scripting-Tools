# After-Effects-Scripting-Tools
This .jsxinc file includes basic and custom Javascript methods and functions that I think is missing in the Extend Script environment.

I will update this file as I create new methods, so be sure to check regularly for updates !
Feel free to add this script in yours, and contact me if you wanna add some of your useful methods.

## Install
Import the file into your current script.
```javascript
var currentScript = new File($.fileName);
var assetsFolder = new Folder(currentScript.parent.absoluteURI.toString()+"/assets");
try {
	$.evalFile(new File(assetsFolder.toString()+"/js/js_tools.jsxinc"));
} catch(e) {
	//This is one of two things: either there is an error
   //in the file or the file does not exist
   alert("Error while getting one of the asset for the script");
}
```

You can also use the *#include* at the top of your script

    #include "path-to-this-script/js_tools.jsxinc"

## This script includes :
#### "Native" Javascript Methods
##### JSON
- JSON2 ( https://github.com/douglascrockford/JSON-js )
- Object.keys

##### Array
- indexOf
- min
- max
- reduce
- fill ( https://gist.github.com/addyosmani/d5648c89420eb333904c.js )

---
#### Custom Javascript Methods

>**Math**

Method | Description | Returns
------ | ----------- | -----------
`Math.degrees` | Converts from radians to degrees | Float
`Math.radians` | Converts from degrees to radians | Float


>**Array**

Method | Description | Returns
------ | ----------- | -----------
`_combine` | add, subtract, multiply or divide the content of 2 arrays | Array

---
#### Custom AE Methods

>**FolderItem**

Method | Description | Returns
------ | ----------- | -----------
`_getAllItems` | Retreive all the items in a folder and his subfolder(s) | JSON with all the items in the folder. If the `_function` parameter is undefined, nothing is returned

>**MaskPropertyGroup**

Method | Description | Returns
------ | ----------- | -----------
`_removeKeys` | Delete all keyframes from the called *MaskPropertyGroup* | -

>**PropertyGroup**

Method | Description | Returns
------ | ----------- | -----------
`_removeKeys` | Delete all keyframes from the called *PropertyGroup* | -

>**Property**

Method | Description | Returns
------ | ----------- | -----------
`_removeKeys` | Delete all keyframes from the called *Property* | -

>**FootageItem**

Method | Description | Returns
------ | ----------- | -----------
`_createComp` | Create a comp based on the footage | Array containing the *CompItem* and the *Layer* [comp,layer]
