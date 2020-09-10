## Functions

<dl>
<dt><a href="#ActivityAllowed">ActivityAllowed()</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if the current room allows for activities. (They can only be done in certain rooms)</p>
</dd>
<dt><a href="#ActivityDictionaryLoad">ActivityDictionaryLoad()</a> ⇒ <code>void</code></dt>
<dd><p>Loads the activity dictionary that will be used throughout the game to output messages. Loads from cache first if possible.</p>
</dd>
<dt><a href="#ActivityDictionaryText">ActivityDictionaryText(KeyWord)</a> ⇒ <code>string</code></dt>
<dd><p>Searches in the dictionary for a specific keyword&#39;s text</p>
</dd>
<dt><a href="#ActivityDialogBuild">ActivityDialogBuild(C)</a> ⇒ <code>void</code></dt>
<dd><p>Builds the possible dialog activity options based on the character settings</p>
</dd>
<dt><a href="#ActivityEffect">ActivityEffect(S, C, A, Z, [count])</a> ⇒ <code>void</code></dt>
<dd><p>Calculates the effect of an activity performed on a zone</p>
</dd>
<dt><a href="#ActivityChatRoomArousalSync">ActivityChatRoomArousalSync(C)</a> ⇒ <code>void</code></dt>
<dd><p>Syncs the player arousal with everyone in chatroom</p>
</dd>
<dt><a href="#ActivitySetArousal">ActivitySetArousal(C, Progress)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the character arousal level and validates the value</p>
</dd>
<dt><a href="#ActivitySetArousalTimer">ActivitySetArousalTimer(C, Activity, Zone, Progress)</a> ⇒ <code>void</code></dt>
<dd><p>Sets an activity progress on a timer, activities are capped at MaxProgress</p>
</dd>
<dt><a href="#ActivityOrgasmProgressBar">ActivityOrgasmProgressBar(X, Y)</a> ⇒ <code>void</code></dt>
<dd><p>Draws the arousal progress bar at the given coordinates for every orgasm timer.</p>
</dd>
<dt><a href="#ActivityOrgasmWillpowerProgress">ActivityOrgasmWillpowerProgress(C)</a> ⇒ <code>void</code></dt>
<dd><p>Increases the player&#39;s willpower when resisting an orgasm.</p>
</dd>
<dt><a href="#ActivityOrgasmStart">ActivityOrgasmStart(C)</a> ⇒ <code>void</code></dt>
<dd><p>Starts an orgasm for a given character, lasts between 5 to 15 seconds and can be displayed in a chatroom.</p>
</dd>
<dt><a href="#ActivityOrgasmStop">ActivityOrgasmStop(C, Progress)</a> ⇒ <code>void</code></dt>
<dd><p>Triggered when an orgasm needs to be stopped</p>
</dd>
<dt><a href="#ActivityOrgasmGameGenerate">ActivityOrgasmGameGenerate(Progress)</a> ⇒ <code>void</code></dt>
<dd><p>Generates an orgasm button and progresses in the orgasm mini-game. Handles the resets and success/failures</p>
</dd>
<dt><a href="#ActivityOrgasmPrepare">ActivityOrgasmPrepare(C)</a> ⇒ <code>void</code></dt>
<dd><p>Triggers an orgasm for the player or an NPC which lasts from 5 to 15 seconds</p>
</dd>
<dt><a href="#ActivityExpression">ActivityExpression(C, Progress)</a> ⇒ <code>void</code></dt>
<dd><p>Sets a character&#39;s facial expressions based on their arousal level if their settings allow it.</p>
</dd>
<dt><a href="#ActivityTimerProgress">ActivityTimerProgress(C, Progress)</a> ⇒ <code>void</code></dt>
<dd><p>With time, we increase or decrease the arousal. Validates the result to keep it within 0 to 100 and triggers an orgasm when it reaches 100</p>
</dd>
<dt><a href="#ActivityRunSelf">ActivityRunSelf(Source-, Target, Activity)</a> ⇒ <code>void</code></dt>
<dd><p>Calculates the progress one character does on another right away</p>
</dd>
<dt><a href="#ActivityRun">ActivityRun(C, Activity)</a> ⇒ <code>void</code></dt>
<dd><p>Launches a sexual activity for a character and sends the chatroom message if applicable.</p>
</dd>
<dt><a href="#ActivityArousalItem">ActivityArousalItem(Source, Target, Asset)</a> ⇒ <code>void</code></dt>
<dd><p>Checks if a used asset should trigger an activity/arousal progress on the target character</p>
</dd>
<dt><a href="#ActivityFetishItemFactor">ActivityFetishItemFactor(C, Type)</a> ⇒ <code>number</code></dt>
<dd><p>Checks if the character is wearing an item tagged with the fetish type name and returns the love factor for it</p>
</dd>
<dt><a href="#ActivityFetishFactor">ActivityFetishFactor(C)</a> ⇒ <code>number</code></dt>
<dd><p>Loops in all fetishes for a character and calculates the total fetish factor</p>
</dd>
</dl>

<a name="ActivityAllowed"></a>

## ActivityAllowed() ⇒ <code>boolean</code>
Checks if the current room allows for activities. (They can only be done in certain rooms)

**Kind**: global function  
**Returns**: <code>boolean</code> - - Whether or not activities can be done  
<a name="ActivityDictionaryLoad"></a>

## ActivityDictionaryLoad() ⇒ <code>void</code>
Loads the activity dictionary that will be used throughout the game to output messages. Loads from cache first if possible.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ActivityDictionaryText"></a>

## ActivityDictionaryText(KeyWord) ⇒ <code>string</code>
Searches in the dictionary for a specific keyword's text

**Kind**: global function  
**Returns**: <code>string</code> - - Description associated to the given keyword  

