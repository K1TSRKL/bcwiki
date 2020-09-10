## Constants

<dl>
<dt><a href="#GLDrawVertexShaderSource">GLDrawVertexShaderSource</a> : <code>string</code></dt>
<dd><p>Source used for the Vertex Shader</p>
</dd>
<dt><a href="#GLDrawFragmentShaderSource">GLDrawFragmentShaderSource</a> : <code>string</code></dt>
<dd><p>Source used for the Fragment Shader</p>
</dd>
<dt><a href="#GLDrawFragmentShaderSourceFullAlpha">GLDrawFragmentShaderSourceFullAlpha</a> : <code>string</code></dt>
<dd><p>Source used for the Full Alpha Shader</p>
</dd>
<dt><a href="#GLDrawFragmentShaderSourceHalfAlpha">GLDrawFragmentShaderSourceHalfAlpha</a> : <code>string</code></dt>
<dd><p>Source used for the Half Alpha Shader</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#GLDrawLoad">GLDrawLoad()</a> ⇒ <code>void</code></dt>
<dd><p>Loads WebGL, if not available, use the old canvas engine</p>
</dd>
<dt><a href="#GLDrawMakeGLProgam">GLDrawMakeGLProgam(gl)</a> ⇒ <code>void</code></dt>
<dd><p>Makes all programs and shaders on the GL context</p>
</dd>
<dt><a href="#GLDrawInitCharacterCanvas">GLDrawInitCharacterCanvas([canvas])</a> ⇒ <code>HTMLCanvasElement</code></dt>
<dd><p>Initializes a WebGL canvas for characters</p>
</dd>
<dt><a href="#GLDrawCreateShader">GLDrawCreateShader(gl, source, type)</a> ⇒ <code>WebGLShader</code></dt>
<dd><p>Creates a shader for the current WebGL context from a given source</p>
</dd>
<dt><a href="#GLDrawCreateProgram">GLDrawCreateProgram(gl, vertexShader, fragmentShader)</a> ⇒ <code>WebGLProgram</code></dt>
<dd><p>Creates the WebGL program from the vertex and fragment shaders</p>
</dd>
<dt><a href="#GLDrawImageBlink">GLDrawImageBlink(url, gl, dstX, dstY, color, fullAlpha, alphaMasks)</a> ⇒ <code>void</code></dt>
<dd><p>Draws an image from a given url to a WebGLRenderingContext, used when the character is blinking</p>
</dd>
<dt><a href="#GLDrawImage">GLDrawImage(url, gl, dstX, dstY, offsetX, color, fullAlpha, alphaMasks)</a> ⇒ <code>void</code></dt>
<dd><p>Draws an image from a given url to a WebGLRenderingContext</p>
</dd>
<dt><a href="#GLDraw2DCanvasBlink">GLDraw2DCanvasBlink(gl, Img, X, Y, alphaMasks)</a></dt>
<dd><p>Draws a canvas on the WebGL canvas for the blinking effect</p>
</dd>
<dt><a href="#GLDraw2DCanvas">GLDraw2DCanvas(gl, Img, X, Y, alphaMasks)</a></dt>
<dd><p>Draws a canvas on the WebGL canvas</p>
</dd>
<dt><a href="#GLDrawBingImageToTextureInfo">GLDrawBingImageToTextureInfo(gl, Img, textureInfo)</a> ⇒ <code>void</code></dt>
<dd><p>Sets texture info from image data</p>
</dd>
<dt><a href="#GLDrawLoadImage">GLDrawLoadImage(gl, url)</a> ⇒ <code>WebGLTexture</code></dt>
<dd><p>Loads image texture data</p>
</dd>
<dt><a href="#GLDrawLoadMask">GLDrawLoadMask(gl, texWidth, texHeight, offsetX, offsetY, alphaMasks)</a> ⇒ <code>WebGLTexture</code></dt>
<dd><p>Loads alpha mask data</p>
</dd>
<dt><a href="#GLDrawClearRectBlink">GLDrawClearRectBlink(gl, x, y, width, height)</a> ⇒ <code>void</code></dt>
<dd><p>Clears a rectangle on WebGLRenderingContext</p>
</dd>
<dt><a href="#GLDrawClearRect">GLDrawClearRect(gl, x, y, width, height)</a> ⇒ <code>void</code></dt>
<dd><p>Clears a rectangle on WebGLRenderingContext</p>
</dd>
<dt><a href="#GLDrawHexToRGBA">GLDrawHexToRGBA(color)</a> ⇒ <code>string</code></dt>
<dd><p>Converts a hex color to a RGBA color</p>
</dd>
<dt><a href="#GLDrawAppearanceBuild">GLDrawAppearanceBuild(C)</a> ⇒ <code>void</code></dt>
<dd><p>Creates the given character canvas with WebGL</p>
</dd>
</dl>

