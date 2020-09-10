## Functions

<dl>
<dt><a href="#AfkTimerReset">AfkTimerReset()</a> ⇒ <code>void</code></dt>
<dd><p>Resets the timer for AFK count</p>
</dd>
<dt><a href="#AfkTimerIncrement">AfkTimerIncrement()</a> ⇒ <code>void</code></dt>
<dd><p>Increments the AFK Timer by 1. Is called from the browser&#39;s timer handler method.</p>
</dd>
<dt><a href="#AfkTimerStart">AfkTimerStart()</a> ⇒ <code>void</code></dt>
<dd><p>Registers the AfkTimerReset method for every event that is listed in AfkTimerEventsList and starts the timer count.</p>
</dd>
<dt><a href="#AfkTimerStop">AfkTimerStop()</a> ⇒ <code>void</code></dt>
<dd><p>Unregisters the AfkTimerReset method from all events listed in AfkTimerEventsList and stops the timer count</p>
</dd>
<dt><a href="#AfkTimerSetEnabled">AfkTimerSetEnabled(Enabled)</a> ⇒ <code>void</code></dt>
<dd><p>Enables or disables the afk timer. Is called, when the player changes her settings in the preferences dialog</p>
</dd>
<dt><a href="#AfkTimerSetIsAfk">AfkTimerSetIsAfk()</a> ⇒ <code>void</code></dt>
<dd><p>Sets the players&#39;s emote to the Afk symbol, when the timer runs out and saves the current Emoticon, if there is any</p>
</dd>
</dl>

<a name="AfkTimerReset"></a>

## AfkTimerReset() ⇒ <code>void</code>
Resets the timer for AFK count

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="AfkTimerIncrement"></a>

## AfkTimerIncrement() ⇒ <code>void</code>
Increments the AFK Timer by 1. Is called from the browser's timer handler method.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
**See**: [AfkTimerStart](#AfkTimerStart) and [AfkTimerStop](#AfkTimerStop) for the registering and unregistering of this function.  
<a name="AfkTimerStart"></a>

## AfkTimerStart() ⇒ <code>void</code>
Registers the AfkTimerReset method for every event that is listed in AfkTimerEventsList and starts the timer count.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="AfkTimerStop"></a>

## AfkTimerStop() ⇒ <code>void</code>
Unregisters the AfkTimerReset method from all events listed in AfkTimerEventsList and stops the timer count

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="AfkTimerSetEnabled"></a>

## AfkTimerSetEnabled(Enabled) ⇒ <code>void</code>
Enables or disables the afk timer. Is called, when the player changes her settings in the preferences dialog

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Enabled | <code>boolean</code> | Determines, wether the afk timer will be enabled (true) or disabled (false). |

<a name="AfkTimerSetIsAfk"></a>

## AfkTimerSetIsAfk() ⇒ <code>void</code>
Sets the players's emote to the Afk symbol, when the timer runs out and saves the current Emoticon, if there is any

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
