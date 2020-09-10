## Functions

<dl>
<dt><a href="#ElementValue">ElementValue(ID, [Value])</a> ⇒ <code>string</code> | <code>undefined</code></dt>
<dd><p>Handles the value of a HTML element. It sets the value of the element when the Value parameter is provided or it returns the value when the parameter is omitted</p>
</dd>
<dt><a href="#ElementContent">ElementContent(ID, [Content])</a> ⇒ <code>string</code> | <code>undefined</code></dt>
<dd><p>Handles the content of a HTML element. It sets the content of the element when the Content parameter is provided or it returns the value when the parameter is omitted</p>
</dd>
<dt><a href="#ElementCreateTextArea">ElementCreateTextArea(ID)</a> ⇒ <code>void</code></dt>
<dd><p>Creates a new text area element in the main document. Does not create a new element if there is already an existing one with the same ID</p>
</dd>
<dt><a href="#ElementCreateInput">ElementCreateInput(ID, Type, Value, MaxLength)</a> ⇒ <code>void</code></dt>
<dd><p>Creates a new text input element in the main document.Does not create a new element if there is already an existing one with the same ID</p>
</dd>
<dt><a href="#ElementCreateDropdown">ElementCreateDropdown(ID, Options, [ClickEventListener])</a> ⇒ <code>void</code></dt>
<dd><p>Creates a dropdown element and adjusts it to the BC look and feel. In the HTML Code this will look like this:</p>
<div> -- enclosing div used for css and postioning
    <select> -- the select statement with its options
        <option 1>
        <option n>
    </select>
    <div></div> -- the div representing the currently selected item
    <div> -- div for the various options
       <div>Option 1</div>
       <div>Option n</div>
    </div>
</div>
This construct is built automatically and ignores the original select statement. All the logic is handled by 
event handlers that are connected to the various divs. See comments in the code.
What this function cannot handle at the moment:
- The size is always set to 1
- Multiple selects are impossible</dd>
<dt><a href="#ElementCloseAllSelect">ElementCloseAllSelect(elmnt)</a> ⇒ <code>void</code></dt>
<dd><p>Closes all select boxes in the current document, except the current select box</p>
</dd>
<dt><a href="#ElementCreateDiv">ElementCreateDiv(ID)</a> ⇒ <code>void</code></dt>
<dd><p>Creates a new div element in the main document. Does not create a new element if there is already an existing one with the same ID</p>
</dd>
<dt><a href="#ElementRemove">ElementRemove(ID)</a> ⇒ <code>void</code></dt>
<dd><p>Removes an element from the main document</p>
</dd>
<dt><a href="#ElementPosition">ElementPosition(ElementID, X, Y, W, H)</a> ⇒ <code>void</code></dt>
<dd><p>Draws an existing HTML element at a specific position within the document. The element is &quot;centered&quot; on the given coordinates by dividing its height and width by two.</p>
</dd>
<dt><a href="#ElementPositionFix">ElementPositionFix(ElementID, X, Y, W, H)</a> ⇒ <code>void</code></dt>
<dd><p>Draws an existing HTML element at a specific position within the document. The element will not be centered on its given coordinates unlike the ElementPosition function.</p>
</dd>
<dt><a href="#ElementSetDataAttribute">ElementSetDataAttribute(ID, Name, Value)</a> ⇒ <code>void</code></dt>
<dd><p>Sets a custom data-attribute to a specified value on a specified element</p>
</dd>
<dt><a href="#ElementScrollToEnd">ElementScrollToEnd(ID)</a> ⇒ <code>void</code></dt>
<dd><p>Scrolls to the end of a specified element</p>
</dd>
<dt><a href="#ElementIsScrolledToEnd">ElementIsScrolledToEnd(ID)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a given HTML element is scrolled to the very bottom.</p>
</dd>
<dt><a href="#ElementFocus">ElementFocus(ID)</a> ⇒ <code>void</code></dt>
<dd><p>Gives focus to a specified existing element for non-mobile users.</p>
</dd>
</dl>

<a name="ElementValue"></a>

## ElementValue(ID, [Value]) ⇒ <code>string</code> \| <code>undefined</code>
Handles the value of a HTML element. It sets the value of the element when the Value parameter is provided or it returns the value when the parameter is omitted

**Kind**: global function  
**Returns**: <code>string</code> \| <code>undefined</code> - - The value of the element (When no value parameter was passed to the function)  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the element for which we want to get/set the value. |
| [Value] | <code>string</code> | The value to give to the element (if applicable) |

<a name="ElementContent"></a>

## ElementContent(ID, [Content]) ⇒ <code>string</code> \| <code>undefined</code>
Handles the content of a HTML element. It sets the content of the element when the Content parameter is provided or it returns the value when the parameter is omitted

