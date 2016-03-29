# After-Effects-Scripting-Tools
This .jsxinc file includes basic and custom Javascript methods and functions that I think is missing in the Extend Script environment .

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
## This script includes : 
#### "Native" Javascript Methods
##### JSON
- JSON2 ( https://github.com/douglascrockford/JSON-js )
- Object.keys

##### Array
- indexOf
- min and max
- reduce

#### custom Javascript Methods
#### custom AE Methods
###### FolderItem
Method | Description | Returns
------ | ----------- | -----------
`_getAllItems` | Retreive all the items in a folder and his subfolder(s) | JSON with all the items in the folder. If the `_function` parameter is undefined, nothing is returned

###### PropertyGroup
Method | Description | Returns
------ | ----------- | -----------
`_removeKeys` | Delete all keyframes from the called *PropertyGroup* | -

###### Property
Method | Description | Returns
------ | ----------- | -----------
`_removeKeys` | Delete all keyframes from the called *Property* | -

###### FootageItem
Method | Description | Returns
------ | ----------- | -----------
`_createComp` | Create a comp based on the footage | Array containing the *CompItem* and the *Layer* [comp,layer]
