## Functions

<dl>
<dt><a href="#InventoryAdd">InventoryAdd(C, NewItemName, NewItemGroup, Push)</a></dt>
<dd><p>Add a new item by group &amp; name to character inventory</p>
</dd>
<dt><a href="#InventoryAddMany">InventoryAddMany(C, NewItems, Push)</a></dt>
<dd><p>Adds multiple new items by group &amp; name to the character inventory</p>
</dd>
<dt><a href="#InventoryItemCreate">InventoryItemCreate(C, Group, Name)</a> ⇒ <code>Item</code></dt>
<dd><p>Creates a new item for a character based on asset group and name</p>
</dd>
<dt><a href="#InventoryDelete">InventoryDelete(C, DelItemName, DelItemGroup, Push)</a></dt>
<dd><p>Deletes an item from the character inventory</p>
</dd>
<dt><a href="#InventoryLoad">InventoryLoad(C, Inventory)</a></dt>
<dd><p>Loads the current inventory for a character, can be loaded from an object of Name/Group or a compressed array using LZString</p>
</dd>
<dt><a href="#InventoryAvailable">InventoryAvailable(C, InventoryName, InventoryGroup)</a></dt>
<dd><p>Checks if the character has the inventory available</p>
</dd>
<dt><a href="#InventoryPrerequisiteMessage">InventoryPrerequisiteMessage(C, Prerequisite)</a> ⇒ <code>String</code></dt>
<dd><p>Returns an error message if a prerequisite clashes with the character items and clothes</p>
</dd>
<dt><a href="#InventoryAllow">InventoryAllow(C, Prerequisite, SetDialog)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if we can add the item, no other items must block that prerequisite</p>
</dd>
<dt><a href="#InventoryGet">InventoryGet(C, AssetGroup)</a> ⇒ <code>AppearanceItem</code></dt>
<dd><p>Gets the current item / cloth worn a specific area (AssetGroup)</p>
</dd>
<dt><a href="#InventoryWear">InventoryWear(C, AssetName, AssetGroup, ItemColor, Difficulty, MemberNumber)</a></dt>
<dd><p>Makes the character wear an item on a body area</p>
</dd>
<dt><a href="#InventorySetDifficulty">InventorySetDifficulty(C, AssetGroup, Difficulty)</a></dt>
<dd><p>Sets the difficulty to remove an item for a body area</p>
</dd>
<dt><a href="#InventoryLocked">InventoryLocked(C, AssetGroup, CheckProperties)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if there&#39;s already a locked item at a given body area</p>
</dd>
<dt><a href="#InventoryWearRandom">InventoryWearRandom(C, GroupName, Difficulty)</a></dt>
<dd><p>Makes the character wear a random item from a body area, the character doesn&#39;t need to own the item</p>
</dd>
<dt><a href="#InventoryRemove">InventoryRemove(C, AssetGroup)</a></dt>
<dd><p>Removes a specific item from a character body area</p>
</dd>
<dt><a href="#InventoryGroupIsBlocked">InventoryGroupIsBlocked(C, GroupName)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the body area (Asset Group) for a character is blocked and cannot be used</p>
</dd>
<dt><a href="#InventoryItemHasEffect">InventoryItemHasEffect(Item, Effect, CheckProperties)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if an item has a specific effect</p>
</dd>
<dt><a href="#InventoryExpressionTrigger">InventoryExpressionTrigger(C, Item)</a></dt>
<dd><p>Check if we must trigger an expression for the character after an item is used/applied</p>
</dd>
<dt><a href="#InventoryGetLock">InventoryGetLock(Item)</a> ⇒ <code>Asset</code></dt>
<dd><p>Returns the padlock item that locks another item</p>
</dd>
<dt><a href="#InventoryOwnerOnlyItem">InventoryOwnerOnlyItem(Item)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the item has an OwnerOnly flag, such as the owner padlock</p>
</dd>
<dt><a href="#InventoryLoverOnlyItem">InventoryLoverOnlyItem(Item)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the item has a LoverOnly flag, such as the lover padlock</p>
</dd>
<dt><a href="#InventoryCharacterHasLockedRestraint">InventoryCharacterHasLockedRestraint(C)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the character is wearing at least one restraint that&#39;s locked with an extra lock</p>
</dd>
<dt><a href="#InventoryCharacterIsWearingLock">InventoryCharacterIsWearingLock(C, LockName)</a> ⇒ <code>Boolean</code></dt>
<dd></dd>
<dt><a href="#InventoryCharacterHasOwnerOnlyRestraint">InventoryCharacterHasOwnerOnlyRestraint(C)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the character is wearing at least one item that&#39;s a restraint with a OwnerOnly flag, such as the owner padlock</p>
</dd>
<dt><a href="#InventoryCharacterHasLoverOnlyRestraint">InventoryCharacterHasLoverOnlyRestraint(C)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the character is wearing at least one item that&#39;s a restraint with a LoverOnly flag, such as the lover padlock</p>
</dd>
<dt><a href="#InventoryHasLockableItems">InventoryHasLockableItems(C)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if at least one item on the character can be locked</p>
</dd>
<dt><a href="#InventoryLock">InventoryLock(C, Item, Lock, MemberNumber)</a></dt>
<dd><p>Applies a lock to an appearance item of a character</p>
</dd>
<dt><a href="#InventoryUnlock">InventoryUnlock(C, Item)</a></dt>
<dd><p>Unlocks an item and removes all related properties</p>
</dd>
<dt><a href="#InventoryLockRandom">InventoryLockRandom(C, Item, FromOwner)</a></dt>
<dd><p>Applies a random lock on an item</p>
</dd>
<dt><a href="#InventoryFullLockRandom">InventoryFullLockRandom(C, FromOwner)</a></dt>
<dd><p>Applies random locks on each character items that can be locked</p>
</dd>
<dt><a href="#InventoryConfiscateKey">InventoryConfiscateKey()</a></dt>
<dd><p>Removes all common keys from the player inventory</p>
</dd>
<dt><a href="#InventoryConfiscateRemote">InventoryConfiscateRemote()</a></dt>
<dd><p>Removes the remotes of the vibrators from the player inventory</p>
</dd>
<dt><a href="#InventoryIsWorn">InventoryIsWorn(C, AssetName, AssetGroup)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the item is worn by the character</p>
</dd>
<dt><a href="#InventoryIsPermissionBlocked">InventoryIsPermissionBlocked(C, AssetName, AssetGroup)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if a specific item / asset is blocked by the character item permissions</p>
</dd>
<dt><a href="#InventoryIsPermissionLimited">InventoryIsPermissionLimited(C, AssetName, AssetGroup)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if a specific item / asset is limited by the character item permissions</p>
</dd>
<dt><a href="#InventoryCheckLimitedPermission">InventoryCheckLimitedPermission(C, Item)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the item is not limited, if the player is an owner or a lover of the character, or on their whitelist</p>
</dd>
<dt><a href="#InventoryIsKey">InventoryIsKey(Item)</a> ⇒ <code>Boolean</code></dt>
<dd><p>Returns TRUE if the item is a key, having the effect of unlocking other items</p>
</dd>
<dt><a href="#InventoryStringify">InventoryStringify(C)</a> ⇒ <code>string</code></dt>
<dd><p>Serialises the provided character&#39;s inventory into a string for easy comparisons, inventory items are uniquely identified by their name
and group</p>
</dd>
</dl>

