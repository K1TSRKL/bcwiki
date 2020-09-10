## Functions

<dl>
<dt><a href="#DrawHexToRGB">DrawHexToRGB(color)</a> ⇒ <code>string</code></dt>
<dd><p>Converts a hex color string to a RGB color</p>
</dd>
<dt><a href="#DrawRGBToHex">DrawRGBToHex(color)</a> ⇒ <code>string</code></dt>
<dd><p>Converts a RGB color to a hex color string</p>
</dd>
<dt><a href="#DrawLoad">DrawLoad()</a> ⇒ <code>void</code></dt>
<dd><p>Loads the canvas to draw on with its style and event listeners.</p>
</dd>
<dt><a href="#DrawGetImage">DrawGetImage(Source)</a> ⇒ <code>HTMLImageElement</code></dt>
<dd><p>Returns the image file from cache or build it from the source</p>
</dd>
<dt><a href="#DrawGetImageOnLoad">DrawGetImageOnLoad()</a> ⇒ <code>void</code></dt>
<dd><p>Reloads all character canvas once all images are loaded</p>
</dd>
<dt><a href="#DrawGetImageOnError">DrawGetImageOnError(Img, IsAsset)</a> ⇒ <code>void</code></dt>
<dd><p>Attempts to redownload an image if it previously failed to load</p>
</dd>
<dt><a href="#DrawArousalThermometer">DrawArousalThermometer(X, Y, Zoom, Progress, Automatic, Orgasm)</a> ⇒ <code>void</code></dt>
<dd><p>Draws the arousal meter on screen</p>
</dd>
<dt><a href="#DrawArousalMeter">DrawArousalMeter(C, X, Y, Zoom)</a> ⇒ <code>void</code></dt>
<dd><p>Draw the arousal meter next to the player if it is allowed by the character and visible for the player</p>
</dd>
<dt><a href="#DrawCharacter">DrawCharacter(C, X, Y, Zoom, IsHeightResizeAllowed)</a> ⇒ <code>void</code></dt>
<dd><p>Refreshes the character if not all images are loaded and draw the character canvas on the main game screen</p>
</dd>
<dt><a href="#DrawAssetGroupZone">DrawAssetGroupZone(C, Zone, HeightRatio, X, Y, Color, [Thickness])</a> ⇒ <code>void</code></dt>
<dd><p>Draws an asset group zone outline over the character</p>
</dd>
<dt><a href="#DrawAssetGroupZoneBackground">DrawAssetGroupZoneBackground(C, Zone, HeightRatio, X, Y, Color)</a> ⇒ <code>void</code></dt>
<dd><p>Draws an asset group zone background over the character</p>
</dd>
<dt><a href="#DrawImageZoomCanvas">DrawImageZoomCanvas(Source, Canvas, SX, SY, SWidth, SHeight, X, Y, Width, Height)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws a zoomed image from a source to a specific canvas</p>
</dd>
<dt><a href="#DrawImageResize">DrawImageResize(Source, X, Y, Width, Height)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws a resized image from a source to the main canvas</p>
</dd>
<dt><a href="#DrawImageCanvas">DrawImageCanvas(Source, Canvas, X, Y, AlphaMasks)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws a zoomed image from a source to a specific canvas</p>
</dd>
<dt><a href="#DrawCanvas">DrawCanvas(Img, Canvas, X, Y, AlphaMasks)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws a canvas to a specific canvas</p>
</dd>
<dt><a href="#DrawCanvasZoom">DrawCanvasZoom(Canvas, X, Y, Zoom)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a specific canvas with a zoom on the main canvas</p>
</dd>
<dt><a href="#DrawImageZoomMirror">DrawImageZoomMirror(Source, X, Y, Width, Height)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws a zoomed image from a source to the canvas and mirrors it from left to right</p>
</dd>
<dt><a href="#DrawImage">DrawImage(Source, X, Y)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws an image from a source on the main canvas</p>
</dd>
<dt><a href="#DrawImageCanvasColorize">DrawImageCanvasColorize(Source, Canvas, X, Y, Zoom, HexColor, FullAlpha, AlphaMasks)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws an image from a source to the specified canvas</p>
</dd>
<dt><a href="#DrawImageMirror">DrawImageMirror(Source, X, Y)</a> ⇒ <code>boolean</code></dt>
<dd><p>Draws the mirrored version of an image from a source on the canvas</p>
</dd>
<dt><a href="#GetWrapTextSize">GetWrapTextSize(Text, Width, MaxLine)</a> ⇒ <code>void</code></dt>
<dd><p>Reduces the font size progressively until the text fits the wrap size</p>
</dd>
<dt><a href="#DrawTextWrap">DrawTextWrap(Text, X, Y, Width, Height, ForeColor, BackColor, MaxLine)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a word wrapped text in a rectangle</p>
</dd>
<dt><a href="#DrawTextFit">DrawTextFit(Text, X, Y, Width, Color)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a text element on the canvas that will fit on the specified width</p>
</dd>
<dt><a href="#DrawText">DrawText(Text, X, Y, Color, BackColor)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a text element on the canvas</p>
</dd>
<dt><a href="#DrawButton">DrawButton(Left, Top, Width, Height, Label, Color, [Image], [HoveringText])</a> ⇒ <code>void</code></dt>
<dd><p>Draws a button component</p>
</dd>
<dt><a href="#DrawCheckbox">DrawCheckbox(Left, Top, Width, Height, Text, IsChecked)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a checkbox component</p>
</dd>
<dt><a href="#DrawBackNextButton">DrawBackNextButton(Left, Top, Width, Height, Label, Color, [Image], BackText, NextText)</a> ⇒ <code>void</code></dt>
<dd><p>Draw a back &amp; next button component</p>
</dd>
<dt><a href="#DrawButtonHover">DrawButtonHover(Left, Top, Width, Height, HoveringText)</a> ⇒ <code>void</code></dt>
<dd><p>Draw the hovering text tooltip</p>
</dd>
<dt><a href="#DrawEmptyRect">DrawEmptyRect(Left, Top, Width, Height, Color, [Thickness])</a> ⇒ <code>void</code></dt>
<dd><p>Draws a basic empty rectangle with a colored outline</p>
</dd>
<dt><a href="#DrawRect">DrawRect(Left, Top, Width, Height, Color)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a basic rectangle filled with a given color</p>
</dd>
<dt><a href="#DrawCircle">DrawCircle(CenterX, CenterY, Radius, LineWidth, LineColor)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a basic circle</p>
</dd>
<dt><a href="#DrawProgressBar">DrawProgressBar(X, Y, W, H, Progress)</a> ⇒ <code>void</code></dt>
<dd><p>Draws a progress bar</p>
</dd>
<dt><a href="#DrawProcess">DrawProcess()</a> ⇒ <code>void</code></dt>
<dd><p>Constantly looping draw process. Draws beeps, handles the screen size, handles the current blindfold state and draws the current screen.</p>
</dd>
<dt><a href="#DrawItemPreview">DrawItemPreview(X, Y, Item)</a> ⇒ <code>void</code></dt>
<dd><p>Draws the item preview box</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#Item">Item</a> : <code>Object</code></dt>
<dd><p>An item is a pair of asset and its dynamic properties that define a worn asset.</p>
</dd>
</dl>