| Param | Type | Description |
| --- | --- | --- |
| KeyWord | <code>string</code> | Tag of the activity description to search for |

<a name="ActivityDialogBuild"></a>

## ActivityDialogBuild(C) ⇒ <code>void</code>
Builds the possible dialog activity options based on the character settings

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for which to build the activity dialog options |

<a name="ActivityEffect"></a>

## ActivityEffect(S, C, A, Z, [count]) ⇒ <code>void</code>
Calculates the effect of an activity performed on a zone

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| S | <code>Character</code> |  | The character performing the activity |
| C | <code>Character</code> |  | The character on which the activity is performed |
| A | <code>string</code> |  | The activity performed |
| Z | <code>string</code> |  | The group/zone name where the activity was performed |
| [count] | <code>number</code> | <code>1</code> | If the activity is done repeatedly, this defines the number of times, the activity is done.  If you don't want an activity to modify arousal, set this parameter to '0' |

<a name="ActivityChatRoomArousalSync"></a>

## ActivityChatRoomArousalSync(C) ⇒ <code>void</code>
Syncs the player arousal with everyone in chatroom

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for which to sync the arousal data |

<a name="ActivitySetArousal"></a>

## ActivitySetArousal(C, Progress) ⇒ <code>void</code>
Sets the character arousal level and validates the value

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for which to set the arousal progress of |
| Progress | <code>number</code> | Progress to set for the character (Ranges from 0 to 100) |

<a name="ActivitySetArousalTimer"></a>

## ActivitySetArousalTimer(C, Activity, Zone, Progress) ⇒ <code>void</code>
Sets an activity progress on a timer, activities are capped at MaxProgress

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for which to set the timer for |
| Activity | <code>object</code> | The activity for which the timer is for |
| Zone | <code>string</code> | The target zone of the activity |
| Progress | <code>number</code> | Progress to set |

<a name="ActivityOrgasmProgressBar"></a>

## ActivityOrgasmProgressBar(X, Y) ⇒ <code>void</code>
Draws the arousal progress bar at the given coordinates for every orgasm timer.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| X | <code>number</code> | Position on the X axis |
| Y | <code>number</code> | Position on the Y axis |

<a name="ActivityOrgasmWillpowerProgress"></a>

## ActivityOrgasmWillpowerProgress(C) ⇒ <code>void</code>
Increases the player's willpower when resisting an orgasm.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character currently resisting |

<a name="ActivityOrgasmStart"></a>

## ActivityOrgasmStart(C) ⇒ <code>void</code>
Starts an orgasm for a given character, lasts between 5 to 15 seconds and can be displayed in a chatroom.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which an orgasm is starting |

<a name="ActivityOrgasmStop"></a>

## ActivityOrgasmStop(C, Progress) ⇒ <code>void</code>
Triggered when an orgasm needs to be stopped

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to stop the orgasm |
| Progress | <code>number</code> | Arousal level to set the character at once the orgasm ends |

<a name="ActivityOrgasmGameGenerate"></a>

## ActivityOrgasmGameGenerate(Progress) ⇒ <code>void</code>
Generates an orgasm button and progresses in the orgasm mini-game. Handles the resets and success/failures

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Progress | <code>number</code> | Progress of the currently running mini-game |

<a name="ActivityOrgasmPrepare"></a>

## ActivityOrgasmPrepare(C) ⇒ <code>void</code>
Triggers an orgasm for the player or an NPC which lasts from 5 to 15 seconds

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which an orgasm was triggered |

<a name="ActivityExpression"></a>

## ActivityExpression(C, Progress) ⇒ <code>void</code>
Sets a character's facial expressions based on their arousal level if their settings allow it.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to set the facial expressions |
| Progress | <code>number</code> | Current arousal progress |

<a name="ActivityTimerProgress"></a>

## ActivityTimerProgress(C, Progress) ⇒ <code>void</code>
With time, we increase or decrease the arousal. Validates the result to keep it within 0 to 100 and triggers an orgasm when it reaches 100

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which the timer is progressing |
| Progress | <code>number</code> | Progress made (from -100 to 100) |

<a name="ActivityRunSelf"></a>

## ActivityRunSelf(Source-, Target, Activity) ⇒ <code>void</code>
Calculates the progress one character does on another right away

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Source- | <code>Character</code> | The character who performed the activity |
| Target | <code>Character</code> | The character on which the activity was performed |
| Activity | <code>object</code> | The activity performed |

<a name="ActivityRun"></a>

## ActivityRun(C, Activity) ⇒ <code>void</code>
Launches a sexual activity for a character and sends the chatroom message if applicable.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character on which the activity was triggered |
| Activity | <code>object</code> | Activity performed |

<a name="ActivityArousalItem"></a>

## ActivityArousalItem(Source, Target, Asset) ⇒ <code>void</code>
Checks if a used asset should trigger an activity/arousal progress on the target character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Source | <code>Character</code> | The character who used the item |
| Target | <code>Character</code> | The character on which the item was used |
| Asset | <code>object</code> | Asset used |

<a name="ActivityFetishItemFactor"></a>

## ActivityFetishItemFactor(C, Type) ⇒ <code>number</code>
Checks if the character is wearing an item tagged with the fetish type name and returns the love factor for it

**Kind**: global function  
**Returns**: <code>number</code> - - From -2 (hate it) to 2 (adore it) based on the player preferences  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to validate |
| Type | <code>string</code> | The fetish type name |

<a name="ActivityFetishFactor"></a>

## ActivityFetishFactor(C) ⇒ <code>number</code>
Loops in all fetishes for a character and calculates the total fetish factor

**Kind**: global function  
**Returns**: <code>number</code> - - The negative/positive number will have negative/positive impact on arousal  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to validate |
