## Functions

<dl>
<dt><a href="#DialogReputationLess">DialogReputationLess(RepType, Value)</a> ⇒ <code>boolean</code></dt>
<dd><p>Compares the player&#39;s reputation with a given value</p>
</dd>
<dt><a href="#DialogReputationGreater">DialogReputationGreater(RepType, Value)</a> ⇒ <code>boolean</code></dt>
<dd><p>Compares the player&#39;s reputation with a given value</p>
</dd>
<dt><a href="#DialogMoneyGreater">DialogMoneyGreater(Amount)</a> ⇒ <code>boolean</code></dt>
<dd><p>Compares the player&#39;s money with a given amount</p>
</dd>
<dt><a href="#DialogChangeMoney">DialogChangeMoney(Amount)</a> ⇒ <code>void</code></dt>
<dd><p>Changes a given player&#39;s account by a given amount</p>
</dd>
<dt><a href="#DialogSetReputation">DialogSetReputation(RepType, Value)</a> ⇒ <code>void</code></dt>
<dd><p>Alters the current player&#39;s reputation by a given amount</p>
</dd>
<dt><a href="#DialogChangeReputation">DialogChangeReputation(RepType, Value)</a> ⇒ <code>void</code></dt>
<dd><p>Change the player&#39;s reputation progressively through dialog options (a reputation is easier to break than to build)</p>
</dd>
<dt><a href="#DialogWearItem">DialogWearItem(AssetName, AssetGroup)</a> ⇒ <code>void</code></dt>
<dd><p>Equips a specific item on the player from dialog</p>
</dd>
<dt><a href="#DialogWearRandomItem">DialogWearRandomItem(AssetGroup)</a> ⇒ <code>void</code></dt>
<dd><p>Equips a random item from a given group to the player from dialog</p>
</dd>
<dt><a href="#DialogRemoveItem">DialogRemoveItem(AssetGroup)</a> ⇒ <code>void</code></dt>
<dd><p>Removes an item of a specific item group from the player</p>
</dd>
<dt><a href="#DialogRelease">DialogRelease(C)</a> ⇒ <code>void</code></dt>
<dd><p>Releases a character from restraints</p>
</dd>
<dt><a href="#DialogNaked">DialogNaked(C)</a> ⇒ <code>void</code></dt>
<dd><p>Strips a character naked and removes the restrains</p>
</dd>
<dt><a href="#DialogFullRandomRestrain">DialogFullRandomRestrain(C)</a> ⇒ <code>void</code></dt>
<dd><p>Fully restrain a character with random items</p>
</dd>
<dt><a href="#DialogLogQuery">DialogLogQuery(LogType, LogGroup)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if a specific log has been registered with the player</p>
</dd>
<dt><a href="#DialogAllowItem">DialogAllowItem(Allow)</a> ⇒ <code>boolean</code></dt>
<dd><p>Sets the AllowItem flag on the current character</p>
</dd>
<dt><a href="#DialogDoAllowItem">DialogDoAllowItem(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Returns the value of the AllowItem flag of a given character</p>
</dd>
<dt><a href="#DialogIsKneeling">DialogIsKneeling(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Determines if the given character is kneeling</p>
</dd>
<dt><a href="#DialogIsOwner">DialogIsOwner()</a> ⇒ <code>boolean</code></dt>
<dd><p>Determines if the player is owned by the current character</p>
</dd>
<dt><a href="#DialogIsLover">DialogIsLover()</a> ⇒ <code>boolean</code></dt>
<dd><p>Determines, if the current character is the player&#39;s lover</p>
</dd>
<dt><a href="#DialogIsProperty">DialogIsProperty()</a> ⇒ <code>boolean</code></dt>
<dd><p>Determines if the current character is owned by the player</p>
</dd>
<dt><a href="#DialogIsRestrained">DialogIsRestrained(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if a given character is currently restrained</p>
</dd>
<dt><a href="#DialogIsBlind">DialogIsBlind(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if a given character is currently blinded</p>
</dd>
<dt><a href="#DialogIsEgged">DialogIsEgged(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if a given character is currently wearing a vibrating item</p>
</dd>
<dt><a href="#DialogCanInteract">DialogCanInteract(C)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if a given character is able to change her clothes</p>
</dd>
<dt><a href="#DialogSetPose">DialogSetPose(C, [NewPose])</a> ⇒ <code>void</code></dt>
<dd><p>Sets a new pose for the given character</p>
</dd>
<dt><a href="#DialogSkillGreater">DialogSkillGreater(SkillType, Value)</a> ⇒ <code>boolean</code></dt>
<dd><p>CHecks, wether a given skill of the player is greater or equal a given value</p>
</dd>
<dt><a href="#DialogInventoryAvailable">DialogInventoryAvailable(InventoryName, InventoryGroup)</a> ⇒ <code>boolean</code></dt>
<dd><p>Cheks, if a given item is available in the player&#39;s inventory</p>
</dd>
<dt><a href="#DialogChatRoomPlayerIsAdmin">DialogChatRoomPlayerIsAdmin()</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if the player is the administrator of the current chat room</p>
</dd>
<dt><a href="#DialogChatRoomCanSafeword">DialogChatRoomCanSafeword()</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if a safe word can be used.</p>
</dd>
<dt><a href="#DialogPrerequisite">DialogPrerequisite(D)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks the prerequisite for a given dialog</p>
</dd>
<dt><a href="#DialogCanUnlock">DialogCanUnlock(C, Item)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks, if the player owns a key to unlock a given item or is able to unlock the item</p>
</dd>
<dt><a href="#DialogIntro">DialogIntro()</a> ⇒ <code>string</code></dt>
<dd><p>Returns the current character dialog intro</p>
</dd>
<dt><a href="#DialogLeave">DialogLeave()</a> ⇒ <code>void</code></dt>
<dd><p>Generic dialog function to leave conversation. De-inititalizes global variables and reverts the
FocusGroup of the player and the current character to null</p>
</dd>
<dt><a href="#DialogRemove">DialogRemove()</a> ⇒ <code>void</code></dt>
<dd><p>Generic dialog function to remove a piece of the conversation that&#39;s already done</p>
</dd>
<dt><a href="#DialogRemoveGroup">DialogRemoveGroup(GroupName)</a> ⇒ <code>void</code></dt>
<dd><p>Generic dialog function to remove any dialog from a specific group</p>
</dd>
<dt><a href="#DialogEndExpression">DialogEndExpression()</a> ⇒ <code>void</code></dt>
<dd><p>Generic function that sets timers for expression changes, if the player&#39;S expressions have been altered by the dialog</p>
</dd>
<dt><a href="#DialogLeaveItemMenu">DialogLeaveItemMenu()</a> ⇒ <code>void</code></dt>
<dd><p>Leaves the item menu for both characters. De-initializes global variables, sets the FocusGroup of
player andd current character to null and calls various cleanup functions</p>
</dd>
<dt><a href="#DialogLeaveFocusItem">DialogLeaveFocusItem()</a> ⇒ <code>boolean</code></dt>
<dd><p>Leaves the item menu of the focused item. Constructs a function name from the 
item&#39;s asset group name and the item&#39;s name and tries to call that.</p>
</dd>
<dt><a href="#DialogInventoryAdd">DialogInventoryAdd(C, NewInv, NewInvWorn, SortOrder)</a> ⇒ <code>void</code></dt>
<dd><p>Adds the item in the dialog list</p>
</dd>
<dt><a href="#DialogAlwaysAllowRestraint">DialogAlwaysAllowRestraint()</a> ⇒ <code>boolean</code></dt>
<dd><p>Some special screens can always allow you to put on new restraints. This function determines, if this is possible</p>
</dd>
<dt><a href="#DialogCanUseRemote">DialogCanUseRemote(C, Item)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks whether the player can use a remote on the given character and item</p>
</dd>
<dt><a href="#DialogMenuButtonBuild">DialogMenuButtonBuild(C)</a> ⇒ <code>void</code></dt>
<dd><p>Build the buttons in the top menu</p>
</dd>
<dt><a href="#DialogInventorySort">DialogInventorySort()</a> ⇒ <code>void</code></dt>
<dd><p>Sort the inventory list by the global variable SortOrder (a fixed number &amp; current language description)</p>
</dd>
<dt><a href="#DialogInventoryBuild">DialogInventoryBuild(C, [Offset])</a> ⇒ <code>void</code></dt>
<dd><p>Build the inventory listing for the dialog which is what&#39;s equipped, 
the player&#39;s inventory and the character&#39;s inventory for that group</p>
</dd>
<dt><a href="#DialogFacialExpressionsBuild">DialogFacialExpressionsBuild()</a> ⇒ <code>void</code></dt>
<dd><p>Build the initial state of the selection available in the facial expressions menu</p>
</dd>
<dt><a href="#DialogProgressGetOperation">DialogProgressGetOperation(C, PrevItem, NextItem)</a> ⇒ <code>string</code></dt>
<dd><p>Gets the correct label for the current operation (struggling, removing, swaping, adding, etc.)</p>
</dd>
<dt><a href="#DialogStruggle">DialogStruggle(Reverse)</a> ⇒ <code>void</code></dt>
<dd><p>Starts the dialog progress bar and keeps the items that needs to be added / swaped / removed. 
The change of facial expressions during struggling is done here</p>
</dd>
<dt><a href="#DialogProgressStart">DialogProgressStart(C, PrevItem, [NextItem])</a> ⇒ <code>void</code></dt>
<dd><p>Starts the dialog progress bar for struggling out of bondage and keeps the items that needs to be added / swapped / removed.
First the challenge level is calculated based on the base item difficulty, the skill of the rigger and the escapee and modified, if
the escapee is bound in a way. Also blushing and drooling, as well as playing a sound is handled in this function.</p>
</dd>
<dt><a href="#DialogKeyDown">DialogKeyDown()</a> ⇒ <code>void</code></dt>
<dd><p>Handles the KeyDown event. The player can use the space bar to speed up the dialog progress, just like clicking.
Increases or decreases the struggle mini-game, if a/A or s/S were pressed.</p>
</dd>
<dt><a href="#DialogMenuButtonClick">DialogMenuButtonClick()</a> ⇒ <code>void</code></dt>
<dd><p>Handles the Click events in the Dialog Screen</p>
</dd>
<dt><a href="#DialogPublishAction">DialogPublishAction(C, ClickItem)</a> ⇒ <code>void</code></dt>
<dd><p>Publishes the item action to the local chat room or the dialog screen</p>
</dd>
<dt><a href="#DialogItemClick">DialogItemClick(ClickItem)</a> ⇒ <code>void</code></dt>
<dd><p>Handles clicks on an item</p>
</dd>
<dt><a href="#DialogClick">DialogClick()</a> ⇒ <code>void</code></dt>
<dd><p>Handles the click in the dialog screen</p>
</dd>
<dt><a href="#DialogSetText">DialogSetText(NewText)</a> ⇒ <code>void</code></dt>
<dd><p>Displays the given text for 5 seconds</p>
</dd>
<dt><a href="#DialogExtendItem">DialogExtendItem(Item, SourceItem)</a> ⇒ <code>void</code></dt>
<dd><p>Shows the extended item menue for a given item, if possible. 
Therefore a dynamic function name is created and then called.</p>
</dd>
<dt><a href="#DialogChangeItemColor">DialogChangeItemColor(C, Color)</a> ⇒ <code>void</code></dt>
<dd><p>Validates that the player is allowed to change the item color and swaps it on the fly</p>
</dd>
<dt><a href="#DialogDrawActivityMenu">DialogDrawActivityMenu(C)</a> ⇒ <code>void</code></dt>
<dd><p>Draw the activity selection dialog</p>
</dd>
<dt><a href="#DialogDrawItemMenu">DialogDrawItemMenu(C)</a> ⇒ <code>void</code></dt>
<dd><p>Draw the item menu dialog</p>
</dd>
<dt><a href="#DialogFind">DialogFind(C, KeyWord1, [KeyWord2], [ReturnPrevious])</a> ⇒ <code>string</code></dt>
<dd><p>Searches in the dialog for a specific stage keyword and returns that dialog option if we find it</p>
</dd>
<dt><a href="#DialogFindAutoReplace">DialogFindAutoReplace(C, KeyWord1, [KeyWord2], [ReturnPrevious])</a> ⇒ <code>string</code></dt>
<dd><p>Searches in the dialog for a specific stage keyword and returns that dialog option if we find it and replace the names</p>
</dd>
<dt><a href="#DialogDraw">DialogDraw()</a> ⇒ <code>void</code></dt>
<dd><p>Draws the initial Dialog screen. That screen is entered, when the player clicks on herself or another player</p>
</dd>
<dt><a href="#DialogDrawExpressionMenu">DialogDrawExpressionMenu()</a> ⇒ <code>void</code></dt>
<dd><p>Draw the menu for changing facial expressions</p>
</dd>
<dt><a href="#DialogSetSkillRatio">DialogSetSkillRatio(SkillType, NewRatio)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the skill ratio for the player, will be a % of effectiveness applied to the skill when using it. 
This way a player can use only a part of her bondage or evasion skill.</p>
</dd>
<dt><a href="#DialogChatRoomAdminAction">DialogChatRoomAdminAction(ActionType, Publish)</a> ⇒ <code>void</code></dt>
<dd><p>Sends an room administrative command to the server for the chat room from the player dialog</p>
</dd>
<dt><a href="#DialogChatRoomHasSwapTarget">DialogChatRoomHasSwapTarget()</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a chat room player swap is in progress</p>
</dd>
<dt><a href="#DialogChatRoomSafewordRevert">DialogChatRoomSafewordRevert()</a> ⇒ <code>void</code></dt>
<dd><p>Leave the dialog and revert back to a safe state, when the player uses her safe word</p>
</dd>
<dt><a href="#DialogChatRoomSafewordRelease">DialogChatRoomSafewordRelease()</a> ⇒ <code>void</code></dt>
<dd><p>Leave the dialog and release the player of all restraints before returning them to the Main Lobby</p>
</dd>
</dl>

<a name="DialogReputationLess"></a>

## DialogReputationLess(RepType, Value) ⇒ <code>boolean</code>
Compares the player's reputation with a given value

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if a specific reputation type is less or equal than a given value  

| Param | Type | Description |
| --- | --- | --- |
| RepType | <code>string</code> | The name of the reputation to check |
| Value | <code>string</code> | The value to compare |

<a name="DialogReputationGreater"></a>

## DialogReputationGreater(RepType, Value) ⇒ <code>boolean</code>
Compares the player's reputation with a given value

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if a specific reputation type is greater or equal than a given value  

| Param | Type | Description |
| --- | --- | --- |
| RepType | <code>string</code> | The name of the reputation to check |
| Value | <code>string</code> | The value to compare |

<a name="DialogMoneyGreater"></a>

## DialogMoneyGreater(Amount) ⇒ <code>boolean</code>
Compares the player's money with a given amount

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if the player has enough money  

| Param | Type | Description |
| --- | --- | --- |
| Amount | <code>string</code> | The amount of money that must be met |

<a name="DialogChangeMoney"></a>

## DialogChangeMoney(Amount) ⇒ <code>void</code>
Changes a given player's account by a given amount

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Amount | <code>string</code> | The amount that should be charged or added to the player's account |

<a name="DialogSetReputation"></a>

## DialogSetReputation(RepType, Value) ⇒ <code>void</code>
Alters the current player's reputation by a given amount

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| RepType | <code>string</code> | The name of the reputation to change |
| Value | <code>string</code> | The value, the player's reputation should be altered by |

<a name="DialogChangeReputation"></a>

## DialogChangeReputation(RepType, Value) ⇒ <code>void</code>
Change the player's reputation progressively through dialog options (a reputation is easier to break than to build)

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| RepType | <code>string</code> | The name of the reputation to change |
| Value | <code>string</code> | The value, the player's reputation should be altered by |

<a name="DialogWearItem"></a>

## DialogWearItem(AssetName, AssetGroup) ⇒ <code>void</code>
Equips a specific item on the player from dialog

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| AssetName | <code>string</code> | The name of the asset that should be equipped |
| AssetGroup | <code>string</code> | The name of the corresponding asset group |

<a name="DialogWearRandomItem"></a>

## DialogWearRandomItem(AssetGroup) ⇒ <code>void</code>
Equips a random item from a given group to the player from dialog

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| AssetGroup | <code>string</code> | The name of the asset group to pick from |

<a name="DialogRemoveItem"></a>

## DialogRemoveItem(AssetGroup) ⇒ <code>void</code>
Removes an item of a specific item group from the player

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| AssetGroup | <code>string</code> | The item to be removed belongs to this asset group |

<a name="DialogRelease"></a>

## DialogRelease(C) ⇒ <code>void</code>
Releases a character from restraints

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to be released.  Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogNaked"></a>

## DialogNaked(C) ⇒ <code>void</code>
Strips a character naked and removes the restrains

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to be stripped and released. Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogFullRandomRestrain"></a>

## DialogFullRandomRestrain(C) ⇒ <code>void</code>
Fully restrain a character with random items

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to be restrained. Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogLogQuery"></a>

## DialogLogQuery(LogType, LogGroup) ⇒ <code>boolean</code>
Checks, if a specific log has been registered with the player

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if a specific log is registered  

| Param | Type | Description |
| --- | --- | --- |
| LogType | <code>string</code> | The name of the log to search for |
| LogGroup | <code>string</code> | The name of the log group |

<a name="DialogAllowItem"></a>

## DialogAllowItem(Allow) ⇒ <code>boolean</code>
Sets the AllowItem flag on the current character

**Kind**: global function  
**Returns**: <code>boolean</code> - - The boolean version of the flag  

| Param | Type | Description |
| --- | --- | --- |
| Allow | <code>string</code> | The flag to set. Either "TRUE" or "FALSE" |

<a name="DialogDoAllowItem"></a>

## DialogDoAllowItem(C) ⇒ <code>boolean</code>
Returns the value of the AllowItem flag of a given character

**Kind**: global function  
**Returns**: <code>boolean</code> - - The value of the given character's AllowItem flag  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character whose flag should be returned. Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogIsKneeling"></a>

## DialogIsKneeling(C) ⇒ <code>boolean</code>
Determines if the given character is kneeling

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the given character is kneeling  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to check Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogIsOwner"></a>

## DialogIsOwner() ⇒ <code>boolean</code>
Determines if the player is owned by the current character

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the player is owned by the current character, false otherwise  
<a name="DialogIsLover"></a>

## DialogIsLover() ⇒ <code>boolean</code>
Determines, if the current character is the player's lover

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the current character is one of the player's lovers  
<a name="DialogIsProperty"></a>

## DialogIsProperty() ⇒ <code>boolean</code>
Determines if the current character is owned by the player

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the current character is owned by the player, false otherwise  
<a name="DialogIsRestrained"></a>

## DialogIsRestrained(C) ⇒ <code>boolean</code>
Checks, if a given character is currently restrained

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the given character is wearing restraints, false otherwise  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to check. Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogIsBlind"></a>

## DialogIsBlind(C) ⇒ <code>boolean</code>
Checks, if a given character is currently blinded

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the given character is blinded, false otherwise  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to check. Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogIsEgged"></a>

## DialogIsEgged(C) ⇒ <code>boolean</code>
Checks, if a given character is currently wearing a vibrating item

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the given character is wearing a vibrating item, false otherwise  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to check. Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogCanInteract"></a>

## DialogCanInteract(C) ⇒ <code>boolean</code>
Checks, if a given character is able to change her clothes

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the given character is able to change clothes, false otherwise  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>string</code> | The character to check. Either the player (value: Player) or the current character (value: CurrentCharacter) |

<a name="DialogSetPose"></a>

## DialogSetPose(C, [NewPose]) ⇒ <code>void</code>
Sets a new pose for the given character

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| C | <code>string</code> |  | The character whose pose should be altered. Either the player (value: Player) or the current character (value: CurrentCharacter) |
| [NewPose] | <code>string</code> | <code>null</code> | The new pose, the character should take.  Can be omitted to bring the character back to the standing position. |

<a name="DialogSkillGreater"></a>

## DialogSkillGreater(SkillType, Value) ⇒ <code>boolean</code>
CHecks, wether a given skill of the player is greater or equal a given value

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true if a specific skill is greater or equal than a given value  

| Param | Type | Description |
| --- | --- | --- |
| SkillType | <code>string</code> | Name of the skill to check |
| Value | <code>string</code> | The value, the given skill must be compared to |

<a name="DialogInventoryAvailable"></a>

## DialogInventoryAvailable(InventoryName, InventoryGroup) ⇒ <code>boolean</code>
Cheks, if a given item is available in the player's inventory

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the item is available, false otherwise  

| Param | Type |
| --- | --- |
| InventoryName | <code>string</code> | 
| InventoryGroup | <code>string</code> | 

<a name="DialogChatRoomPlayerIsAdmin"></a>

## DialogChatRoomPlayerIsAdmin() ⇒ <code>boolean</code>
Checks, if the player is the administrator of the current chat room

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the player belogs to the group of administrators for the current char room false otherwise  
<a name="DialogChatRoomCanSafeword"></a>

## DialogChatRoomCanSafeword() ⇒ <code>boolean</code>
Checks, if a safe word can be used.

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the player is currently within a chat room  
<a name="DialogPrerequisite"></a>

## DialogPrerequisite(D) ⇒ <code>boolean</code>
Checks the prerequisite for a given dialog

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the prerequisite is met, false otherwise  

| Param | Type | Description |
| --- | --- | --- |
| D | <code>number</code> | Index of the dialog to check |

<a name="DialogCanUnlock"></a>

## DialogCanUnlock(C, Item) ⇒ <code>boolean</code>
Checks, if the player owns a key to unlock a given item or is able to unlock the item

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if the character can unlock the given item, false otherwise  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character whose inventory and ability to unlock the lock should be checked |
| Item | <code>Item</code> | The item that should be unlocked |

<a name="DialogIntro"></a>

## DialogIntro() ⇒ <code>string</code>
Returns the current character dialog intro

**Kind**: global function  
**Returns**: <code>string</code> - - The name of the current dialog, if such a dialog exists, any empty string otherwise  
<a name="DialogLeave"></a>

## DialogLeave() ⇒ <code>void</code>
Generic dialog function to leave conversation. De-inititalizes global variables and reverts the
FocusGroup of the player and the current character to null

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogRemove"></a>

## DialogRemove() ⇒ <code>void</code>
Generic dialog function to remove a piece of the conversation that's already done

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogRemoveGroup"></a>

## DialogRemoveGroup(GroupName) ⇒ <code>void</code>
Generic dialog function to remove any dialog from a specific group

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| GroupName | <code>string</code> | All dialog options are removed from this group |

<a name="DialogEndExpression"></a>

## DialogEndExpression() ⇒ <code>void</code>
Generic function that sets timers for expression changes, if the player'S expressions have been altered by the dialog

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogLeaveItemMenu"></a>

## DialogLeaveItemMenu() ⇒ <code>void</code>
Leaves the item menu for both characters. De-initializes global variables, sets the FocusGroup of
player andd current character to null and calls various cleanup functions

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogLeaveFocusItem"></a>

## DialogLeaveFocusItem() ⇒ <code>boolean</code>
Leaves the item menu of the focused item. Constructs a function name from the 
item's asset group name and the item's name and tries to call that.

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if an item specific exit function was called, false otherwise  
<a name="DialogInventoryAdd"></a>

## DialogInventoryAdd(C, NewInv, NewInvWorn, SortOrder) ⇒ <code>void</code>
Adds the item in the dialog list

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character, whose inventory should be manipulated |
| NewInv | <code>Item</code> | The item that should be added to the player's inventory |
| NewInvWorn | <code>boolean</code> | Should be true, if the item is worn, false otherwise |
| SortOrder | <code>number</code> | Defines the group the item is added to. |

<a name="DialogAlwaysAllowRestraint"></a>

## DialogAlwaysAllowRestraint() ⇒ <code>boolean</code>
Some special screens can always allow you to put on new restraints. This function determines, if this is possible

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns trues, if it is possible to put on new restraints.  
<a name="DialogCanUseRemote"></a>

## DialogCanUseRemote(C, Item) ⇒ <code>boolean</code>
Checks whether the player can use a remote on the given character and item

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true if the player is able to use a remote for the given character and item. Returns false otherwise.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | the character that the item is equipped on |
| Item | <code>Item</code> | the item to check for remote usage against |

<a name="DialogMenuButtonBuild"></a>

## DialogMenuButtonBuild(C) ⇒ <code>void</code>
Build the buttons in the top menu

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for whom the dialog is prepared |

<a name="DialogInventorySort"></a>

## DialogInventorySort() ⇒ <code>void</code>
Sort the inventory list by the global variable SortOrder (a fixed number & current language description)

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogInventoryBuild"></a>

## DialogInventoryBuild(C, [Offset]) ⇒ <code>void</code>
Build the inventory listing for the dialog which is what's equipped, 
the player's inventory and the character's inventory for that group

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character whose inventory must be built |
| [Offset] | <code>number</code> | The offset to be at, if specified. |

<a name="DialogFacialExpressionsBuild"></a>

## DialogFacialExpressionsBuild() ⇒ <code>void</code>
Build the initial state of the selection available in the facial expressions menu

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogProgressGetOperation"></a>

## DialogProgressGetOperation(C, PrevItem, NextItem) ⇒ <code>string</code>
Gets the correct label for the current operation (struggling, removing, swaping, adding, etc.)

**Kind**: global function  
**Returns**: <code>string</code> - - The appropriate dialog option  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character who acts |
| PrevItem | <code>Item</code> | The first item that's part of the action |
| NextItem | <code>Item</code> | The second item that's part of the action |

<a name="DialogStruggle"></a>

## DialogStruggle(Reverse) ⇒ <code>void</code>
Starts the dialog progress bar and keeps the items that needs to be added / swaped / removed. 
The change of facial expressions during struggling is done here

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Reverse | <code>boolean</code> | If set to true, the progress is decreased |

<a name="DialogProgressStart"></a>

## DialogProgressStart(C, PrevItem, [NextItem]) ⇒ <code>void</code>
Starts the dialog progress bar for struggling out of bondage and keeps the items that needs to be added / swapped / removed.
First the challenge level is calculated based on the base item difficulty, the skill of the rigger and the escapee and modified, if
the escapee is bound in a way. Also blushing and drooling, as well as playing a sound is handled in this function.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character who tries to struggle |
| PrevItem | <code>Item</code> | The item, the character wants to struggle out of |
| [NextItem] | <code>Item</code> | The item that should substitute the first one |

<a name="DialogKeyDown"></a>

## DialogKeyDown() ⇒ <code>void</code>
Handles the KeyDown event. The player can use the space bar to speed up the dialog progress, just like clicking.
Increases or decreases the struggle mini-game, if a/A or s/S were pressed.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogMenuButtonClick"></a>

## DialogMenuButtonClick() ⇒ <code>void</code>
Handles the Click events in the Dialog Screen

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogPublishAction"></a>

## DialogPublishAction(C, ClickItem) ⇒ <code>void</code>
Publishes the item action to the local chat room or the dialog screen

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character who is the actor in this action |
| ClickItem | <code>Item</code> | The item that is used |

<a name="DialogItemClick"></a>

## DialogItemClick(ClickItem) ⇒ <code>void</code>
Handles clicks on an item

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ClickItem | <code>Item</code> | The item that is clicked |

<a name="DialogClick"></a>

## DialogClick() ⇒ <code>void</code>
Handles the click in the dialog screen

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogSetText"></a>

## DialogSetText(NewText) ⇒ <code>void</code>
Displays the given text for 5 seconds

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NewText | <code>string</code> | The text to be displayed |

<a name="DialogExtendItem"></a>

## DialogExtendItem(Item, SourceItem) ⇒ <code>void</code>
Shows the extended item menue for a given item, if possible. 
Therefore a dynamic function name is created and then called.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Item | <code>Item</code> | The item the extended menu should be shown for |
| SourceItem | <code>Item</code> | The source of the extended menu |

<a name="DialogChangeItemColor"></a>

## DialogChangeItemColor(C, Color) ⇒ <code>void</code>
Validates that the player is allowed to change the item color and swaps it on the fly

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The player who wants to change the color |
| Color | <code>string</code> | The new color in the format "#rrggbb" |

<a name="DialogDrawActivityMenu"></a>

## DialogDrawActivityMenu(C) ⇒ <code>void</code>
Draw the activity selection dialog

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for whom the activity selection dialog is drawn. That can be the player or another character. |

<a name="DialogDrawItemMenu"></a>

## DialogDrawItemMenu(C) ⇒ <code>void</code>
Draw the item menu dialog

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for whom the activity selection dialog is drawn. That can be the player or another character. |

<a name="DialogFind"></a>

## DialogFind(C, KeyWord1, [KeyWord2], [ReturnPrevious]) ⇒ <code>string</code>
Searches in the dialog for a specific stage keyword and returns that dialog option if we find it

**Kind**: global function  
**Returns**: <code>string</code> - - The name of a dialog. That can either be the one with the keyword or the previous dialog. 
An empty string is returned, if neither keyword was found and no previous dialog was given.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character whose dialog optio* |
| KeyWord1 | <code>string</code> | The key word to search for |
| [KeyWord2] | <code>string</code> | An optionally given second key word. is only looked for, if specified and the first  keyword was not found. |
| [ReturnPrevious] | <code>boolean</code> | If specified, returns the previous dialog, if neither of the the two key words were found  ns should be searched |

<a name="DialogFindAutoReplace"></a>

## DialogFindAutoReplace(C, KeyWord1, [KeyWord2], [ReturnPrevious]) ⇒ <code>string</code>
Searches in the dialog for a specific stage keyword and returns that dialog option if we find it and replace the names

**Kind**: global function  
**Returns**: <code>string</code> - - The name of a dialog. That can either be the one with the keyword or the previous dialog.
An empty string is returned, if neither keyword was found and no previous dialog was given. 'SourceCharacter' 
is replaced with the player's name and 'DestinationCharacter' with the current character's name.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character whose dialog options should be searched |
| KeyWord1 | <code>string</code> | The key word to search for |
| [KeyWord2] | <code>string</code> | An optionally given second key word. is only looked for, if specified and the first keyword was not found. |
| [ReturnPrevious] | <code>boolean</code> | If specified, returns the previous dialog, if neither of the the two key words were found |

<a name="DialogDraw"></a>

## DialogDraw() ⇒ <code>void</code>
Draws the initial Dialog screen. That screen is entered, when the player clicks on herself or another player

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogDrawExpressionMenu"></a>

## DialogDrawExpressionMenu() ⇒ <code>void</code>
Draw the menu for changing facial expressions

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogSetSkillRatio"></a>

## DialogSetSkillRatio(SkillType, NewRatio) ⇒ <code>void</code>
Sets the skill ratio for the player, will be a % of effectiveness applied to the skill when using it. 
This way a player can use only a part of her bondage or evasion skill.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| SkillType | <code>string</code> | The name of the skill to influence |
| NewRatio | <code>strign</code> | The ration of this skill that should be used |

<a name="DialogChatRoomAdminAction"></a>

## DialogChatRoomAdminAction(ActionType, Publish) ⇒ <code>void</code>
Sends an room administrative command to the server for the chat room from the player dialog

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ActionType | <code>string</code> | The name of the administrative command to use |
| Publish | <code>string</code> | Determines wether the action should be published to the ChatRoom. As this is a string, use "true" to do so |

<a name="DialogChatRoomHasSwapTarget"></a>

## DialogChatRoomHasSwapTarget() ⇒ <code>boolean</code>
Checks if a chat room player swap is in progress

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns true, if a swap is in progress, false otherwise  
<a name="DialogChatRoomSafewordRevert"></a>

## DialogChatRoomSafewordRevert() ⇒ <code>void</code>
Leave the dialog and revert back to a safe state, when the player uses her safe word

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="DialogChatRoomSafewordRelease"></a>

## DialogChatRoomSafewordRelease() ⇒ <code>void</code>
Leave the dialog and release the player of all restraints before returning them to the Main Lobby

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
