## Functions

<dl>
<dt><a href="#CharacterReset">CharacterReset(CharacterID, CharacterAssetFamily)</a> ⇒ <code>void</code></dt>
<dd><p>Loads a character into the buffer, creates it if it does not exist</p>
</dd>
<dt><a href="#CharacterRandomName">CharacterRandomName(C)</a> ⇒ <code>void</code></dt>
<dd><p>Attributes a random name for the character, does not select a name in use</p>
</dd>
<dt><a href="#CharacterBuildDialog">CharacterBuildDialog(C, CSV)</a> ⇒ <code>void</code></dt>
<dd><p>Builds the dialog objects from the character CSV file</p>
</dd>
<dt><a href="#CharacterLoadCSVDialog">CharacterLoadCSVDialog(C, [Override])</a> ⇒ <code>void</code></dt>
<dd><p>Loads the content of a CSV file to build the character dialog. Can override the current screen.</p>
</dd>
<dt><a href="#CharacterArchetypeClothes">CharacterArchetypeClothes(C, Archetype, [ForceColor])</a> ⇒ <code>void</code></dt>
<dd><p>Sets the clothes based on a character archetype</p>
</dd>
<dt><a href="#CharacterLoadNPC">CharacterLoadNPC(NPCType)</a> ⇒ <code>Character</code></dt>
<dd><p>Loads an NPC into the character array. The appearance is randomized, and a type can be provided to dress them in a given style.</p>
</dd>
<dt><a href="#CharacterOnlineRefresh">CharacterOnlineRefresh(Char, data, SourceMemberNumber)</a></dt>
<dd><p>Sets up an online character</p>
</dd>
<dt><a href="#CharacterLoadOnline">CharacterLoadOnline(data, SourceMemberNumber)</a> ⇒ <code>Character</code></dt>
<dd><p>Loads an online character and flags it for a refresh if any data was changed</p>
</dd>
<dt><a href="#CharacterDelete">CharacterDelete(NPCType)</a> ⇒ <code>void</code></dt>
<dd><p>Deletes an NPC from the buffer</p>
</dd>
<dt><a href="#CharacterDeleteAllOnline">CharacterDeleteAllOnline()</a> ⇒ <code>void</code></dt>
<dd><p>Deletes all online characters from the character array</p>
</dd>
<dt><a href="#CharacterAddPose">CharacterAddPose(C, NewPose)</a> ⇒ <code>void</code></dt>
<dd><p>Adds a pose to a character&#39;s pose list, does not add it if it&#39;s already there</p>
</dd>
<dt><a href="#CharacterLoadPose">CharacterLoadPose(C)</a> ⇒ <code>void</code></dt>
<dd><p>Refreshes the list of poses for a character. Each pose can only be found once in the pose array</p>
</dd>
<dt><a href="#CharacterAddEffect">CharacterAddEffect(C, NewEffect)</a> ⇒ <code>void</code></dt>
<dd><p>Adds an effect to a character&#39;s effect list, does not add it if it&#39;s already there</p>
</dd>
<dt><a href="#CharacterLoadEffect">CharacterLoadEffect(C)</a> ⇒ <code>void</code></dt>
<dd><p>Refreshes the list of effects for a character. Each effect can only be found once in the effect array</p>
</dd>
<dt><a href="#CharacterLoadCanvas">CharacterLoadCanvas(C)</a> ⇒ <code>void</code></dt>
<dd><p>Loads a character&#39;s canvas by sorting its appearance and drawing it.</p>
</dd>
<dt><a href="#CharacterLoadCanvasAll">CharacterLoadCanvasAll()</a> ⇒ <code>void</code></dt>
<dd><p>Reloads all character canvases in need of being redrawn.</p>
</dd>
<dt><a href="#CharacterSetCurrent">CharacterSetCurrent(C)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the current character to have a dialog with</p>
</dd>
<dt><a href="#CharacterChangeMoney">CharacterChangeMoney(C, Value)</a> ⇒ <code>void</code></dt>
<dd><p>Changes the character money and sync with the account server, factors in the cheaters version.</p>
</dd>
<dt><a href="#CharacterRefresh">CharacterRefresh(C, [Push])</a> ⇒ <code>void</code></dt>
<dd><p>Refreshes the character parameters (Effects, poses, canvas, settings, etc.)</p>
</dd>
<dt><a href="#CharacterHasNoItem">CharacterHasNoItem(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a character is wearing items (restraints), the slave collar is ignored.</p>
</dd>
<dt><a href="#CharacterIsNaked">CharacterIsNaked(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a character is naked</p>
</dd>
<dt><a href="#CharacterIsInUnderwear">CharacterIsInUnderwear(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a character is in underwear</p>
</dd>
<dt><a href="#CharacterNaked">CharacterNaked(C)</a> ⇒ <code>void</code></dt>
<dd><p>Removes all appearance items from the character</p>
</dd>
<dt><a href="#CharacterRandomUnderwear">CharacterRandomUnderwear(C)</a> ⇒ <code>void</code></dt>
<dd><p>Dresses the given character in random underwear</p>
</dd>
<dt><a href="#CharacterUnderwear">CharacterUnderwear(C, Appearance)</a> ⇒ <code>void</code></dt>
<dd><p>Removes all appearance items from the character except underwear</p>
</dd>
<dt><a href="#CharacterDress">CharacterDress(C, Appearance)</a> ⇒ <code>void</code></dt>
<dd><p>Redresses a character based on a given appearance array</p>
</dd>
<dt><a href="#CharacterRelease">CharacterRelease(C)</a> ⇒ <code>void</code></dt>
<dd><p>Removes all binding items from a given character</p>
</dd>
<dt><a href="#CharacterReleaseFromLock">CharacterReleaseFromLock(C, LockName)</a> ⇒ <code>void</code></dt>
<dd><p>Releases a character from all locks matching the given lock name</p>
</dd>
<dt><a href="#CharacterReleaseNoLock">CharacterReleaseNoLock(C)</a> ⇒ <code>void</code></dt>
<dd><p>Releases a character from all restraints that are not locked</p>
</dd>
<dt><a href="#CharacterReleaseTotal">CharacterReleaseTotal(C)</a> ⇒ <code>void</code></dt>
<dd><p>Removes all items except for clothing and slave collars from the character</p>
</dd>
<dt><a href="#CharacterGetBonus">CharacterGetBonus(C, BonusType)</a> ⇒ <code>number</code></dt>
<dd><p>Gets the bonus amount of a given type for a given character (Kidnap league)</p>
</dd>
<dt><a href="#CharacterFullRandomRestrain">CharacterFullRandomRestrain(C, [Ratio])</a></dt>
<dd><p>Restrains a character with random restraints. Some restraints are specifically disabled for randomization in their definition.</p>
</dd>
<dt><a href="#CharacterSetActivePose">CharacterSetActivePose(C, NewPose)</a> ⇒ <code>void</code></dt>
<dd><p>Sets a new pose for the character</p>
</dd>
<dt><a href="#CharacterSetFacialExpression">CharacterSetFacialExpression(C, AssetGroup, Expression, [Timer])</a> ⇒ <code>void</code></dt>
<dd><p>Sets a specific facial expression for the character&#39;s specified AssetGroup, if there&#39;s a timer, the expression will expire after it, a timed expression cannot override another one.</p>
</dd>
<dt><a href="#CharacterResetFacialExpression">CharacterResetFacialExpression(C)</a> ⇒ <code>void</code></dt>
<dd><p>Resets the character&#39;s facial expression to the default</p>
</dd>
<dt><a href="#CharacterGetCurrent">CharacterGetCurrent()</a> ⇒ <code>Character</code></dt>
<dd><p>Gets the currently selected character</p>
</dd>
<dt><a href="#CharacterCompressWardrobe">CharacterCompressWardrobe(Wardrobe)</a> ⇒ <code>string</code></dt>
<dd><p>Compresses a character wardrobe from an array to a LZ string to use less storage space</p>
</dd>
<dt><a href="#CharacterDecompressWardrobe">CharacterDecompressWardrobe(Wardrobe)</a> ⇒ <code>Array.&lt;Array.&lt;*&gt;&gt;</code></dt>
<dd><p>Decompresses a character wardrobe from a LZ String to an array if it was previously compressed (For backward compatibility with old wardrobes)</p>
</dd>
<dt><a href="#CharacterHasItemForActivity">CharacterHasItemForActivity(C, Activity)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if the character is wearing an item that allows for a specific activity</p>
</dd>
</dl>

<a name="CharacterReset"></a>

## CharacterReset(CharacterID, CharacterAssetFamily) ⇒ <code>void</code>
Loads a character into the buffer, creates it if it does not exist

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| CharacterID | <code>number</code> \| <code>string</code> | ID of the character |
| CharacterAssetFamily | <code>string</code> | Name of the asset family of the character |

<a name="CharacterRandomName"></a>

## CharacterRandomName(C) ⇒ <code>void</code>
Attributes a random name for the character, does not select a name in use

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to attribute a name |

<a name="CharacterBuildDialog"></a>

## CharacterBuildDialog(C, CSV) ⇒ <code>void</code>
Builds the dialog objects from the character CSV file

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to build the dialog |
| CSV | <code>string</code> | Content of the CSV file |

<a name="CharacterLoadCSVDialog"></a>

## CharacterLoadCSVDialog(C, [Override]) ⇒ <code>void</code>
Loads the content of a CSV file to build the character dialog. Can override the current screen.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to build the dialog objects |
| [Override] | <code>string</code> | Optional: Path to the specific CSV to build the character dialog with |

<a name="CharacterArchetypeClothes"></a>

## CharacterArchetypeClothes(C, Archetype, [ForceColor]) ⇒ <code>void</code>
Sets the clothes based on a character archetype

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to set the clothes for |
| Archetype | <code>string</code> | Archetype to determine the clothes to put on |
| [ForceColor] | <code>string</code> | Color to use for the added clothes |

<a name="CharacterLoadNPC"></a>

## CharacterLoadNPC(NPCType) ⇒ <code>Character</code>
Loads an NPC into the character array. The appearance is randomized, and a type can be provided to dress them in a given style.

**Kind**: global function  
**Returns**: <code>Character</code> - - The randomly generated NPC  

| Param | Type | Description |
| --- | --- | --- |
| NPCType | <code>string</code> | Archetype of the NPC |

<a name="CharacterOnlineRefresh"></a>

## CharacterOnlineRefresh(Char, data, SourceMemberNumber)
Sets up an online character

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| Char | <code>Character</code> | Online character to set up |
| data | <code>object</code> | Character data received |
| SourceMemberNumber | <code>number</code> | Source number of the refresh |

<a name="CharacterLoadOnline"></a>

## CharacterLoadOnline(data, SourceMemberNumber) ⇒ <code>Character</code>
Loads an online character and flags it for a refresh if any data was changed

**Kind**: global function  
**Returns**: <code>Character</code> - - The reloaded character  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> | Character data received |
| SourceMemberNumber | <code>number</code> | Source number of the load trigger |

<a name="CharacterDelete"></a>

## CharacterDelete(NPCType) ⇒ <code>void</code>
Deletes an NPC from the buffer

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NPCType | <code>string</code> | Account name of the npc to delete |

<a name="CharacterDeleteAllOnline"></a>

## CharacterDeleteAllOnline() ⇒ <code>void</code>
Deletes all online characters from the character array

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="CharacterAddPose"></a>

## CharacterAddPose(C, NewPose) ⇒ <code>void</code>
Adds a pose to a character's pose list, does not add it if it's already there

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to add a pose to its list |
| NewPose | <code>string</code> | The name of the pose to add |

<a name="CharacterLoadPose"></a>

## CharacterLoadPose(C) ⇒ <code>void</code>
Refreshes the list of poses for a character. Each pose can only be found once in the pose array

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to refresh the pose list |

<a name="CharacterAddEffect"></a>

## CharacterAddEffect(C, NewEffect) ⇒ <code>void</code>
Adds an effect to a character's effect list, does not add it if it's already there

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to add an effect to its list |
| NewEffect | <code>string</code> | The name of the effect to add |

<a name="CharacterLoadEffect"></a>

## CharacterLoadEffect(C) ⇒ <code>void</code>
Refreshes the list of effects for a character. Each effect can only be found once in the effect array

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to refresh the effect list |

<a name="CharacterLoadCanvas"></a>

## CharacterLoadCanvas(C) ⇒ <code>void</code>
Loads a character's canvas by sorting its appearance and drawing it.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to load the canvas for |

<a name="CharacterLoadCanvasAll"></a>

## CharacterLoadCanvasAll() ⇒ <code>void</code>
Reloads all character canvases in need of being redrawn.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="CharacterSetCurrent"></a>

## CharacterSetCurrent(C) ⇒ <code>void</code>
Sets the current character to have a dialog with

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to have a conversation with |

<a name="CharacterChangeMoney"></a>

## CharacterChangeMoney(C, Value) ⇒ <code>void</code>
Changes the character money and sync with the account server, factors in the cheaters version.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which we are altering the money amount |
| Value | <code>number</code> | Money to subtract/add |

<a name="CharacterRefresh"></a>

## CharacterRefresh(C, [Push]) ⇒ <code>void</code>
Refreshes the character parameters (Effects, poses, canvas, settings, etc.)

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| C | <code>Character</code> |  | Character to refresh |
| [Push] | <code>boolean</code> | <code>true</code> | Pushes the data to the server if true or null |

<a name="CharacterHasNoItem"></a>

## CharacterHasNoItem(C) ⇒ <code>boolean</code>
Checks if a character is wearing items (restraints), the slave collar is ignored.

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the given character is wearing an item  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to inspect the appearance of |

<a name="CharacterIsNaked"></a>

## CharacterIsNaked(C) ⇒ <code>boolean</code>
Checks if a character is naked

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the given character is naked  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to inspect the appearance of |

<a name="CharacterIsInUnderwear"></a>

## CharacterIsInUnderwear(C) ⇒ <code>boolean</code>
Checks if a character is in underwear

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the given character is in underwear  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to inspect the appearance of |

<a name="CharacterNaked"></a>

## CharacterNaked(C) ⇒ <code>void</code>
Removes all appearance items from the character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to undress |

<a name="CharacterRandomUnderwear"></a>

## CharacterRandomUnderwear(C) ⇒ <code>void</code>
Dresses the given character in random underwear

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to randomly dress |

<a name="CharacterUnderwear"></a>

## CharacterUnderwear(C, Appearance) ⇒ <code>void</code>
Removes all appearance items from the character except underwear

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to undress partially |
| Appearance | <code>Array.&lt;\*&gt;</code> | Appearance array to remove clothes from |

<a name="CharacterDress"></a>

## CharacterDress(C, Appearance) ⇒ <code>void</code>
Redresses a character based on a given appearance array

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to redress |
| Appearance | <code>Array.&lt;\*&gt;</code> | Appearance array to redress the character with |

<a name="CharacterRelease"></a>

## CharacterRelease(C) ⇒ <code>void</code>
Removes all binding items from a given character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to release |

<a name="CharacterReleaseFromLock"></a>

## CharacterReleaseFromLock(C, LockName) ⇒ <code>void</code>
Releases a character from all locks matching the given lock name

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to release from the lock(s) |
| LockName | <code>string</code> | Name of the lock to look for |

<a name="CharacterReleaseNoLock"></a>

## CharacterReleaseNoLock(C) ⇒ <code>void</code>
Releases a character from all restraints that are not locked

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to release |

<a name="CharacterReleaseTotal"></a>

## CharacterReleaseTotal(C) ⇒ <code>void</code>
Removes all items except for clothing and slave collars from the character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character to release |

<a name="CharacterGetBonus"></a>

## CharacterGetBonus(C, BonusType) ⇒ <code>number</code>
Gets the bonus amount of a given type for a given character (Kidnap league)

**Kind**: global function  
**Returns**: <code>number</code> - - Active bonus amount for the bonus type  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which we want to get the bonus amount |
| BonusType | <code>string</code> | Type/name of the bonus to look for |

<a name="CharacterFullRandomRestrain"></a>

## CharacterFullRandomRestrain(C, [Ratio])
Restrains a character with random restraints. Some restraints are specifically disabled for randomization in their definition.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The target character to restrain |
| [Ratio] | <code>&quot;FEW&quot;</code> \| <code>&quot;LOT&quot;</code> \| <code>&quot;ALL&quot;</code> | Amount of restraints to put on the character |

<a name="CharacterSetActivePose"></a>

## CharacterSetActivePose(C, NewPose) ⇒ <code>void</code>
Sets a new pose for the character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to set the pose |
| NewPose | <code>string</code> | Name of the pose to set as active |

<a name="CharacterSetFacialExpression"></a>

## CharacterSetFacialExpression(C, AssetGroup, Expression, [Timer]) ⇒ <code>void</code>
Sets a specific facial expression for the character's specified AssetGroup, if there's a timer, the expression will expire after it, a timed expression cannot override another one.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to set the expression of |
| AssetGroup | <code>group</code> | Asset group for the expression |
| Expression | <code>string</code> | Name of the expression to use |
| [Timer] | <code>number</code> | Optional: time the expression will last |

<a name="CharacterResetFacialExpression"></a>

## CharacterResetFacialExpression(C) ⇒ <code>void</code>
Resets the character's facial expression to the default

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which to reset the expression of |

<a name="CharacterGetCurrent"></a>

## CharacterGetCurrent() ⇒ <code>Character</code>
Gets the currently selected character

**Kind**: global function  
**Returns**: <code>Character</code> - - Currently selected character  
<a name="CharacterCompressWardrobe"></a>

## CharacterCompressWardrobe(Wardrobe) ⇒ <code>string</code>
Compresses a character wardrobe from an array to a LZ string to use less storage space

**Kind**: global function  
**Returns**: <code>string</code> - - The compressed wardrobe  

| Param | Type | Description |
| --- | --- | --- |
| Wardrobe | <code>Array.&lt;Array.&lt;\*&gt;&gt;</code> | Uncompressed wardrobe |

<a name="CharacterDecompressWardrobe"></a>

## CharacterDecompressWardrobe(Wardrobe) ⇒ <code>Array.&lt;Array.&lt;\*&gt;&gt;</code>
Decompresses a character wardrobe from a LZ String to an array if it was previously compressed (For backward compatibility with old wardrobes)

**Kind**: global function  
**Returns**: <code>Array.&lt;Array.&lt;\*&gt;&gt;</code> - - The array of wardrobe items decompressed  

| Param | Type | Description |
| --- | --- | --- |
| Wardrobe | <code>Array.&lt;Array.&lt;\*&gt;&gt;</code> \| <code>string</code> | The current wardrobe |

<a name="CharacterHasItemForActivity"></a>

## CharacterHasItemForActivity(C, Activity) ⇒ <code>boolean</code>
Checks if the character is wearing an item that allows for a specific activity

**Kind**: global function  
**Returns**: <code>boolean</code> - - TRUE if at least one item allows that activity  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to test for |
| Activity | <code>String</code> | The name of the activity that must be allowed |