<a name="DrawHexToRGB"></a>

## DrawHexToRGB(color) ⇒ <code>string</code>
Converts a hex color string to a RGB color

**Kind**: global function  
**Returns**: <code>string</code> - - RGB color  

| Param | Type | Description |
| --- | --- | --- |
| color | <code>string</code> | Hex color to conver |

<a name="DrawRGBToHex"></a>

## DrawRGBToHex(color) ⇒ <code>string</code>
Converts a RGB color to a hex color string

**Kind**: global function  
**Returns**: <code>string</code> - - Hex color string  

| Param | Type | Description |
| --- | --- | --- |
| color | <code>string</code> | RGB color to conver |

<a name="DrawLoad"></a>

## DrawLoad() ⇒ <code>void</code>
Loads the canvas to draw on with its style and event listeners.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DrawGetImage"></a>

## DrawGetImage(Source) ⇒ <code>HTMLImageElement</code>
Returns the image file from cache or build it from the source

**Kind**: global function  
**Returns**: <code>HTMLImageElement</code> - - Image file  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |

<a name="DrawGetImageOnLoad"></a>

## DrawGetImageOnLoad() ⇒ <code>void</code>
Reloads all character canvas once all images are loaded

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DrawGetImageOnError"></a>

## DrawGetImageOnError(Img, IsAsset) ⇒ <code>void</code>
Attempts to redownload an image if it previously failed to load

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Img | <code>HTMLImageElement</code> | Image tag that failed to load |
| IsAsset | <code>boolean</code> | Whether or not the image is part of an asset |

<a name="DrawArousalThermometer"></a>

