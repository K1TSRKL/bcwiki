## Functions

<dl>
<dt><a href="#TimerToString">TimerToString(T)</a> ⇒ <code>string</code></dt>
<dd><p>Returns a string of the time remaining on a given timer</p>
</dd>
<dt><a href="#TimerHourToString">TimerHourToString(T)</a> ⇒ <code>string</code></dt>
<dd><p>Returns a string of the time remaining on a given timer (Hours and minutes only)</p>
</dd>
<dt><a href="#TimerInventoryRemove">TimerInventoryRemove()</a> ⇒ <code>void</code></dt>
<dd><p>Check if we must remove items from characters. (Expressions, items being removed, locks, etc.)</p>
</dd>
<dt><a href="#TimerInventoryRemoveSet">TimerInventoryRemoveSet(C, AssetGroup, Timer)</a> ⇒ <code>void</code></dt>
<dd><p>Sets a remove timer in seconds for a specific item part / body part</p>
</dd>
<dt><a href="#TimerPrivateOwnerBeep">TimerPrivateOwnerBeep()</a> ⇒ <code>void</code></dt>
<dd><p>Random trigger for the NPC owner in a private room. If possible, when triggered it will beep the player anywhere in the club, the player has 2 minutes to get back to her</p>
</dd>
<dt><a href="#TimerProcess">TimerProcess(Timestamp)</a> ⇒ <code>void</code></dt>
<dd><p>Main timer process</p>
</dd>
<dt><a href="#TimermsToTime">TimermsToTime(s)</a> ⇒</dt>
<dd><p>Returns a string of the time remaining on a given timer (Hours, minutes, seconds)</p>
</dd>
</dl>

<a name="TimerToString"></a>

## TimerToString(T) ⇒ <code>string</code>
Returns a string of the time remaining on a given timer

**Kind**: global function  
**Returns**: <code>string</code> - - The time string in the DD:HH:MM:SS format (Days and hours not displayed if it contains none)  

| Param | Type | Description |
| --- | --- | --- |
| T | <code>number</code> | Time to convert to a string in ms |

<a name="TimerHourToString"></a>

## TimerHourToString(T) ⇒ <code>string</code>
Returns a string of the time remaining on a given timer (Hours and minutes only)

**Kind**: global function  
**Returns**: <code>string</code> - - The time string in the HH:MM format  

| Param | Type | Description |
| --- | --- | --- |
| T | <code>number</code> | Time to convert to a string in ms |

<a name="TimerInventoryRemove"></a>

## TimerInventoryRemove() ⇒ <code>void</code>
Check if we must remove items from characters. (Expressions, items being removed, locks, etc.)

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="TimerInventoryRemoveSet"></a>

## TimerInventoryRemoveSet(C, AssetGroup, Timer) ⇒ <code>void</code>
Sets a remove timer in seconds for a specific item part / body part

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which we are removing an item |
| AssetGroup | <code>string</code> | Group targeted by the removal |
| Timer | <code>number</code> | Seconds it takes to remove the item |

<a name="TimerPrivateOwnerBeep"></a>

## TimerPrivateOwnerBeep() ⇒ <code>void</code>
Random trigger for the NPC owner in a private room. If possible, when triggered it will beep the player anywhere in the club, the player has 2 minutes to get back to her

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="TimerProcess"></a>

## TimerProcess(Timestamp) ⇒ <code>void</code>
Main timer process

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Timestamp | <code>number</code> | Time in ms of the time when the function was called |

<a name="TimermsToTime"></a>

## TimermsToTime(s) ⇒
Returns a string of the time remaining on a given timer (Hours, minutes, seconds)

**Kind**: global function  
**Returns**: -  The time string in the HH:MM:SS format  

| Param | Type | Description |
| --- | --- | --- |
| s | <code>number</code> | Time to convert to a string in ms |
