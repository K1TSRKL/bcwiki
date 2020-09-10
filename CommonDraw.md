## Functions

<dl>
<dt><a href="#CommonDrawCanvasPrepare">CommonDrawCanvasPrepare(C)</a> ⇒ <code>void</code></dt>
<dd><p>Prepares the character&#39;s drawing canvases before drawing the character&#39;s appearance.</p>
</dd>
<dt><a href="#CommonDrawAppearanceBuild">CommonDrawAppearanceBuild(C, clearRect, clearRectBlink, drawCanvas, drawCanvasBlink, drawImage, drawImageBlink, drawImageColorize, drawImageColorizeBlink)</a></dt>
<dd><p>Draws the given character&#39;s appearance using the provided drawing callbacks</p>
</dd>
<dt><a href="#CommonDrawFindPose">CommonDrawFindPose(C, AllowedPoses)</a> ⇒ <code>string</code></dt>
<dd><p>Finds the correct pose to draw for drawable layer for the provided character from the provided list of allowed poses</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#clearRect">clearRect</a> : <code>function</code></dt>
<dd><p>A callback function used for clearing a rectangular area of a canvas</p>
</dd>
<dt><a href="#drawImage">drawImage</a> : <code>function</code></dt>
<dd><p>A callback function used to draw an image to a canvas</p>
</dd>
<dt><a href="#drawCanvas">drawCanvas</a> : <code>function</code></dt>
<dd><p>A callback function used to draw a canvas on a canvas</p>
</dd>
<dt><a href="#drawImageColorize">drawImageColorize</a> : <code>function</code></dt>
<dd><p>A callback function used to draw a colorized image to a canvas</p>
</dd>
</dl>

<a name="CommonDrawCanvasPrepare"></a>

## CommonDrawCanvasPrepare(C) ⇒ <code>void</code>
Prepares the character's drawing canvases before drawing the character's appearance.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to prepare |

<a name="CommonDrawAppearanceBuild"></a>

## CommonDrawAppearanceBuild(C, clearRect, clearRectBlink, drawCanvas, drawCanvasBlink, drawImage, drawImageBlink, drawImageColorize, drawImageColorizeBlink)
Draws the given character's appearance using the provided drawing callbacks

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character whose appearance to draw |
| clearRect | [<code>clearRect</code>](#clearRect) | A callback to clear an area of the main character canvas |
| clearRectBlink | [<code>clearRect</code>](#clearRect) | A callback to clear an area of the blink character canvas |
| drawCanvas | [<code>drawCanvas</code>](#drawCanvas) | Function used to draw a canvas on top of the normal canvas |
| drawCanvasBlink | [<code>drawCanvas</code>](#drawCanvas) | Function used to draw a canvas on top of the blink canvas |
| drawImage | [<code>drawImage</code>](#drawImage) | A callback to draw an image to the main character canvas |
| drawImageBlink | [<code>drawImage</code>](#drawImage) | A callback to draw an image to the blink character canvas |
| drawImageColorize | [<code>drawImageColorize</code>](#drawImageColorize) | A callback to draw a colorized image to the main character canvas |
| drawImageColorizeBlink | [<code>drawImageColorize</code>](#drawImageColorize) | A callback to draw a colorized image to the blink character canvas |

<a name="CommonDrawFindPose"></a>

## CommonDrawFindPose(C, AllowedPoses) ⇒ <code>string</code>
Finds the correct pose to draw for drawable layer for the provided character from the provided list of allowed poses

**Kind**: global function  
**Returns**: <code>string</code> - - The name of the pose to draw for the layer, or an empty string if no pose should be drawn  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to check for poses against |
| AllowedPoses | <code>Array.&lt;string&gt;</code> | The list of permitted poses for the current layer |

<a name="clearRect"></a>

## clearRect : <code>function</code>
A callback function used for clearing a rectangular area of a canvas

**Kind**: global typedef  

| Param | Type | Description |
| --- | --- | --- |
| x | <code>number</code> | The x coordinate of the left of the rectangle to clear |
| y | <code>number</code> | The y coordinate of the top of the rectangle to clear |
| w | <code>number</code> | The width of the rectangle to clear |
| h | <code>number</code> | The height of the rectangle to clear |

<a name="drawImage"></a>

## drawImage : <code>function</code>
A callback function used to draw an image to a canvas

**Kind**: global typedef  

| Param | Type | Description |
| --- | --- | --- |
| src | <code>string</code> | The URL of the image to draw |
| x | <code>number</code> | The x coordinate to draw the image at |
| y | <code>number</code> | The y coordinate to draw the image at |
| alphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the image when drawing |

<a name="drawCanvas"></a>

## drawCanvas : <code>function</code>
A callback function used to draw a canvas on a canvas

**Kind**: global typedef  

| Param | Type | Description |
| --- | --- | --- |
| Img | <code>string</code> | The canvas to draw |
| x | <code>number</code> | The x coordinate to draw the canvas at |
| y | <code>number</code> | The y coordinate to draw the canvas at |

<a name="drawImageColorize"></a>

## drawImageColorize : <code>function</code>
A callback function used to draw a colorized image to a canvas

**Kind**: global typedef  

| Param | Type | Description |
| --- | --- | --- |
| src | <code>string</code> | The URL of the image to draw |
| x | <code>number</code> | The x coordinate to draw the image at |
| y | <code>number</code> | The y coordinate to draw the image at |
| color | <code>string</code> | The color to apply to the image |
| fullAlpha | <code>boolean</code> | Whether or not to apply colour to the entire image |
| alphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the image when drawing |