## DrawArousalThermometer(X, Y, Zoom, Progress, Automatic, Orgasm) ⇒ <code>void</code>
Draws the arousal meter on screen

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| X | <code>number</code> | Position of the meter on the X axis |
| Y | <code>number</code> | Position of the meter on the Y axis |
| Zoom | <code>number</code> | Zoom factor |
| Progress | <code>number</code> | Current progress of the arousal meter |
| Automatic | <code>boolean</code> | Wheter or not the arousal is in automatic mode |
| Orgasm | <code>boolean</code> | Whether or not the meter is in recover from orgasm mode |

<a name="DrawArousalMeter"></a>

## DrawArousalMeter(C, X, Y, Zoom) ⇒ <code>void</code>
Draw the arousal meter next to the player if it is allowed by the character and visible for the player

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to potentially draw the arousal meter |
| X | <code>number</code> | Position of the meter on the X axis |
| Y | <code>number</code> | Position of the meter on the Y axis |
| Zoom | <code>number</code> | Zoom factor |

<a name="DrawCharacter"></a>

## DrawCharacter(C, X, Y, Zoom, IsHeightResizeAllowed) ⇒ <code>void</code>
Refreshes the character if not all images are loaded and draw the character canvas on the main game screen

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to draw |
| X | <code>number</code> | Position of the character on the X axis |
| Y | <code>number</code> | Position of the character on the Y axis |
| Zoom | <code>number</code> | Zoom factor |
| IsHeightResizeAllowed | <code>boolean</code> | Whether or not the settings allow for the height modifier to be applied |

<a name="DrawAssetGroupZone"></a>

## DrawAssetGroupZone(C, Zone, HeightRatio, X, Y, Color, [Thickness]) ⇒ <code>void</code>
Draws an asset group zone outline over the character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| C | <code>Character</code> |  | Character for which to draw the zone |
| Zone | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> |  | Zone to be drawn |
| HeightRatio | <code>number</code> |  | Height ratio of the character |
| X | <code>number</code> |  | Position of the character on the X axis |
| Y | <code>number</code> |  | Position of the character on the Y axis |
| Color | <code>string</code> |  | Color of the zone outline |
| [Thickness] | <code>number</code> | <code>3</code> | Thickness of the outline |

<a name="DrawAssetGroupZoneBackground"></a>

## DrawAssetGroupZoneBackground(C, Zone, HeightRatio, X, Y, Color) ⇒ <code>void</code>
Draws an asset group zone background over the character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to draw the zone |
| Zone | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | Zone to be drawn |
| HeightRatio | <code>number</code> | Height ratio of the character |
| X | <code>number</code> | Position of the character on the X axis |
| Y | <code>number</code> | Position of the character on the Y axis |
| Color | <code>string</code> | Color of the zone background |

<a name="DrawImageZoomCanvas"></a>

## DrawImageZoomCanvas(Source, Canvas, SX, SY, SWidth, SHeight, X, Y, Width, Height) ⇒ <code>boolean</code>
Draws a zoomed image from a source to a specific canvas

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |
| Canvas | <code>HTMLCanvasElement</code> | Canvas on which to draw the image |
| SX | <code>number</code> | The X coordinate where to start clipping |
| SY | <code>number</code> | The Y coordinate where to start clipping |
| SWidth | <code>number</code> | The width of the clipped image |
| SHeight | <code>number</code> | The height of the clipped image |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |
| Width | <code>number</code> | Width of the image |
| Height | <code>number</code> | Height of the image |

<a name="DrawImageResize"></a>

## DrawImageResize(Source, X, Y, Width, Height) ⇒ <code>boolean</code>
Draws a resized image from a source to the main canvas

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |
| Width | <code>number</code> | Width of the image after being resized |
| Height | <code>number</code> | Height of the image after being resized |

<a name="DrawImageCanvas"></a>

## DrawImageCanvas(Source, Canvas, X, Y, AlphaMasks) ⇒ <code>boolean</code>
Draws a zoomed image from a source to a specific canvas

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |
| Canvas | <code>HTMLCanvasElement</code> | Canvas on which to draw the image |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |
| AlphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="DrawCanvas"></a>

## DrawCanvas(Img, Canvas, X, Y, AlphaMasks) ⇒ <code>boolean</code>
Draws a canvas to a specific canvas

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Img | <code>HTMLCanvasElement</code> | Canvas to draw |
| Canvas | <code>HTMLCanvasElement</code> | Canvas on which to draw the image |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |
| AlphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="DrawCanvasZoom"></a>

