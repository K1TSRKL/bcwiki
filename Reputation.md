## Functions

<dl>
<dt><a href="#ReputationChange">ReputationChange(RepType, RepValue, [Push])</a> ⇒ <code>void</code></dt>
<dd><p>Alters a given reputation value for the player</p>
</dd>
<dt><a href="#ReputationLoad">ReputationLoad(NewRep)</a> ⇒ <code>void</code></dt>
<dd><p>Loads the reputation data from the server</p>
</dd>
<dt><a href="#ReputationGet">ReputationGet(RepType)</a> ⇒ <code>number</code></dt>
<dd><p>Returns a specific reputation value for the player</p>
</dd>
<dt><a href="#ReputationCharacterGet">ReputationCharacterGet(C, RepType)</a> ⇒ <code>number</code></dt>
<dd><p>Returns a specific reputation value for a given character</p>
</dd>
<dt><a href="#ReputationProgress">ReputationProgress(RepType, Value)</a> ⇒ <code>void</code></dt>
<dd><p>Alter the reputation progress by a factor. The higher the rep, the slower it gets, a reputation is easier to break than to build. Takes the cheater version factor into account.</p>
</dd>
</dl>

<a name="ReputationChange"></a>

## ReputationChange(RepType, RepValue, [Push]) ⇒ <code>void</code>
Alters a given reputation value for the player

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| RepType | <code>string</code> |  | The name/type of the reputation to alter |
| RepValue | <code>number</code> |  | Reputation to add/subtract to the current reputation value. |
| [Push] | <code>boolean</code> | <code>true</code> | Pushes the reputation to the server if TRUE |

<a name="ReputationLoad"></a>

## ReputationLoad(NewRep) ⇒ <code>void</code>
Loads the reputation data from the server

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NewRep | <code>Array.&lt;{Type: string, Value: number}&gt;</code> | The array of reputation-value pairs to load for the current player |

<a name="ReputationGet"></a>

## ReputationGet(RepType) ⇒ <code>number</code>
Returns a specific reputation value for the player

**Kind**: global function  
**Returns**: <code>number</code> - - Returns the value of the reputation. It can range from 100 to -100, and it defaults to 0 if the player never earned this type of reputation before.  

| Param | Type | Description |
| --- | --- | --- |
| RepType | <code>string</code> | Type/name of the reputation to get the value of. |

<a name="ReputationCharacterGet"></a>

## ReputationCharacterGet(C, RepType) ⇒ <code>number</code>
Returns a specific reputation value for a given character

**Kind**: global function  
**Returns**: <code>number</code> - - Returns the value of the reputation. It can range from 100 to -100, and it defaults to 0 if the given character never earned this type of reputation before.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to get the reputation for. |
| RepType | <code>string</code> | Type/name of the reputation to get the value of. |

<a name="ReputationProgress"></a>

## ReputationProgress(RepType, Value) ⇒ <code>void</code>
Alter the reputation progress by a factor. The higher the rep, the slower it gets, a reputation is easier to break than to build. Takes the cheater version factor into account.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| RepType | <code>string</code> | Type/name of the reputation |
| Value | <code>number</code> | Value of the reputation change before the factor is applied |
