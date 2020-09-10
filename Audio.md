## Functions

<dl>
<dt><a href="#AudioPlayInstantSound">AudioPlayInstantSound(src, volume)</a> ⇒ <code>void</code></dt>
<dd><p>Plays a sound at a given volume</p>
</dd>
<dt><a href="#AudioDialogStart">AudioDialogStart(SourceFile)</a> ⇒ <code>void</code></dt>
<dd><p>Begins to play a sound when applying/removing an item</p>
</dd>
<dt><a href="#AudioDialogStop">AudioDialogStop()</a> ⇒ <code>void</code></dt>
<dd><p>Stops playing the sound when done applying/removing an item</p>
</dd>
<dt><a href="#AudioPlayContent">AudioPlayContent(data)</a> ⇒ <code>void</code></dt>
<dd><p>Takes the received data dictionary content and identifies the audio to be played</p>
</dd>
</dl>

<a name="AudioPlayInstantSound"></a>

## AudioPlayInstantSound(src, volume) ⇒ <code>void</code>
Plays a sound at a given volume

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| src | <code>string</code> | Source of the audio file to play |
| volume | <code>number</code> | Volume of the audio in percentage (ranges from 0 to 1) |

<a name="AudioDialogStart"></a>

## AudioDialogStart(SourceFile) ⇒ <code>void</code>
Begins to play a sound when applying/removing an item

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| SourceFile | <code>string</code> | Source of the audio file to play |

<a name="AudioDialogStop"></a>

## AudioDialogStop() ⇒ <code>void</code>
Stops playing the sound when done applying/removing an item

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="AudioPlayContent"></a>

## AudioPlayContent(data) ⇒ <code>void</code>
Takes the received data dictionary content and identifies the audio to be played

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> | Data received |