<a name="InventoryAdd"></a>

## InventoryAdd(C, NewItemName, NewItemGroup, Push)
Add a new item by group & name to character inventory

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character that gets the new item added to her inventory |
| NewItemName | <code>String</code> | The name of the new item to add |
| NewItemGroup | <code>String</code> | The group name of the new item to add |
| Push | <code>Boolean</code> | Set to TRUE to push to the server |

<a name="InventoryAddMany"></a>

## InventoryAddMany(C, NewItems, Push)
Adds multiple new items by group & name to the character inventory

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character that gets the new items added to her inventory |
| NewItems | <code>Array.&lt;{Name: string, Group: string}&gt;</code> | The new items to add |
| Push | <code>Boolean</code> | Set to TRUE to push to the server, pushed by default |

<a name="InventoryItemCreate"></a>

## InventoryItemCreate(C, Group, Name) ⇒ <code>Item</code>
Creates a new item for a character based on asset group and name

**Kind**: global function  
**Returns**: <code>Item</code> - A new item for character using the specified asset name, or null if the specified asset could not be found in the named group  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to create the item for |
| Group | <code>string</code> | The name of the asset group the item belongs to |
| Name | <code>string</code> | The name of the asset for the item |

<a name="InventoryDelete"></a>

## InventoryDelete(C, DelItemName, DelItemGroup, Push)
Deletes an item from the character inventory

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we should remove the item |
| DelItemName | <code>String</code> | The name of the item to delete |
| DelItemGroup | <code>String</code> | The group name of the item to delete |
| Push | <code>Boolean</code> | Set to TRUE to push to the server |