## DrawCanvasZoom(Canvas, X, Y, Zoom) ⇒ <code>void</code>
Draws a specific canvas with a zoom on the main canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Canvas | <code>HTMLCanvasElement</code> | Canvas to draw on the main canvas |
| X | <code>number</code> | Position of the canvas on the X axis |
| Y | <code>number</code> | Position of the canvas on the Y axis |
| Zoom | <code>number</code> | Zoom factor |

<a name="DrawImageZoomMirror"></a>

## DrawImageZoomMirror(Source, X, Y, Width, Height) ⇒ <code>boolean</code>
Draws a zoomed image from a source to the canvas and mirrors it from left to right

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |
| Width | <code>number</code> | Width of the image |
| Height | <code>number</code> | Height of the image |

<a name="DrawImage"></a>

## DrawImage(Source, X, Y) ⇒ <code>boolean</code>
Draws an image from a source on the main canvas

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |

<a name="DrawImageCanvasColorize"></a>

## DrawImageCanvasColorize(Source, Canvas, X, Y, Zoom, HexColor, FullAlpha, AlphaMasks) ⇒ <code>boolean</code>
Draws an image from a source to the specified canvas

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |
| Canvas | <code>HTMLCanvasElement</code> | Canvas on which to draw the image |
| X | <code>number</code> | Position of the rectangle on the X axis |
| Y | <code>number</code> | Position of the rectangle on the Y axis |
| Zoom | <code>number</code> | Zoom factor |
| HexColor | <code>string</code> | Color of the image to draw |
| FullAlpha | <code>boolean</code> | Whether or not it is drawn in full alpha mode |
| AlphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="DrawImageMirror"></a>

## DrawImageMirror(Source, X, Y) ⇒ <code>boolean</code>
Draws the mirrored version of an image from a source on the canvas

**Kind**: global function  
**Returns**: <code>boolean</code> - - whether the image was complete or not  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>string</code> | URL of the image |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |

<a name="GetWrapTextSize"></a>

## GetWrapTextSize(Text, Width, MaxLine) ⇒ <code>void</code>
Reduces the font size progressively until the text fits the wrap size

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Text | <code>string</code> | Text that will be drawn |
| Width | <code>number</code> | Width in which the text must fit |
| MaxLine | <code>number</code> | Maximum of lines the word can wrap for |

<a name="DrawTextWrap"></a>

## DrawTextWrap(Text, X, Y, Width, Height, ForeColor, BackColor, MaxLine) ⇒ <code>void</code>
Draws a word wrapped text in a rectangle

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Text | <code>string</code> | Text to draw |
| X | <code>number</code> | Position of the rectangle on the X axis |
| Y | <code>number</code> | Position of the rectangle on the Y axis |
| Width | <code>number</code> | Width of the rectangle |
| Height | <code>number</code> | Height of the rectangle |
| ForeColor | <code>string</code> | Foreground color |
| BackColor | <code>string</code> | Background color |
| MaxLine | <code>number</code> | Maximum of lines the word can wrap for |

<a name="DrawTextFit"></a>

## DrawTextFit(Text, X, Y, Width, Color) ⇒ <code>void</code>
Draws a text element on the canvas that will fit on the specified width

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Text | <code>string</code> | Text to draw |
| X | <code>number</code> | Position of the text on the X axis |
| Y | <code>number</code> | Position of the text on the Y axis |
| Width | <code>number</code> | Width in which the text has to fit |
| Color | <code>string</code> | Color of the text |

<a name="DrawText"></a>

## DrawText(Text, X, Y, Color, BackColor) ⇒ <code>void</code>
Draws a text element on the canvas

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Text | <code>string</code> | Text to draw |
| X | <code>number</code> | Position of the text on the X axis |
| Y | <code>number</code> | Position of the text on the Y axis |
| Color | <code>string</code> | Color of the text |
| BackColor | <code>string</code> | Color of the background |

<a name="DrawButton"></a>

## DrawButton(Left, Top, Width, Height, Label, Color, [Image], [HoveringText]) ⇒ <code>void</code>
Draws a button component

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Left | <code>number</code> | Position of the component from the left of the canvas |
| Top | <code>number</code> | Position of the component from the top of the canvas |
| Width | <code>number</code> | Width of the component |
| Height | <code>number</code> | Height of the component |
| Label | <code>string</code> | Text to display in the button |
| Color | <code>string</code> | Color of the component |
| [Image] | <code>string</code> | URL of the image to draw inside the button, if applicable |
| [HoveringText] | <code>string</code> | Text of the tooltip, if applicable |

<a name="DrawCheckbox"></a>