**Kind**: global function  
**Returns**: <code>string</code> \| <code>undefined</code> - - The content of the element (When no Content parameter was passed to the function)  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the element for which we want to get/set the value. |
| [Content] | <code>string</code> | The content/inner HTML to give to the element (if applicable) |

<a name="ElementCreateTextArea"></a>

## ElementCreateTextArea(ID) ⇒ <code>void</code>
Creates a new text area element in the main document. Does not create a new element if there is already an existing one with the same ID

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the text area to create. |

<a name="ElementCreateInput"></a>

## ElementCreateInput(ID, Type, Value, MaxLength) ⇒ <code>void</code>
Creates a new text input element in the main document.Does not create a new element if there is already an existing one with the same ID

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the input tag to create. |
| Type | <code>string</code> | Type of the input tag to create. |
| Value | <code>string</code> | Value of the input tag to create. |
| MaxLength | <code>string</code> | Maximum input tag of the input to create. |

<a name="ElementCreateDropdown"></a>

## ElementCreateDropdown(ID, Options, [ClickEventListener]) ⇒ <code>void</code>
Creates a dropdown element and adjusts it to the BC look and feel. In the HTML Code this will look like this:
<div> -- enclosing div used for css and postioning
    <select> -- the select statement with its options
        <option 1>
        <option n>
    </select>
    <div></div> -- the div representing the currently selected item
    <div> -- div for the various options
       <div>Option 1</div>
       <div>Option n</div>
    </div>
</div>
This construct is built automatically and ignores the original select statement. All the logic is handled by 
event handlers that are connected to the various divs. See comments in the code.
What this function cannot handle at the moment:
- The size is always set to 1
- Multiple selects are impossible

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| ID | <code>string</code> |  | The name of the select item. The outer div will get this name, for positioning. The select tag will get the name ID+"-select" |
| Options | <code>Array.&lt;atring&gt;</code> |  | The list of options for the current select statement |
| [ClickEventListener] | <code>function</code> | <code></code> | An event listener to be called, when the value of the drop down box changes |

<a name="ElementCloseAllSelect"></a>

## ElementCloseAllSelect(elmnt) ⇒ <code>void</code>
Closes all select boxes in the current document, except the current select box

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| elmnt | <code>object</code> | The select box to exclude from the closing |

<a name="ElementCreateDiv"></a>

## ElementCreateDiv(ID) ⇒ <code>void</code>
Creates a new div element in the main document. Does not create a new element if there is already an existing one with the same ID

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the div tag to create. |

<a name="ElementRemove"></a>

## ElementRemove(ID) ⇒ <code>void</code>
Removes an element from the main document

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the tag to remove from the document. |

<a name="ElementPosition"></a>

## ElementPosition(ElementID, X, Y, W, H) ⇒ <code>void</code>
Draws an existing HTML element at a specific position within the document. The element is "centered" on the given coordinates by dividing its height and width by two.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ElementID | <code>string</code> | The id of the input tag to (re-)position. |
| X | <code>number</code> | Center point of the element on the X axis. |
| Y | <code>number</code> | Center point of the element on the Y axis. |
| W | <code>number</code> | Width of the element. |
| H | <code>number</code> | Height of the element. |

<a name="ElementPositionFix"></a>

## ElementPositionFix(ElementID, X, Y, W, H) ⇒ <code>void</code>
Draws an existing HTML element at a specific position within the document. The element will not be centered on its given coordinates unlike the ElementPosition function.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ElementID | <code>string</code> | The id of the input tag to (re-)position. |
| X | <code>number</code> | Starting point of the element on the X axis. |
| Y | <code>number</code> | Starting point of the element on the Y axis. |
| W | <code>number</code> | Width of the element. |
| H | <code>number</code> | Height of the element. |

<a name="ElementSetDataAttribute"></a>

## ElementSetDataAttribute(ID, Name, Value) ⇒ <code>void</code>
Sets a custom data-attribute to a specified value on a specified element

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the element to create/set the data attribute of. |
| Name | <code>string</code> | Name of the data attribute. ("data-" will be automatically appended to it.) |
| Value | <code>string</code> | Value to give to the attribute. |

<a name="ElementScrollToEnd"></a>

## ElementScrollToEnd(ID) ⇒ <code>void</code>
Scrolls to the end of a specified element

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the element to scroll down to the bottom of. |

<a name="ElementIsScrolledToEnd"></a>

## ElementIsScrolledToEnd(ID) ⇒ <code>boolean</code>
Checks if a given HTML element is scrolled to the very bottom.

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the specified element is scrolled to the very bottom  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the element to check for scroll height. |

<a name="ElementFocus"></a>

## ElementFocus(ID) ⇒ <code>void</code>
Gives focus to a specified existing element for non-mobile users.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ID | <code>string</code> | The id of the element to give focus to. |
