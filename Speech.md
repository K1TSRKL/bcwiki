## Constants

<dl>
<dt><a href="#SpeechGagLevelLookup">SpeechGagLevelLookup</a> : <code>Object.&lt;string, number&gt;</code></dt>
<dd><p>A lookup mapping the gag effect names to their corresponding gag level numbers.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#SpeechFullEmote">SpeechFullEmote(D)</a> ⇒ <code>boolean</code></dt>
<dd><p>Analyzes a phrase to determine if it is a full emote. A full emote is a phrase wrapped in &quot;()&quot;</p>
</dd>
<dt><a href="#SpeechGetEffectGagLevel">SpeechGetEffectGagLevel(Effect)</a> ⇒ <code>number</code></dt>
<dd><p>Returns the gag level corresponding to the given effect array, or 0 if the effect array contains no gag effects</p>
</dd>
<dt><a href="#SpeechGetGagLevel">SpeechGetGagLevel(C, AssetGroup)</a> ⇒ <code>number</code></dt>
<dd><p>Gets the cumulative gag level of an asset group. Each gagging effect has a specific numeric value. The following
Effect arrays are used for the calculation, (higher on this list means that effect array will override the others):
    - Item.Property.Effect
    - Item.Asset.Effect
    - Item.Asset.Group.Effect</p>
</dd>
<dt><a href="#SpeechGarble">SpeechGarble(C, CD)</a> ⇒ <code>string</code></dt>
<dd><p>Processes the character&#39;s speech, anything between parentheses isn&#39;t touched. Effects alter the speech differently according to a character&#39;s language. Effects that can be applied are the following: gag talk, baby talk and stuttering.</p>
</dd>
<dt><a href="#SpeechStutter">SpeechStutter(C, CD)</a> ⇒ <code>string</code></dt>
<dd><p>Makes the character stutter if she has a vibrating item and/or is aroused. Stuttering based on arousal is toggled in the character&#39;s settings.</p>
</dd>
<dt><a href="#SpeechBabyTalk">SpeechBabyTalk(C, CD)</a> ⇒ <code>string</code></dt>
<dd><p>Makes the character talk like a Baby when she has drunk regression milk</p>
</dd>
</dl>

<a name="SpeechGagLevelLookup"></a>

## SpeechGagLevelLookup : <code>Object.&lt;string, number&gt;</code>
A lookup mapping the gag effect names to their corresponding gag level numbers.

**Kind**: global constant  
<a name="SpeechFullEmote"></a>

## SpeechFullEmote(D) ⇒ <code>boolean</code>
Analyzes a phrase to determine if it is a full emote. A full emote is a phrase wrapped in "()"

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the current speech phrase is a full emote (all between parentheses)  

| Param | Type | Description |
| --- | --- | --- |
| D | <code>string</code> | A phrase |

<a name="SpeechGetEffectGagLevel"></a>

## SpeechGetEffectGagLevel(Effect) ⇒ <code>number</code>
Returns the gag level corresponding to the given effect array, or 0 if the effect array contains no gag effects

**Kind**: global function  
**Returns**: <code>number</code> - - The gag level corresponding to the given effects  

| Param | Type | Description |
| --- | --- | --- |
| Effect | <code>string</code> | The effect to lookup the gag level for |

<a name="SpeechGetGagLevel"></a>

## SpeechGetGagLevel(C, AssetGroup) ⇒ <code>number</code>
Gets the cumulative gag level of an asset group. Each gagging effect has a specific numeric value. The following
Effect arrays are used for the calculation, (higher on this list means that effect array will override the others):
    - Item.Property.Effect
    - Item.Asset.Effect
    - Item.Asset.Group.Effect

**Kind**: global function  
**Returns**: <code>number</code> - - Returns the total gag effect of the character's assets  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character, whose assets are used for the check |
| AssetGroup | <code>string</code> | The name of the asset group to look through |

<a name="SpeechGarble"></a>

## SpeechGarble(C, CD) ⇒ <code>string</code>
Processes the character's speech, anything between parentheses isn't touched. Effects alter the speech differently according to a character's language. Effects that can be applied are the following: gag talk, baby talk and stuttering.

**Kind**: global function  
**Returns**: <code>string</code> - - Returns the dialog after speech effects were processed (Garbling, Stuttering, Baby talk)  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character, whose dialog might need to be altered |
| CD | <code>string</code> | The character's dialog to alter |

<a name="SpeechStutter"></a>

## SpeechStutter(C, CD) ⇒ <code>string</code>
Makes the character stutter if she has a vibrating item and/or is aroused. Stuttering based on arousal is toggled in the character's settings.

**Kind**: global function  
**Returns**: <code>string</code> - - Returns the dialog after the stuttering factor was applied  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character, whose dialog might need to be altered |
| CD | <code>string</code> | The character's dialog to alter |

<a name="SpeechBabyTalk"></a>

## SpeechBabyTalk(C, CD) ⇒ <code>string</code>
Makes the character talk like a Baby when she has drunk regression milk

**Kind**: global function  
**Returns**: <code>string</code> - - Returns the dialog after baby talk was applied  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character, whose dialog needs to be altered |
| CD | <code>string</code> | The character's dialog to alter |
