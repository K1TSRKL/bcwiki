## Functions

<dl>
<dt><a href="#LogAdd">LogAdd(NewLogName, NewLogGroup, [NewLogValue], [Push])</a> ⇒ <code>void</code></dt>
<dd><p>Adds a new entry to the player&#39;s logs, renews the value if it already exists.</p>
</dd>
<dt><a href="#LogDelete">LogDelete(NewLogName, NewLogGroup, [Push])</a> ⇒ <code>void</code></dt>
<dd><p>Deletes a log entry.</p>
</dd>
<dt><a href="#LogQuery">LogQuery(NewLogName, NewLogGroup)</a> ⇒ <code>boolean</code></dt>
<dd><p>Searches for an existing log entry.</p>
</dd>
<dt><a href="#LogValue">LogValue(NewLogName, NewLogGroup)</a> ⇒ <code>number</code> | <code>undefined</code></dt>
<dd><p>Returns the value associated to a log.</p>
</dd>
<dt><a href="#LogLoad">LogLoad(NewLog)</a> ⇒ <code>void</code></dt>
<dd><p>Loads the account log.</p>
</dd>
</dl>

<a name="LogAdd"></a>

## LogAdd(NewLogName, NewLogGroup, [NewLogValue], [Push]) ⇒ <code>void</code>
Adds a new entry to the player's logs, renews the value if it already exists.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NewLogName | <code>string</code> | The name of the log |
| NewLogGroup | <code>string</code> | The name of the log's group |
| [NewLogValue] | <code>number</code> | Value for the log as the time in ms. Is undefined if the value is permanent |
| [Push] | <code>boolean</code> | TRUE if we must push the log to the server |

<a name="LogDelete"></a>

## LogDelete(NewLogName, NewLogGroup, [Push]) ⇒ <code>void</code>
Deletes a log entry.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NewLogName | <code>string</code> | The name of the log |
| NewLogGroup | <code>string</code> | The name of the log's group |
| [Push] | <code>boolean</code> | TRUE if we must push the log to the server |

<a name="LogQuery"></a>

## LogQuery(NewLogName, NewLogGroup) ⇒ <code>boolean</code>
Searches for an existing log entry.

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if there is an existing log matching the Name/Group with no value or a value above the current time in ms.  

| Param | Type | Description |
| --- | --- | --- |
| NewLogName | <code>string</code> | The name of the log to search for |
| NewLogGroup | <code>string</code> | The name of the log's group |

<a name="LogValue"></a>

## LogValue(NewLogName, NewLogGroup) ⇒ <code>number</code> \| <code>undefined</code>
Returns the value associated to a log.

**Kind**: global function  
**Returns**: <code>number</code> \| <code>undefined</code> - - Returns the value of the log which is a date represented in ms or undefined. Returns null if no matching log is found.  

| Param | Type | Description |
| --- | --- | --- |
| NewLogName | <code>string</code> | The name of the log to query the value |
| NewLogGroup | <code>string</code> | The name of the log's group |

<a name="LogLoad"></a>

## LogLoad(NewLog) ⇒ <code>void</code>
Loads the account log.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NewLog | <code>Array.&lt;{Name: string, Group: string, Value: number}&gt;</code> | Existing logs received by the server |
