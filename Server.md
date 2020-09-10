## Functions

<dl>
<dt><a href="#ServerInit">ServerInit()</a></dt>
<dd><p>Loads the server by attaching the socket events and their respective callbacks</p>
</dd>
<dt><a href="#ServerSetConnected">ServerSetConnected(connected, errorMessage)</a></dt>
<dd><p>Sets the connection status of the server and updates the login page message</p>
</dd>
<dt><a href="#ServerConnect">ServerConnect()</a></dt>
<dd><p>Callback when receiving a &quot;connect&quot; event on the socket - this will be called on initial connection and on successful reconnects.</p>
</dd>
<dt><a href="#ServerReconnecting">ServerReconnecting()</a></dt>
<dd><p>Callback when receiving a &quot;reconnecting&quot; event on the socket - this is called when socket.io initiates a retry after a failed connection attempt.</p>
</dd>
<dt><a href="#ServerInfo">ServerInfo(data)</a> ⇒ <code>void</code></dt>
<dd><p>Callback used to parse received information related to the server</p>
</dd>
<dt><a href="#ServerDisconnect">ServerDisconnect(data)</a> ⇒ <code>void</code></dt>
<dd><p>Callback used when we are disconnected from the server, try to enter the reconnection mode (relog screen) if the user was logged in</p>
</dd>
<dt><a href="#ServerSend">ServerSend()</a></dt>
<dd><p>Sends a message with the given data to the server via socket.emit</p>
</dd>
<dt><a href="#ServerPlayerSync">ServerPlayerSync()</a> ⇒ <code>void</code></dt>
<dd><p>Syncs Money, owner name and lover name with the server</p>
</dd>
<dt><a href="#ServerPlayerInventorySync">ServerPlayerInventorySync()</a> ⇒ <code>void</code></dt>
<dd><p>Syncs the full player inventory to the server. The inventory is a stringified object compressed with LZString</p>
</dd>
<dt><a href="#ServerPlayerLogSync">ServerPlayerLogSync()</a> ⇒ <code>void</code></dt>
<dd><p>Syncs the full player log array to the server.</p>
</dd>
<dt><a href="#ServerPlayerReputationSync">ServerPlayerReputationSync()</a> ⇒ <code>void</code></dt>
<dd><p>Syncs the full player reputation array to the server.</p>
</dd>
<dt><a href="#ServerPlayerSkillSync">ServerPlayerSkillSync()</a> ⇒ <code>void</code></dt>
<dd><p>Syncs the full player skill array to the server.</p>
</dd>
<dt><a href="#ServerAppearanceBundle">ServerAppearanceBundle(Appearance)</a> ⇒ <code><a href="#AppearanceBundle">AppearanceBundle</a></code></dt>
<dd><p>Prepares an appearance bundle so we can push it to the server. It minimizes it by keeping only the necessary information. (Asset name, group name, color, properties and difficulty)</p>
</dd>
<dt><a href="#ServerValidateProperties">ServerValidateProperties(C, Item)</a> ⇒ <code>void</code></dt>
<dd><p>Validates the properties for a given item to prevent griefing in multiplayer</p>
</dd>
<dt><a href="#ServerAppearanceLoadFromBundle">ServerAppearanceLoadFromBundle(C, AssetFamily, Bundle, SourceMemberNumber)</a> ⇒ <code>void</code></dt>
<dd><p>Loads the appearance assets from a server bundle that only contains the main info (no asset) and validates their properties to prevent griefing and respecting permissions in multiplayer</p>
</dd>
<dt><a href="#ServerPlayerAppearanceSync">ServerPlayerAppearanceSync()</a> ⇒ <code>void</code></dt>
<dd><p>Syncs the player appearance with the server</p>
</dd>
<dt><a href="#ServerPrivateCharacterSync">ServerPrivateCharacterSync()</a> ⇒ <code>void</code></dt>
<dd><p>Syncs all the private room characters with the server</p>
</dd>
<dt><a href="#ServerAccountQueryResult">ServerAccountQueryResult(data)</a> ⇒ <code>void</code></dt>
<dd><p>Callback used to parse received information related to a query made by the player such as viewing their online friends or current email status</p>
</dd>
<dt><a href="#ServerAccountBeep">ServerAccountBeep(data)</a> ⇒ <code>void</code></dt>
<dd><p>Callback used to parse received information related to ta beep from another account</p>
</dd>
<dt><a href="#ServerDrawBeep">ServerDrawBeep()</a></dt>
<dd><p>Draws the last beep sent by the server if the timer is still valid, used during the drawing process</p>
</dd>
<dt><a href="#ServerAccountOwnership">ServerAccountOwnership(data)</a> ⇒ <code>void</code></dt>
<dd><p>Callback used to parse received information related to the player ownership data</p>
</dd>
<dt><a href="#ServerAccountLovership">ServerAccountLovership(data)</a> ⇒ <code>void</code></dt>
<dd><p>Callback used to parse received information related to the player lovership data</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#Item">Item</a> : <code>Object</code></dt>
<dd><p>An item is a pair of asset and its dynamic properties that define a worn asset.</p>
</dd>
<dt><a href="#AppearanceArray">AppearanceArray</a> : <code><a href="#Item">Array.&lt;Item&gt;</a></code></dt>
<dd><p>An appearance array is an array of object defining each appearance item of a character in all of its details.</p>
</dd>
<dt><a href="#AppearanceBundle">AppearanceBundle</a> : <code>Array.&lt;{Group: string, Name: string, Difficulty: (number|undefined), Color: (string|undefined), Property: (object|undefined)}&gt;</code></dt>
<dd><p>An appearance bundle is an array of object defining each appearance item of a character. It&#39;s a minified version of the normal appearance array</p>
</dd>
</dl>