<a name="GLDrawVertexShaderSource"></a>

## GLDrawVertexShaderSource : <code>string</code>
Source used for the Vertex Shader

**Kind**: global constant  
<a name="GLDrawFragmentShaderSource"></a>

## GLDrawFragmentShaderSource : <code>string</code>
Source used for the Fragment Shader

**Kind**: global constant  
<a name="GLDrawFragmentShaderSourceFullAlpha"></a>

## GLDrawFragmentShaderSourceFullAlpha : <code>string</code>
Source used for the Full Alpha Shader

**Kind**: global constant  
<a name="GLDrawFragmentShaderSourceHalfAlpha"></a>

## GLDrawFragmentShaderSourceHalfAlpha : <code>string</code>
Source used for the Half Alpha Shader

**Kind**: global constant  
<a name="GLDrawLoad"></a>

## GLDrawLoad() ⇒ <code>void</code>
Loads WebGL, if not available, use the old canvas engine

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="GLDrawMakeGLProgam"></a>

## GLDrawMakeGLProgam(gl) ⇒ <code>void</code>
Makes all programs and shaders on the GL context

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGL2RenderingContext</code> | The WebGL context of the canvas |

<a name="GLDrawInitCharacterCanvas"></a>

## GLDrawInitCharacterCanvas([canvas]) ⇒ <code>HTMLCanvasElement</code>
Initializes a WebGL canvas for characters

**Kind**: global function  
**Returns**: <code>HTMLCanvasElement</code> - - The prepared canvas  

| Param | Type | Description |
| --- | --- | --- |
| [canvas] | <code>HTMLCanvasElement</code> | The canvas used to draw characters on |

<a name="GLDrawCreateShader"></a>

## GLDrawCreateShader(gl, source, type) ⇒ <code>WebGLShader</code>
Creates a shader for the current WebGL context from a given source

**Kind**: global function  
**Returns**: <code>WebGLShader</code> - - The created WebGL shader  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGL2RenderingContext</code> | WebGL context |
| source | <code>string</code> | Source of the shader to create |
| type | <code>WebGLShader</code> | The type of the shader to create |

<a name="GLDrawCreateProgram"></a>

## GLDrawCreateProgram(gl, vertexShader, fragmentShader) ⇒ <code>WebGLProgram</code>
Creates the WebGL program from the vertex and fragment shaders

**Kind**: global function  
**Returns**: <code>WebGLProgram</code> - - The created WebGL program  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGL2RenderingContext</code> | WebGL context |
| vertexShader | <code>WebGLShader</code> | The vertex shader to create the program with |
| fragmentShader | <code>WebGLShader</code> | The fragment shader to create the program with |

<a name="GLDrawImageBlink"></a>

## GLDrawImageBlink(url, gl, dstX, dstY, color, fullAlpha, alphaMasks) ⇒ <code>void</code>
Draws an image from a given url to a WebGLRenderingContext, used when the character is blinking

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| url | <code>string</code> | URL of the image to render |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| dstX | <code>number</code> | Position of the image on the X axis |
| dstY | <code>number</code> | Position of the image on the Y axis |
| color | <code>string</code> | Color of the image to draw |
| fullAlpha | <code>boolean</code> | Whether or not the full alpha should be rendered |
| alphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="GLDrawImage"></a>