<a name="InventoryLoad"></a>

## InventoryLoad(C, Inventory)
Loads the current inventory for a character, can be loaded from an object of Name/Group or a compressed array using LZString

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we should load the inventory |
| Inventory | <code>Array</code> | An array of Name / Group of items to load |

<a name="InventoryAvailable"></a>

## InventoryAvailable(C, InventoryName, InventoryGroup)
Checks if the character has the inventory available

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we should remove the item |
| InventoryName | <code>String</code> | The name of the item to validate |
| InventoryGroup | <code>String</code> | The group name of the item to validate |

<a name="InventoryPrerequisiteMessage"></a>

## InventoryPrerequisiteMessage(C, Prerequisite) ⇒ <code>String</code>
Returns an error message if a prerequisite clashes with the character items and clothes

**Kind**: global function  
**Returns**: <code>String</code> - - The error tag, can be converted to an error message  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we check for prerequisites |
| Prerequisite | <code>String</code> | The name of the prerequisite |

<a name="InventoryAllow"></a>

## InventoryAllow(C, Prerequisite, SetDialog) ⇒ <code>Boolean</code>
Returns TRUE if we can add the item, no other items must block that prerequisite

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if the item can be added to the character  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we check for prerequisites |
| Prerequisite | <code>Array</code> \| <code>String</code> | An array of prerequisites or a string for a single prerequisite |
| SetDialog | <code>Boolean</code> | If TRUE, set the screen dialog message at the same time |

<a name="InventoryGet"></a>

## InventoryGet(C, AssetGroup) ⇒ <code>AppearanceItem</code>
Gets the current item / cloth worn a specific area (AssetGroup)

**Kind**: global function  
**Returns**: <code>AppearanceItem</code> - - Returns the appearance which is the item / cloth asset, color and properties  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we must check the appearance |
| AssetGroup | <code>String</code> | The name of the asset group to scan |

<a name="InventoryWear"></a>

## InventoryWear(C, AssetName, AssetGroup, ItemColor, Difficulty, MemberNumber)
Makes the character wear an item on a body area

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character that must wear the item |
| AssetName | <code>String</code> | The name of the asset to wear |
| AssetGroup | <code>String</code> | The name of the asset group to wear |
| ItemColor | <code>String</code> | The hex color of the item, can be undefined or "Default" |
| Difficulty | <code>Number</code> | The difficulty level to escape from the item |
| MemberNumber | <code>Number</code> | The member number of the character putting the item on - defaults to -1 |

<a name="InventorySetDifficulty"></a>

## InventorySetDifficulty(C, AssetGroup, Difficulty)
Sets the difficulty to remove an item for a body area

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character that is wearing the item |
| AssetGroup | <code>String</code> | The name of the asset group |
| Difficulty | <code>Int</code> | The new difficulty level to escape from the item |

<a name="InventoryLocked"></a>

## InventoryLocked(C, AssetGroup, CheckProperties) ⇒ <code>Boolean</code>
Returns TRUE if there's already a locked item at a given body area

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if the item is locked  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character that is wearing the item |
| AssetGroup | <code>String</code> | The name of the asset group (body area) |
| CheckProperties | <code>Boolean</code> | Set to TRUE to check for additionnal properties |

