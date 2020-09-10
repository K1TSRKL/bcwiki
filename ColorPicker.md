## Functions

<dl>
<dt><a href="#ColorPickerAttachEventListener">ColorPickerAttachEventListener()</a> ⇒ <code>void</code></dt>
<dd><p>Attaches event listeners required for the color picker to the canvas</p>
</dd>
<dt><a href="#ColorPickerRemoveEventListener">ColorPickerRemoveEventListener()</a> ⇒ <code>void</code></dt>
<dd><p>Removes the color picker related event listeners from the canvas</p>
</dd>
<dt><a href="#ColorPickerStartPick">ColorPickerStartPick(Event)</a> ⇒ <code>void</code></dt>
<dd><p>When the touch/mouse event begins to be registered. On mobile we only fire it once</p>
</dd>
<dt><a href="#ColorPickerEndPick">ColorPickerEndPick()</a> ⇒ <code>void</code></dt>
<dd><p>When we stop registering the touch/mouse event, to remove the attached event listeners</p>
</dd>
<dt><a href="#ColorPickerGetCoordinates">ColorPickerGetCoordinates(Event)</a> ⇒ <code>Object</code></dt>
<dd><p>Gets the coordinates of the current event on the canvas</p>
</dd>
<dt><a href="#ColorPickerPickHue">ColorPickerPickHue(Event)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the picked hue based on the Event coordinates on the canvas</p>
</dd>
<dt><a href="#ColorPickerPickSV">ColorPickerPickSV(Event)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the picked saturation (SV) based on the Event coordinates on the canvas</p>
</dd>
<dt><a href="#ColorPickerSelectFromPallete">ColorPickerSelectFromPallete(Event)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the picked HSV from the color pallet</p>
</dd>
<dt><a href="#ColorPickerNotify">ColorPickerNotify()</a> ⇒ <code>void</code></dt>
<dd><p>Alters the color picker display based on the selected value</p>
</dd>
<dt><a href="#ColorPickerHide">ColorPickerHide()</a> ⇒ <code>void</code></dt>
<dd><p>Removes the color picker and its listeners from the canvas</p>
</dd>
<dt><a href="#ColorPickerCSSColorEquals">ColorPickerCSSColorEquals(Color1, Color2)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if two hex color codes are equal, will convert short hand hex codes (#FFF is equal to #FFFFFF)</p>
</dd>
<dt><a href="#ColorPickerDraw">ColorPickerDraw(X, Y, Width, Height, Src, Callback)</a> ⇒ <code>void</code></dt>
<dd><p>Draws the color picker on the canvas</p>
</dd>
<dt><a href="#ColorPickerCSSToHSV">ColorPickerCSSToHSV(Color, [DefaultHSV])</a> ⇒ <code><a href="#HSVColor">HSVColor</a></code></dt>
<dd><p>Parses a hex color code and converts it to a HSV object</p>
</dd>
<dt><a href="#ColorPickerHSVToCSS">ColorPickerHSVToCSS(HSV)</a> ⇒ <code><a href="#HexColor">HexColor</a></code></dt>
<dd><p>Converts a HSV object into a valid hex code to use in the css</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#HexColor">HexColor</a> : <code>string</code></dt>
<dd><p>A hexadecimal color code</p>
</dd>
<dt><a href="#HSVColor">HSVColor</a> : <code>Object</code></dt>
<dd><p>A HSV color value</p>
</dd>
</dl>

<a name="ColorPickerAttachEventListener"></a>

## ColorPickerAttachEventListener() ⇒ <code>void</code>
Attaches event listeners required for the color picker to the canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ColorPickerRemoveEventListener"></a>

## ColorPickerRemoveEventListener() ⇒ <code>void</code>
Removes the color picker related event listeners from the canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ColorPickerStartPick"></a>

## ColorPickerStartPick(Event) ⇒ <code>void</code>
When the touch/mouse event begins to be registered. On mobile we only fire it once

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Event | <code>Event</code> | The touch/mouse event |

<a name="ColorPickerEndPick"></a>

## ColorPickerEndPick() ⇒ <code>void</code>
When we stop registering the touch/mouse event, to remove the attached event listeners

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ColorPickerGetCoordinates"></a>

## ColorPickerGetCoordinates(Event) ⇒ <code>Object</code>
Gets the coordinates of the current event on the canvas

**Kind**: global function  
**Returns**: <code>Object</code> - - Coordinates of the click/touch event on the canvas  

| Param | Type | Description |
| --- | --- | --- |
| Event | <code>Event</code> | The touch/mouse event |

<a name="ColorPickerPickHue"></a>

## ColorPickerPickHue(Event) ⇒ <code>void</code>
Sets the picked hue based on the Event coordinates on the canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Event | <code>Event</code> | The touch/mouse event |

<a name="ColorPickerPickSV"></a>

## ColorPickerPickSV(Event) ⇒ <code>void</code>
Sets the picked saturation (SV) based on the Event coordinates on the canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Event | <code>Event</code> | The touch/mouse event |

<a name="ColorPickerSelectFromPallete"></a>

## ColorPickerSelectFromPallete(Event) ⇒ <code>void</code>
Sets the picked HSV from the color pallet

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Event | <code>Event</code> | The touch/mouse event |

<a name="ColorPickerNotify"></a>

## ColorPickerNotify() ⇒ <code>void</code>
Alters the color picker display based on the selected value

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ColorPickerHide"></a>

## ColorPickerHide() ⇒ <code>void</code>
Removes the color picker and its listeners from the canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ColorPickerCSSColorEquals"></a>

## ColorPickerCSSColorEquals(Color1, Color2) ⇒ <code>boolean</code>
Checks if two hex color codes are equal, will convert short hand hex codes (#FFF is equal to #FFFFFF)

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the two colors are the same  

| Param | Type | Description |
| --- | --- | --- |
| Color1 | [<code>HexColor</code>](#HexColor) | First color to compare |
| Color2 | [<code>HexColor</code>](#HexColor) | Second color to compare |

<a name="ColorPickerDraw"></a>

## ColorPickerDraw(X, Y, Width, Height, Src, Callback) ⇒ <code>void</code>
Draws the color picker on the canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| X | <code>number</code> | Coordinate on the X axis |
| Y | <code>number</code> | Coordinate on the Y axis |
| Width | <code>number</code> | Width of the color picker |
| Height | <code>number</code> | Height of the color picker |
| Src | <code>HTMLInputElement</code> | Input element that can contain a hex color code |
| Callback | <code>function</code> | Callback to execute when the selected color changes |

<a name="ColorPickerCSSToHSV"></a>

## ColorPickerCSSToHSV(Color, [DefaultHSV]) ⇒ [<code>HSVColor</code>](#HSVColor)
Parses a hex color code and converts it to a HSV object

**Kind**: global function  
**Returns**: [<code>HSVColor</code>](#HSVColor) - - The HSV color from a hex color code  
**See**: [https://gist.github.com/mjackson/5311256](https://gist.github.com/mjackson/5311256)  

| Param | Type | Description |
| --- | --- | --- |
| Color | [<code>HexColor</code>](#HexColor) | Hex color code |
| [DefaultHSV] | [<code>HSVColor</code>](#HSVColor) | The HSV to output if the color is not valid |

<a name="ColorPickerHSVToCSS"></a>

## ColorPickerHSVToCSS(HSV) ⇒ [<code>HexColor</code>](#HexColor)
Converts a HSV object into a valid hex code to use in the css

**Kind**: global function  
**Returns**: [<code>HexColor</code>](#HexColor) - - Hex color code corresponding to the given HSV  

| Param | Type | Description |
| --- | --- | --- |
| HSV | [<code>HSVColor</code>](#HSVColor) | HSV value to convert |

<a name="HexColor"></a>

## HexColor : <code>string</code>
A hexadecimal color code

**Kind**: global typedef  
<a name="HSVColor"></a>

## HSVColor : <code>Object</code>
A HSV color value

**Kind**: global typedef  