## GLDrawImage(url, gl, dstX, dstY, offsetX, color, fullAlpha, alphaMasks) ⇒ <code>void</code>
Draws an image from a given url to a WebGLRenderingContext

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| url | <code>string</code> | URL of the image to render |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| dstX | <code>number</code> | Position of the image on the X axis |
| dstY | <code>number</code> | Position of the image on the Y axis |
| offsetX | <code>number</code> | Additional offset to add to the X axis (for blinking) |
| color | <code>string</code> | Color of the image to draw |
| fullAlpha | <code>boolean</code> | Whether or not the full alpha should be rendered |
| alphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="GLDraw2DCanvasBlink"></a>

## GLDraw2DCanvasBlink(gl, Img, X, Y, alphaMasks)
Draws a canvas on the WebGL canvas for the blinking effect

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| Img | <code>ImageData</code> | Canvas to get the data of |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |
| alphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="GLDraw2DCanvas"></a>

## GLDraw2DCanvas(gl, Img, X, Y, alphaMasks)
Draws a canvas on the WebGL canvas

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| Img | <code>ImageData</code> | Canvas to get the data of |
| X | <code>number</code> | Position of the image on the X axis |
| Y | <code>number</code> | Position of the image on the Y axis |
| alphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="GLDrawBingImageToTextureInfo"></a>

## GLDrawBingImageToTextureInfo(gl, Img, textureInfo) ⇒ <code>void</code>
Sets texture info from image data

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| Img | <code>ImageData</code> | Image to get the data of |
| textureInfo | <code>WebGLTexture</code> | Texture information |

<a name="GLDrawLoadImage"></a>

## GLDrawLoadImage(gl, url) ⇒ <code>WebGLTexture</code>
Loads image texture data

**Kind**: global function  
**Returns**: <code>WebGLTexture</code> - - The texture info of a given image  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| url | <code>string</code> | URL of the image |

<a name="GLDrawLoadMask"></a>

## GLDrawLoadMask(gl, texWidth, texHeight, offsetX, offsetY, alphaMasks) ⇒ <code>WebGLTexture</code>
Loads alpha mask data

**Kind**: global function  
**Returns**: <code>WebGLTexture</code> - - The WebGL texture corresponding to the mask  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGLRenderingContext</code> | The WebGL context |
| texWidth | <code>number</code> | The width of the texture to mask |
| texHeight | <code>number</code> | The height of the texture to mask |
| offsetX | <code>number</code> | The X offset at which the texture is to be drawn on the target canvas |
| offsetY | <code>number</code> | The Y offset at which the texture is to be drawn on the target canvas |
| alphaMasks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha masks to apply to the asset |

<a name="GLDrawClearRectBlink"></a>

## GLDrawClearRectBlink(gl, x, y, width, height) ⇒ <code>void</code>
Clears a rectangle on WebGLRenderingContext

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| x | <code>number</code> | Position of the image on the X axis |
| y | <code>number</code> | Position of the image on the Y axis |
| width | <code>number</code> | Width of the rectangle to clear |
| height | <code>number</code> | Height of the rectangle to clear |

<a name="GLDrawClearRect"></a>

## GLDrawClearRect(gl, x, y, width, height) ⇒ <code>void</code>
Clears a rectangle on WebGLRenderingContext

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| gl | <code>WebGLRenderingContext</code> | WebGL context |
| x | <code>number</code> | Position of the image on the X axis |
| y | <code>number</code> | Position of the image on the Y axis |
| width | <code>number</code> | Width of the rectangle to clear |
| height | <code>number</code> | Height of the rectangle to clear |

<a name="GLDrawHexToRGBA"></a>

## GLDrawHexToRGBA(color) ⇒ <code>string</code>
Converts a hex color to a RGBA color

**Kind**: global function  
**Returns**: <code>string</code> - - Converted color code  

| Param | Type | Description |
| --- | --- | --- |
| color | <code>string</code> | Hex color code to convert to RGBA |

<a name="GLDrawAppearanceBuild"></a>

## GLDrawAppearanceBuild(C) ⇒ <code>void</code>
Creates the given character canvas with WebGL

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to build the canvas for |
