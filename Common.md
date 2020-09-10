## Functions

<dl>
<dt><a href="#CommonIsNumeric">CommonIsNumeric(n)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a variable is a number</p>
</dd>
<dt><a href="#CommonGetFormatDate">CommonGetFormatDate()</a> ⇒ <code>string</code></dt>
<dd><p>Gets the current time as a string</p>
</dd>
<dt><a href="#CommonDetectMobile">CommonDetectMobile()</a> ⇒ <code>boolean</code></dt>
<dd><p>Detects if the user is on a mobile browser</p>
</dd>
<dt><a href="#CommonGetBrowser">CommonGetBrowser()</a> ⇒ <code>Object</code></dt>
<dd><p>Gets the current browser name and version</p>
</dd>
<dt><a href="#CommonParseCSV">CommonParseCSV(str)</a> ⇒ <code>Array.&lt;Array.&lt;string&gt;&gt;</code></dt>
<dd><p>Parse a CSV file content into an array</p>
</dd>
<dt><a href="#CommonReadCSV">CommonReadCSV(Array, Path, Screen, File)</a> ⇒ <code>void</code></dt>
<dd><p>Read a CSV file from cache, or fetch it from the server</p>
</dd>
<dt><a href="#CommonGet">CommonGet(Path, Callback)</a> ⇒ <code>void</code></dt>
<dd><p>AJAX utility to get a file and return its content</p>
</dd>
<dt><a href="#CommonClick">CommonClick()</a> ⇒ <code>void</code></dt>
<dd><p>Catches the clicks on the main screen and forwards it to the current screen click function if it exists, otherwise it sends it to the dialog click function</p>
</dd>
<dt><a href="#CommonKeyDown">CommonKeyDown()</a> ⇒ <code>void</code></dt>
<dd><p>Catches key presses on the main screen and forwards it to the current screen key down function if it exists, otherwise it sends it to the dialog key down function</p>
</dd>
<dt><a href="#CommonDynamicFunction">CommonDynamicFunction(FunctionName)</a> ⇒ <code>void</code></dt>
<dd><p>Calls a basic dynamic function if it exists, for complex functions, use: CommonDynamicFunctionParams</p>
</dd>
<dt><a href="#CommonDynamicFunctionParams">CommonDynamicFunctionParams(FunctionName)</a> ⇒ <code>*</code></dt>
<dd><p>Calls a dynamic function with parameters (if it exists), also allow ! in front to reverse the result. The dynamic function is the provided function name in the dialog option object and it is prefixed by the current screen.</p>
</dd>
<dt><a href="#CommonCallFunctionByName">CommonCallFunctionByName(FunctionName, [...args])</a></dt>
<dd><p>Calls a named global function with the passed in arguments, if the named function exists. Differs from
 CommonDynamicFunctionParams in that arguments are not parsed from the passed in FunctionName string, but
 passed directly into the function call, allowing for more complex JS objects to be passed in. This
 function will not log to console if the provided function name does not exist as a global function.</p>
</dd>
<dt><a href="#CommonSetScreen">CommonSetScreen(NewModule, NewScreen)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the current screen and calls the loading script if needed</p>
</dd>
<dt><a href="#CommonTime">CommonTime()</a> ⇒ <code>number</code></dt>
<dd><p>Gets the current time in ms</p>
</dd>
<dt><a href="#CommonIsColor">CommonIsColor(Value)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a given value is a valid HEX color code</p>
</dd>
<dt><a href="#CommonRandomItemFromList">CommonRandomItemFromList(ItemPrevious, ItemList)</a> ⇒ <code>*</code></dt>
<dd><p>Get a random item from a list while making sure not to pick the previous one.</p>
</dd>
<dt><a href="#CommonConvertStringToArray">CommonConvertStringToArray(s)</a> ⇒ <code>Array.&lt;number&gt;</code></dt>
<dd><p>Converts a string of numbers split by commas to an array, sanitizes the array by removing all NaN or undefined elements.</p>
</dd>
<dt><a href="#CommonConvertArrayToString">CommonConvertArrayToString(Arr)</a> ⇒ <code>string</code></dt>
<dd><p>Converts an array to a string separated by commas (equivalent of .join(&quot;,&quot;))</p>
</dd>
</dl>

<a name="CommonIsNumeric"></a>

## CommonIsNumeric(n) ⇒ <code>boolean</code>
Checks if a variable is a number

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the variable is a finite number  

| Param | Type | Description |
| --- | --- | --- |
| n | <code>\*</code> | Variable to check for |

<a name="CommonGetFormatDate"></a>

## CommonGetFormatDate() ⇒ <code>string</code>
Gets the current time as a string

**Kind**: global function  
**Returns**: <code>string</code> - - Returns the current date and time in a yyyy-mm-dd hh:mm:ss format  
<a name="CommonDetectMobile"></a>

## CommonDetectMobile() ⇒ <code>boolean</code>
Detects if the user is on a mobile browser

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the user is on a mobile browser  
<a name="CommonGetBrowser"></a>

## CommonGetBrowser() ⇒ <code>Object</code>
Gets the current browser name and version

