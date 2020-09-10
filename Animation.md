## Constants

<dl>
<dt><a href="#AnimationPersistentStorage">AnimationPersistentStorage</a> : <code>object</code></dt>
<dd><p>Where animation data is stored. Animation data is only managed client side, nothing should be synced.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#AnimationGetDynamicDataName">AnimationGetDynamicDataName(C, Type, [Asset])</a> ⇒ <code>string</code></dt>
<dd><p>Gets the dynamic data storage name for a given item on a given character.</p>
</dd>
<dt><a href="#AnimationPersistentDataGet">AnimationPersistentDataGet(C, Asset)</a> ⇒ <code>object</code></dt>
<dd><p>Gets the persistent data  for a given item on a given character. This method should not be called explicitly, use the Data builder passed to the dynamic drawing functions.</p>
</dd>
<dt><a href="#AnimationRequestRefreshRate">AnimationRequestRefreshRate(C, RequestedRate)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the maximum animation refresh rate for a given character.</p>
</dd>
<dt><a href="#AnimationRequestDraw">AnimationRequestDraw(C)</a> ⇒ <code>void</code></dt>
<dd><p>Marks a given character to be redrawn on the next animation refresh.</p>
</dd>
<dt><a href="#AnimationGroupGet">AnimationGroupGet(C, Asset)</a> ⇒ <code>object</code></dt>
<dd><p>Gets the group object for a given character. This method should not be called explicitly, use the Data builder passed to the dynamic drawing functions.</p>
</dd>
<dt><a href="#AnimationGroupSubscribe">AnimationGroupSubscribe(C, Asset, Name)</a> ⇒ <code>void</code></dt>
<dd><p>Marks a given asset as part of a shared data group.</p>
</dd>
<dt><a href="#AnimationGenerateTempCanvas">AnimationGenerateTempCanvas(C, A, W, H)</a> ⇒ <code>HTMLCanvasElement</code></dt>
<dd><p>Generates a temporary canvas used draw on for dynamic assets.
Careful! The width of the canvas should never be higher than 500px.</p>
</dd>
<dt><a href="#AnimationPurge">AnimationPurge(C, IncludeAll)</a> ⇒ <code>void</code></dt>
<dd><p>Purges all dynamic asset data corresponding to a given character.</p>
</dd>
</dl>

<a name="AnimationDataTypes"></a>

## AnimationDataTypes
Types of dynamic data that can be stored.

**Kind**: global enum  
**Properties**

| Name | Default |
| --- | --- |
| AssetGroup | <code>AssetGroup</code> | 
| Base | <code></code> | 
| Canvas | <code>DynamicPlayerCanvas</code> | 
| PersistentData | <code>PersistentData</code> | 
| Rebuild | <code>Rebuild</code> | 
| RefreshTime | <code>RefreshTime</code> | 
| RefreshRate | <code>RefreshRate</code> | 

<a name="AnimationPersistentStorage"></a>

## AnimationPersistentStorage : <code>object</code>
Where animation data is stored. Animation data is only managed client side, nothing should be synced.

**Kind**: global constant  
<a name="AnimationGetDynamicDataName"></a>

## AnimationGetDynamicDataName(C, Type, [Asset]) ⇒ <code>string</code>
Gets the dynamic data storage name for a given item on a given character.

**Kind**: global function  
**Returns**: <code>string</code> - - Contains the name of the persistent data key.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character wearing the animated object |
| Type | [<code>AnimationDataTypes</code>](#AnimationDataTypes) | Type of data to query |
| [Asset] | <code>Asset</code> | The animated object |

<a name="AnimationPersistentDataGet"></a>

## AnimationPersistentDataGet(C, Asset) ⇒ <code>object</code>
Gets the persistent data  for a given item on a given character. This method should not be called explicitly, use the Data builder passed to the dynamic drawing functions.

**Kind**: global function  
**Returns**: <code>object</code> - - Contains the persistent data of the animated object, returns a new empty object if it was never initialized previously.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character wearing the animated object |
| Asset | <code>Asset</code> | The animated object |

<a name="AnimationRequestRefreshRate"></a>

## AnimationRequestRefreshRate(C, RequestedRate) ⇒ <code>void</code>
Sets the maximum animation refresh rate for a given character.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character wearing the dynamic object |
| RequestedRate | <code>number</code> | The maximum refresh rate to request in ms |

<a name="AnimationRequestDraw"></a>

## AnimationRequestDraw(C) ⇒ <code>void</code>
Marks a given character to be redrawn on the next animation refresh.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character wearing the dynamic object |

<a name="AnimationGroupGet"></a>

## AnimationGroupGet(C, Asset) ⇒ <code>object</code>
Gets the group object for a given character. This method should not be called explicitly, use the Data builder passed to the dynamic drawing functions.

**Kind**: global function  
**Returns**: <code>object</code> - - Contains the persistent group data, returns a new empty object if it was never initialized previously.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character wearing the animated object |
| Asset | <code>Asset</code> | The animated object |

<a name="AnimationGroupSubscribe"></a>

## AnimationGroupSubscribe(C, Asset, Name) ⇒ <code>void</code>
Marks a given asset as part of a shared data group.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character wearing the dynamic object |
| Asset | <code>Asset</code> | The animated object |
| Name | <code>string</code> | Name of the group to subscribe to. |

<a name="AnimationGenerateTempCanvas"></a>

## AnimationGenerateTempCanvas(C, A, W, H) ⇒ <code>HTMLCanvasElement</code>
Generates a temporary canvas used draw on for dynamic assets.
Careful! The width of the canvas should never be higher than 500px.

**Kind**: global function  
**Returns**: <code>HTMLCanvasElement</code> - - The temporary canvas to use  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which the temporary canvas is |
| A | <code>Asset</code> | Asset for which the canvas is |
| W | <code>number</code> | Width of the canvas (can be changed later) |
| H | <code>number</code> | Height of the canvas (can be changed later) |

<a name="AnimationPurge"></a>

## AnimationPurge(C, IncludeAll) ⇒ <code>void</code>
Purges all dynamic asset data corresponding to a given character.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to delete the animation data of |
| IncludeAll | <code>boolean</code> | TRUE if we should delete every animation data for the given character. |