## DrawCheckbox(Left, Top, Width, Height, Text, IsChecked) ⇒ <code>void</code>
Draws a checkbox component

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Left | <code>number</code> | Position of the component from the left of the canvas |
| Top | <code>number</code> | Position of the component from the top of the canvas |
| Width | <code>number</code> | Width of the component |
| Height | <code>number</code> | Height of the component |
| Text | <code>string</code> | Label associated with the checkbox |
| IsChecked | <code>boolean</code> | Whether or not the checkbox is checked |

<a name="DrawBackNextButton"></a>

## DrawBackNextButton(Left, Top, Width, Height, Label, Color, [Image], BackText, NextText) ⇒ <code>void</code>
Draw a back & next button component

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Left | <code>number</code> | Position of the component from the left of the canvas |
| Top | <code>number</code> | Position of the component from the top of the canvas |
| Width | <code>number</code> | Width of the component |
| Height | <code>number</code> | Height of the component |
| Label | <code>string</code> | Text inside the component |
| Color | <code>string</code> | Color of the component |
| [Image] | <code>string</code> | Image URL to draw in the component |
| BackText | <code>string</code> | Text for the back button tooltip |
| NextText | <code>string</code> | Text for the next button tooltip |

<a name="DrawButtonHover"></a>

## DrawButtonHover(Left, Top, Width, Height, HoveringText) ⇒ <code>void</code>
Draw the hovering text tooltip

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Left | <code>number</code> | Position of the tooltip from the left of the canvas |
| Top | <code>number</code> | Position of the tooltip from the top of the canvas |
| Width | <code>number</code> | Width of the tooltip |
| Height | <code>number</code> | Height of the tooltip |
| HoveringText | <code>string</code> | Text to display in the tooltip |

<a name="DrawEmptyRect"></a>

## DrawEmptyRect(Left, Top, Width, Height, Color, [Thickness]) ⇒ <code>void</code>
Draws a basic empty rectangle with a colored outline

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| Left | <code>number</code> |  | Position of the rectangle from the left of the canvas |
| Top | <code>number</code> |  | Position of the rectangle from the top of the canvas |
| Width | <code>number</code> |  | Width of the rectangle |
| Height | <code>number</code> |  | Height of the rectangle |
| Color | <code>string</code> |  | Color of the rectangle outline |
| [Thickness] | <code>number</code> | <code>3</code> | Thickness of the rectangle line |

<a name="DrawRect"></a>

## DrawRect(Left, Top, Width, Height, Color) ⇒ <code>void</code>
Draws a basic rectangle filled with a given color

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Left | <code>number</code> | Position of the rectangle from the left of the canvas |
| Top | <code>number</code> | Position of the rectangle from the top of the canvas |
| Width | <code>number</code> | Width of the rectangle |
| Height | <code>number</code> | Height of the rectangle |
| Color | <code>string</code> | Color of the rectangle |

<a name="DrawCircle"></a>

## DrawCircle(CenterX, CenterY, Radius, LineWidth, LineColor) ⇒ <code>void</code>
Draws a basic circle

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| CenterX | <code>number</code> | Position of the center of the circle on the X axis |
| CenterY | <code>number</code> | Position of the center of the circle on the Y axis |
| Radius | <code>number</code> | Radius of the circle to draw |
| LineWidth | <code>number</code> | Width of the line |
| LineColor | <code>string</code> | Color of the circle's line |

<a name="DrawProgressBar"></a>

## DrawProgressBar(X, Y, W, H, Progress) ⇒ <code>void</code>
Draws a progress bar

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| X | <code>number</code> | Position of the bar on the X axis |
| Y | <code>number</code> | Position of the bar on the Y axis |
| W | <code>number</code> | Width of the bar |
| H | <code>number</code> | Height of the bar |
| Progress | <code>number</code> | Current progress to display on the bar |

<a name="DrawProcess"></a>

## DrawProcess() ⇒ <code>void</code>
Constantly looping draw process. Draws beeps, handles the screen size, handles the current blindfold state and draws the current screen.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DrawItemPreview"></a>

## DrawItemPreview(X, Y, Item) ⇒ <code>void</code>
Draws the item preview box

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| X | <code>number</code> | Position of the item on the X axis |
| Y | <code>number</code> | Position of the item on the Y axis |
| Item | [<code>Item</code>](#Item) | The item to draw the preview for |

<a name="Item"></a>

## Item : <code>Object</code>
An item is a pair of asset and its dynamic properties that define a worn asset.

**Kind**: global typedef  
