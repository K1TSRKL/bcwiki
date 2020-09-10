## Functions

<dl>
<dt><a href="#TextGet">TextGet(TextTag)</a> ⇒ <code>string</code></dt>
<dd><p>Finds the text value linked to the tag in the buffer</p>
</dd>
<dt><a href="#TextBuild">TextBuild(CSV)</a> ⇒ <code>void</code></dt>
<dd><p>Builds the text objects from the CSV file, then applies the translation to the text.</p>
</dd>
<dt><a href="#TextLoad">TextLoad(TextGroup)</a> ⇒ <code>void</code></dt>
<dd><p>Loads the CSV text file of the current screen into the buffer. It will get the CSV from the cache if the file was already fetched from the server</p>
</dd>
</dl>

<a name="TextGet"></a>

## TextGet(TextTag) ⇒ <code>string</code>
Finds the text value linked to the tag in the buffer

**Kind**: global function  
**Returns**: <code>string</code> - - Returns the text associated to the tag, will return a missing tag text if the tag was not found.  

| Param | Type | Description |
| --- | --- | --- |
| TextTag | <code>string</code> | Tag for the text to find |

<a name="TextBuild"></a>

## TextBuild(CSV) ⇒ <code>void</code>
Builds the text objects from the CSV file, then applies the translation to the text.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| CSV | <code>Array.&lt;Array.&lt;string&gt;&gt;</code> | The content of the CSV file to parse (List of tag-text pairs) |

<a name="TextLoad"></a>

## TextLoad(TextGroup) ⇒ <code>void</code>
Loads the CSV text file of the current screen into the buffer. It will get the CSV from the cache if the file was already fetched from the server

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| TextGroup | <code>string</code> | Screen for which to load the CSV of |