<a name="ServerInit"></a>

## ServerInit()
Loads the server by attaching the socket events and their respective callbacks

**Kind**: global function  
<a name="ServerSetConnected"></a>

## ServerSetConnected(connected, errorMessage)
Sets the connection status of the server and updates the login page message

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| connected | <code>boolean</code> | whether or not the websocket connection to the server has been established successfully |
| errorMessage | <code>string</code> | the error message to display if not connected |

<a name="ServerConnect"></a>

## ServerConnect()
Callback when receiving a "connect" event on the socket - this will be called on initial connection and on successful reconnects.

**Kind**: global function  
<a name="ServerReconnecting"></a>

## ServerReconnecting()
Callback when receiving a "reconnecting" event on the socket - this is called when socket.io initiates a retry after a failed connection attempt.

**Kind**: global function  
<a name="ServerInfo"></a>

## ServerInfo(data) ⇒ <code>void</code>
Callback used to parse received information related to the server

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>Object</code> | Data object containing the server information |

<a name="ServerDisconnect"></a>

## ServerDisconnect(data) ⇒ <code>void</code>
Callback used when we are disconnected from the server, try to enter the reconnection mode (relog screen) if the user was logged in

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>\*</code> | Error to log |

<a name="ServerSend"></a>

## ServerSend()
Sends a message with the given data to the server via socket.emit

**Kind**: global function  
<a name="ServerPlayerSync"></a>

## ServerPlayerSync() ⇒ <code>void</code>
Syncs Money, owner name and lover name with the server

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ServerPlayerInventorySync"></a>

## ServerPlayerInventorySync() ⇒ <code>void</code>
Syncs the full player inventory to the server. The inventory is a stringified object compressed with LZString

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ServerPlayerLogSync"></a>

## ServerPlayerLogSync() ⇒ <code>void</code>
Syncs the full player log array to the server.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ServerPlayerReputationSync"></a>

## ServerPlayerReputationSync() ⇒ <code>void</code>
Syncs the full player reputation array to the server.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ServerPlayerSkillSync"></a>

## ServerPlayerSkillSync() ⇒ <code>void</code>
Syncs the full player skill array to the server.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ServerAppearanceBundle"></a>

## ServerAppearanceBundle(Appearance) ⇒ [<code>AppearanceBundle</code>](#AppearanceBundle)
Prepares an appearance bundle so we can push it to the server. It minimizes it by keeping only the necessary information. (Asset name, group name, color, properties and difficulty)

**Kind**: global function  
**Returns**: [<code>AppearanceBundle</code>](#AppearanceBundle) - - The appearance bundle created from the given appearance array  

| Param | Type | Description |
| --- | --- | --- |
| Appearance | [<code>AppearanceArray</code>](#AppearanceArray) | The appearance array to bundle |

<a name="ServerValidateProperties"></a>

## ServerValidateProperties(C, Item) ⇒ <code>void</code>
Validates the properties for a given item to prevent griefing in multiplayer

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character the item will be applied to |
| Item | [<code>Item</code>](#Item) | The item for which to validate the properties |

<a name="ServerAppearanceLoadFromBundle"></a>

## ServerAppearanceLoadFromBundle(C, AssetFamily, Bundle, SourceMemberNumber) ⇒ <code>void</code>
Loads the appearance assets from a server bundle that only contains the main info (no asset) and validates their properties to prevent griefing and respecting permissions in multiplayer

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to load the appearance |
| AssetFamily | <code>string</code> | Family of assets used for the appearance array |
| Bundle | [<code>AppearanceBundle</code>](#AppearanceBundle) | Bundled appearance |
| SourceMemberNumber | <code>number</code> | Member number of the user who triggered the change |

<a name="ServerPlayerAppearanceSync"></a>

## ServerPlayerAppearanceSync() ⇒ <code>void</code>
Syncs the player appearance with the server

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ServerPrivateCharacterSync"></a>

## ServerPrivateCharacterSync() ⇒ <code>void</code>
Syncs all the private room characters with the server

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="ServerAccountQueryResult"></a>

## ServerAccountQueryResult(data) ⇒ <code>void</code>
Callback used to parse received information related to a query made by the player such as viewing their online friends or current email status

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> | Data object containing the query data |

<a name="ServerAccountBeep"></a>

## ServerAccountBeep(data) ⇒ <code>void</code>
Callback used to parse received information related to ta beep from another account

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> | Data object containing the beep object which contain at the very least a name and a member number |

<a name="ServerDrawBeep"></a>

## ServerDrawBeep()
Draws the last beep sent by the server if the timer is still valid, used during the drawing process

**Kind**: global function  
<a name="ServerAccountOwnership"></a>

## ServerAccountOwnership(data) ⇒ <code>void</code>
Callback used to parse received information related to the player ownership data

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> | Data object containing the Owner name and Ownership object |

<a name="ServerAccountLovership"></a>

## ServerAccountLovership(data) ⇒ <code>void</code>
Callback used to parse received information related to the player lovership data

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> | Data object containing the Lovership array |

<a name="Item"></a>

## Item : <code>Object</code>
An item is a pair of asset and its dynamic properties that define a worn asset.

**Kind**: global typedef  
<a name="AppearanceArray"></a>

## AppearanceArray : [<code>Array.&lt;Item&gt;</code>](#Item)
An appearance array is an array of object defining each appearance item of a character in all of its details.

**Kind**: global typedef  
<a name="AppearanceBundle"></a>

## AppearanceBundle : <code>Array.&lt;{Group: string, Name: string, Difficulty: (number\|undefined), Color: (string\|undefined), Property: (object\|undefined)}&gt;</code>
An appearance bundle is an array of object defining each appearance item of a character. It's a minified version of the normal appearance array

**Kind**: global typedef  
