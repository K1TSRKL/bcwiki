## Constants

<dl>
<dt><a href="#NPCTrait">NPCTrait</a> : <code>Array.&lt;Array.&lt;string&gt;&gt;</code></dt>
<dd><p>List for all possible pairs of NPC traits. A pair defines opposites.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#NPCTraitSet">NPCTraitSet(C, TraitName, TraitValue)</a> ⇒ <code>void</code></dt>
<dd><p>Sets a specific trait for a NPC</p>
</dd>
<dt><a href="#NPCTraitGenerate">NPCTraitGenerate(C)</a> ⇒ <code>void</code></dt>
<dd><p>Generate random traits for a NPC (70% odds for each traits, can switch on both sides, strength is from 1 to 100). Will generate at least one trait.</p>
</dd>
<dt><a href="#NPCTraitReverse">NPCTraitReverse(Trait)</a> ⇒ <code>string</code></dt>
<dd><p>Get the opposite trait of a specified trait.</p>
</dd>
<dt><a href="#NPCTraitGetOptionValue">NPCTraitGetOptionValue(Dialog, NPCTrait)</a> ⇒ <code>number</code></dt>
<dd><p>Returns the weight value of the specified option (The higher the value, the higher the chances the option will be picked, an opposite trait will always result as an option that&#39;s not picked)</p>
</dd>
<dt><a href="#NPCTraitKeepBestOption">NPCTraitKeepBestOption(C, Group)</a> ⇒ <code>void</code></dt>
<dd><p>Finds and keeps the best possible option for a specified NPC dialog group. A group is a list of similar options where each option is influenced by a specified trait.</p>
</dd>
<dt><a href="#NPCTraitDialog">NPCTraitDialog(C)</a> ⇒ <code>void</code></dt>
<dd><p>Picks the dialog group option that fits mosts with the NPC traits</p>
</dd>
<dt><a href="#NPCArousal">NPCArousal(C)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the arousal settings for a NPC if it&#39;s not already done</p>
</dd>
<dt><a href="#NPCTraitGet">NPCTraitGet(C, TraitType)</a> ⇒ <code>number</code></dt>
<dd><p>Returns the trait value of an NPC. If the opposite trait is found, it will return a negative value.</p>
</dd>
<dt><a href="#NPCEventAdd">NPCEventAdd(C, EventName, EventValue)</a> ⇒ <code>void</code></dt>
<dd><p>Adds a new event in a specified NPC log or updates an existing event if it was previously logged.</p>
</dd>
<dt><a href="#NPCEventDelete">NPCEventDelete(C, EventName)</a> ⇒ <code>void</code></dt>
<dd><p>Deletes a specified NPC event from the log</p>
</dd>
<dt><a href="#NPCEventGet">NPCEventGet(C, EventName)</a> ⇒ <code>number</code></dt>
<dd><p>Returns a specified NPC event value.</p>
</dd>
<dt><a href="#NPCLongEventDelay">NPCLongEventDelay(C)</a> ⇒ <code>number</code></dt>
<dd><p>For longer events like a collaring, the serious trait will dictate the time (1 day if playful, 3 days if nothing, 7 days if serious)</p>
</dd>
<dt><a href="#NPCLongLoverEventDelay">NPCLongLoverEventDelay(C)</a> ⇒ <code>number</code></dt>
<dd><p>The horny / frigid trait comes into play when a NPC decides if it can take the player as a lover. (1 week if horny, 2 weeks if nothing, 4 weeks if frigid)</p>
</dd>
<dt><a href="#NPCLoveChange">NPCLoveChange(C, LoveFactor)</a> ⇒ <code>void</code></dt>
<dd><p>Changes the love factor for a specified NPC, will stay within the -100 to 100 range</p>
</dd>
<dt><a href="#NPCInteraction">NPCInteraction()</a> ⇒ <code>void</code></dt>
<dd><p>Raises the love factor progressively with interaction time</p>
</dd>
</dl>

<a name="NPCTrait"></a>

## NPCTrait : <code>Array.&lt;Array.&lt;string&gt;&gt;</code>
List for all possible pairs of NPC traits. A pair defines opposites.

**Kind**: global constant  
<a name="NPCTraitSet"></a>

## NPCTraitSet(C, TraitName, TraitValue) ⇒ <code>void</code>
Sets a specific trait for a NPC

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to set the trait for |
| TraitName | <code>string</code> | Name of the trait to set |
| TraitValue | <code>number</code> | Value of the trait to set |

<a name="NPCTraitGenerate"></a>

## NPCTraitGenerate(C) ⇒ <code>void</code>
Generate random traits for a NPC (70% odds for each traits, can switch on both sides, strength is from 1 to 100). Will generate at least one trait.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to generate the trait for |

<a name="NPCTraitReverse"></a>

## NPCTraitReverse(Trait) ⇒ <code>string</code>
Get the opposite trait of a specified trait.

**Kind**: global function  
**Returns**: <code>string</code> - - Name of the opposite trait.  

| Param | Type | Description |
| --- | --- | --- |
| Trait | <code>string</code> | Name of the trait to find the opposite of. |

<a name="NPCTraitGetOptionValue"></a>

## NPCTraitGetOptionValue(Dialog, NPCTrait) ⇒ <code>number</code>
Returns the weight value of the specified option (The higher the value, the higher the chances the option will be picked, an opposite trait will always result as an option that's not picked)

**Kind**: global function  
**Returns**: <code>number</code> - - Weight of the dialog option  

| Param | Type | Description |
| --- | --- | --- |
| Dialog | <code>string</code> | Specified dialog line. |
| NPCTrait | <code>string</code> | Trait to influence the weight |

<a name="NPCTraitKeepBestOption"></a>

## NPCTraitKeepBestOption(C, Group) ⇒ <code>void</code>
Finds and keeps the best possible option for a specified NPC dialog group. A group is a list of similar options where each option is influenced by a specified trait.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to get the dialog of |
| Group | <code>string</code> | Name of the dialog group to look for |

<a name="NPCTraitDialog"></a>

## NPCTraitDialog(C) ⇒ <code>void</code>
Picks the dialog group option that fits mosts with the NPC traits

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to get the dialog options of |

<a name="NPCArousal"></a>

## NPCArousal(C) ⇒ <code>void</code>
Sets the arousal settings for a NPC if it's not already done

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to set the arousal stats of |

<a name="NPCTraitGet"></a>

## NPCTraitGet(C, TraitType) ⇒ <code>number</code>
Returns the trait value of an NPC. If the opposite trait is found, it will return a negative value.

**Kind**: global function  
**Returns**: <code>number</code> - - Value of the trait, returns 0 if it was never set.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to get the trait of |
| TraitType | <code>string</code> | Name of the trait to get the value of |

<a name="NPCEventAdd"></a>

## NPCEventAdd(C, EventName, EventValue) ⇒ <code>void</code>
Adds a new event in a specified NPC log or updates an existing event if it was previously logged.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC for which to add the event to |
| EventName | <code>string</code> | Name of the even to add |
| EventValue | <code>number</code> | Value of the even to add (time in ms) |

<a name="NPCEventDelete"></a>

## NPCEventDelete(C, EventName) ⇒ <code>void</code>
Deletes a specified NPC event from the log

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC for which to delete the event |
| EventName | <code>string</code> | Name of the even to delete |

<a name="NPCEventGet"></a>

## NPCEventGet(C, EventName) ⇒ <code>number</code>
Returns a specified NPC event value.

**Kind**: global function  
**Returns**: <code>number</code> - - Value of the event as the time in ms, returns 0 if it was never logged  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to get the event value of |
| EventName | <code>string</code> | Name of the even to get the value of |

<a name="NPCLongEventDelay"></a>

## NPCLongEventDelay(C) ⇒ <code>number</code>
For longer events like a collaring, the serious trait will dictate the time (1 day if playful, 3 days if nothing, 7 days if serious)

**Kind**: global function  
**Returns**: <code>number</code> - - Delay required for the event.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to get the event delay of |

<a name="NPCLongLoverEventDelay"></a>

## NPCLongLoverEventDelay(C) ⇒ <code>number</code>
The horny / frigid trait comes into play when a NPC decides if it can take the player as a lover. (1 week if horny, 2 weeks if nothing, 4 weeks if frigid)

**Kind**: global function  
**Returns**: <code>number</code> - - Delay required for the lover event.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to get the event delay of |

<a name="NPCLoveChange"></a>

## NPCLoveChange(C, LoveFactor) ⇒ <code>void</code>
Changes the love factor for a specified NPC, will stay within the -100 to 100 range

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | NPC to change the love factor of |
| LoveFactor | <code>number</code> | Amount to add to the current love factor (can be negative). |

<a name="NPCInteraction"></a>

## NPCInteraction() ⇒ <code>void</code>
Raises the love factor progressively with interaction time

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