<a name="InventoryWearRandom"></a>

## InventoryWearRandom(C, GroupName, Difficulty)
Makes the character wear a random item from a body area, the character doesn't need to own the item

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character that must wear the item |
| GroupName | <code>String</code> | The name of the asset group (body area) |
| Difficulty | <code>Int</code> | The difficulty level to escape from the item |

<a name="InventoryRemove"></a>

## InventoryRemove(C, AssetGroup)
Removes a specific item from a character body area

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we must remove the item |
| AssetGroup | <code>String</code> | The name of the asset group (body area) |

<a name="InventoryGroupIsBlocked"></a>

## InventoryGroupIsBlocked(C, GroupName) ⇒ <code>Boolean</code>
Returns TRUE if the body area (Asset Group) for a character is blocked and cannot be used

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if the group is blocked  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we validate the group |
| GroupName | <code>String</code> | The name of the asset group (body area) |

<a name="InventoryItemHasEffect"></a>

## InventoryItemHasEffect(Item, Effect, CheckProperties) ⇒ <code>Boolean</code>
Returns TRUE if an item has a specific effect

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if the effect is on the item  

| Param | Type | Description |
| --- | --- | --- |
| Item | <code>AppearanceItem</code> | The item from appearance that must be validated |
| Effect | <code>String</code> | The name of the effect to validate, can be undefined to check for any effect |
| CheckProperties | <code>Boolean</code> | Set to TRUE to check for item extra properties |

<a name="InventoryExpressionTrigger"></a>

## InventoryExpressionTrigger(C, Item)
Check if we must trigger an expression for the character after an item is used/applied

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character that we must validate |
| Item | <code>AppearanceItem</code> | The item from appearance that we must validate |

<a name="InventoryGetLock"></a>

## InventoryGetLock(Item) ⇒ <code>Asset</code>
Returns the padlock item that locks another item

**Kind**: global function  
**Returns**: <code>Asset</code> - - The asset of the padlock item or NULL if none  

| Param | Type | Description |
| --- | --- | --- |
| Item | <code>AppearanceItem</code> | The item from appearance that must be scanned |

<a name="InventoryOwnerOnlyItem"></a>

## InventoryOwnerOnlyItem(Item) ⇒ <code>Boolean</code>
Returns TRUE if the item has an OwnerOnly flag, such as the owner padlock

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if owner only  

| Param | Type | Description |
| --- | --- | --- |
| Item | <code>AppearanceItem</code> | The item from appearance that must be scanned |

<a name="InventoryLoverOnlyItem"></a>

## InventoryLoverOnlyItem(Item) ⇒ <code>Boolean</code>
Returns TRUE if the item has a LoverOnly flag, such as the lover padlock

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if lover only  

| Param | Type | Description |
| --- | --- | --- |
| Item | <code>AppearanceItem</code> | The item from appearance that must be scanned |

<a name="InventoryCharacterHasLockedRestraint"></a>

## InventoryCharacterHasLockedRestraint(C) ⇒ <code>Boolean</code>
Returns TRUE if the character is wearing at least one restraint that's locked with an extra lock

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if one restraint with an extra lock is found  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to scan |

<a name="InventoryCharacterIsWearingLock"></a>

## InventoryCharacterIsWearingLock(C, LockName) ⇒ <code>Boolean</code>
**Kind**: global function  
**Returns**: <code>Boolean</code> - - Returns TRUE if any item has the specified lock locked onto it  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to scan |
| LockName | <code>String</code> | The type of lock to check for |

<a name="InventoryCharacterHasOwnerOnlyRestraint"></a>

## InventoryCharacterHasOwnerOnlyRestraint(C) ⇒ <code>Boolean</code>
Returns TRUE if the character is wearing at least one item that's a restraint with a OwnerOnly flag, such as the owner padlock

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if one owner only restraint is found  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to scan |

<a name="InventoryCharacterHasLoverOnlyRestraint"></a>

## InventoryCharacterHasLoverOnlyRestraint(C) ⇒ <code>Boolean</code>
Returns TRUE if the character is wearing at least one item that's a restraint with a LoverOnly flag, such as the lover padlock

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if one lover only restraint is found  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to scan |