**Kind**: global function  
**Returns**: <code>Object</code> - - Browser info  
<a name="CommonParseCSV"></a>

## CommonParseCSV(str) ⇒ <code>Array.&lt;Array.&lt;string&gt;&gt;</code>
Parse a CSV file content into an array

**Kind**: global function  
**Returns**: <code>Array.&lt;Array.&lt;string&gt;&gt;</code> - Array representing each line of the parsed content, each line itself is split by commands and stored within an array.  

| Param | Type | Description |
| --- | --- | --- |
| str | <code>string</code> | Content of the CSV |

<a name="CommonReadCSV"></a>

## CommonReadCSV(Array, Path, Screen, File) ⇒ <code>void</code>
Read a CSV file from cache, or fetch it from the server

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Array | <code>string</code> | Name of where the cached text is stored |
| Path | <code>string</code> | Path/Group in which the screen is located |
| Screen | <code>string</code> | Screen for which the file is for |
| File | <code>string</code> | Name of the file to get |

<a name="CommonGet"></a>

## CommonGet(Path, Callback) ⇒ <code>void</code>
AJAX utility to get a file and return its content

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Path | <code>string</code> | Path of the resource to request |
| Callback | <code>function</code> | Callback to execute once the resource is received |

<a name="CommonClick"></a>

## CommonClick() ⇒ <code>void</code>
Catches the clicks on the main screen and forwards it to the current screen click function if it exists, otherwise it sends it to the dialog click function

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="CommonKeyDown"></a>

## CommonKeyDown() ⇒ <code>void</code>
Catches key presses on the main screen and forwards it to the current screen key down function if it exists, otherwise it sends it to the dialog key down function

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="CommonDynamicFunction"></a>

## CommonDynamicFunction(FunctionName) ⇒ <code>void</code>
Calls a basic dynamic function if it exists, for complex functions, use: CommonDynamicFunctionParams

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| FunctionName | <code>string</code> | Name of the function to call |

<a name="CommonDynamicFunctionParams"></a>

## CommonDynamicFunctionParams(FunctionName) ⇒ <code>\*</code>
Calls a dynamic function with parameters (if it exists), also allow ! in front to reverse the result. The dynamic function is the provided function name in the dialog option object and it is prefixed by the current screen.

**Kind**: global function  
**Returns**: <code>\*</code> - - Returns what the dynamic function returns or FALSE if the function does not exist  

| Param | Type | Description |
| --- | --- | --- |
| FunctionName | <code>string</code> | Function name to call dynamically |

<a name="CommonCallFunctionByName"></a>

## CommonCallFunctionByName(FunctionName, [...args])
Calls a named global function with the passed in arguments, if the named function exists. Differs from
 CommonDynamicFunctionParams in that arguments are not parsed from the passed in FunctionName string, but
 passed directly into the function call, allowing for more complex JS objects to be passed in. This
 function will not log to console if the provided function name does not exist as a global function.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| FunctionName | <code>string</code> | The name of the global function to call |
| [...args] | <code>\*</code> | zero or more arguments to be passed to the function (optional) |

<a name="CommonSetScreen"></a>

## CommonSetScreen(NewModule, NewScreen) ⇒ <code>void</code>
Sets the current screen and calls the loading script if needed

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NewModule | <code>string</code> | Module of the screen to display |
| NewScreen | <code>string</code> | Screen to display |

<a name="CommonTime"></a>

## CommonTime() ⇒ <code>number</code>
Gets the current time in ms

**Kind**: global function  
**Returns**: <code>number</code> - - Date in ms  
<a name="CommonIsColor"></a>

## CommonIsColor(Value) ⇒ <code>boolean</code>
Checks if a given value is a valid HEX color code

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the string is a valid HEX color  

| Param | Type | Description |
| --- | --- | --- |
| Value | <code>string</code> | Potential HEX color code |

<a name="CommonRandomItemFromList"></a>

## CommonRandomItemFromList(ItemPrevious, ItemList) ⇒ <code>\*</code>
Get a random item from a list while making sure not to pick the previous one.

**Kind**: global function  
**Returns**: <code>\*</code> - - The randomly selected item from the list  

| Param | Type | Description |
| --- | --- | --- |
| ItemPrevious | <code>\*</code> | Previously selected item from the given list |
| ItemList | <code>\*</code> | List for which to pick a random item from |

<a name="CommonConvertStringToArray"></a>

## CommonConvertStringToArray(s) ⇒ <code>Array.&lt;number&gt;</code>
Converts a string of numbers split by commas to an array, sanitizes the array by removing all NaN or undefined elements.

**Kind**: global function  
**Returns**: <code>Array.&lt;number&gt;</code> - - Array of valid numbers from the given string  

| Param | Type | Description |
| --- | --- | --- |
| s | <code>string</code> | String of numbers split by commas |

<a name="CommonConvertArrayToString"></a>

## CommonConvertArrayToString(Arr) ⇒ <code>string</code>
Converts an array to a string separated by commas (equivalent of .join(","))

**Kind**: global function  
**Returns**: <code>string</code> - - String of all the array items joined together  

| Param | Type | Description |
| --- | --- | --- |
| Arr | <code>Array</code> | Array to convert to a joined string |