<a name="InventoryHasLockableItems"></a>

## InventoryHasLockableItems(C) ⇒ <code>Boolean</code>
Returns TRUE if at least one item on the character can be locked

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if at least one item can be locked  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to scan |

<a name="InventoryLock"></a>

## InventoryLock(C, Item, Lock, MemberNumber)
Applies a lock to an appearance item of a character

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which the lock must be applied |
| Item | <code>AppearanceItem</code> | The item from appearance to lock |
| Lock | <code>Asset</code> \| <code>String</code> | The asset of the lock or the name of the lock asset |
| MemberNumber | <code>Int</code> | The member number to put on the lock |

<a name="InventoryUnlock"></a>

## InventoryUnlock(C, Item)
Unlocks an item and removes all related properties

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which the item must be unlocked |
| Item | <code>AppearanceItem</code> | The item from appearance to unlock |

<a name="InventoryLockRandom"></a>

## InventoryLockRandom(C, Item, FromOwner)
Applies a random lock on an item

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which the item must be locked |
| Item | <code>AppearanceItem</code> | The item from appearance to lock |
| FromOwner | <code>Boolean</code> | Set to TRUE if the source is the owner, to apply owner locks |

<a name="InventoryFullLockRandom"></a>

## InventoryFullLockRandom(C, FromOwner)
Applies random locks on each character items that can be locked

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which the items must be locked |
| FromOwner | <code>Boolean</code> | Set to TRUE if the source is the owner, to apply owner locks |

<a name="InventoryConfiscateKey"></a>

## InventoryConfiscateKey()
Removes all common keys from the player inventory

**Kind**: global function  
<a name="InventoryConfiscateRemote"></a>

## InventoryConfiscateRemote()
Removes the remotes of the vibrators from the player inventory

**Kind**: global function  
<a name="InventoryIsWorn"></a>

## InventoryIsWorn(C, AssetName, AssetGroup) ⇒ <code>Boolean</code>
Returns TRUE if the item is worn by the character

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if item is worn  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character to scan |
| AssetName | <code>String</code> | The asset / item name to scan |
| AssetGroup | <code>String</code> | The asset group name to scan |

<a name="InventoryIsPermissionBlocked"></a>

## InventoryIsPermissionBlocked(C, AssetName, AssetGroup) ⇒ <code>Boolean</code>
Returns TRUE if a specific item / asset is blocked by the character item permissions

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if asset / item is blocked  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we check the permissions |
| AssetName | <code>String</code> | The asset / item name to scan |
| AssetGroup | <code>String</code> | The asset group name to scan |

<a name="InventoryIsPermissionLimited"></a>

## InventoryIsPermissionLimited(C, AssetName, AssetGroup) ⇒ <code>Boolean</code>
Returns TRUE if a specific item / asset is limited by the character item permissions

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if asset / item is limited  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we check the permissions |
| AssetName | <code>String</code> | The asset / item name to scan |
| AssetGroup | <code>String</code> | The asset group name to scan |

<a name="InventoryCheckLimitedPermission"></a>

## InventoryCheckLimitedPermission(C, Item) ⇒ <code>Boolean</code>
Returns TRUE if the item is not limited, if the player is an owner or a lover of the character, or on their whitelist

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if item is allowed  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character on which we check the limited permissions for the item |
| Item | <code>Item</code> | The item being interacted with |

<a name="InventoryIsKey"></a>

## InventoryIsKey(Item) ⇒ <code>Boolean</code>
Returns TRUE if the item is a key, having the effect of unlocking other items

**Kind**: global function  
**Returns**: <code>Boolean</code> - - TRUE if item is a key  

| Param | Type | Description |
| --- | --- | --- |
| Item | <code>Item</code> | The item to validate |

<a name="InventoryStringify"></a>

## InventoryStringify(C) ⇒ <code>string</code>
Serialises the provided character's inventory into a string for easy comparisons, inventory items are uniquely identified by their name
and group

**Kind**: global function  
**Returns**: <code>string</code> - - A simple string representation of the character's inventory  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character whose inventory we should serialise |
