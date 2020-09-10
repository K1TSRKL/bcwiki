## Constants

<dl>
<dt><a href="#ExtendedItemOffsets">ExtendedItemOffsets</a> : <code>Object.&lt;string, number&gt;</code></dt>
<dd><p>A lookup for the current pagination offset for all extended item options. Offsets are only recorded if the extended item requires
pagination.
Example format:</p>
<pre><code class="language-json">{
    &quot;ItemArms/HempRope&quot;: 4,
    &quot;ItemArms/Web&quot;: 0
}</code></pre>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#ExtendedItemLoad">ExtendedItemLoad(Options, DialogKey)</a> ⇒ <code>void</code></dt>
<dd><p>Loads the item extension properties</p>
</dd>
<dt><a href="#ExtendedItemDraw">ExtendedItemDraw(Options, DialogPrefix)</a> ⇒ <code>void</code></dt>
<dd><p>Draws the extended item type selection screen</p>
</dd>
<dt><a href="#ExtendedItemClick">ExtendedItemClick(Options, IsCloth)</a> ⇒ <code>void</code></dt>
<dd><p>Handles clicks on the extended item type selection screen</p>
</dd>
<dt><a href="#ExtendedItemSetType">ExtendedItemSetType(Options, Option, IsCloth)</a> ⇒ <code>void</code></dt>
<dd><p>Handler function for setting the type of an extended item</p>
</dd>
<dt><a href="#ExtendedItemDrawTwo">ExtendedItemDrawTwo(Options, DialogPrefix, IsSelfBondage)</a> ⇒ <code>void</code></dt>
<dd><p>Draws the extended item type selection screen when there are only two options</p>
</dd>
<dt><a href="#ExtendedItemDrawGrid">ExtendedItemDrawGrid(Options, DialogPrefix, IsSelfBondage)</a> ⇒ <code>void</code></dt>
<dd><p>Draws the extended item type selection screen when there are more than two options. Options will be paginated if necessary, with four
options drawn per page in a 2x2 grid</p>
</dd>
<dt><a href="#ExtendedItemClickTwo">ExtendedItemClickTwo(Options, IsSelfBondage, IsCloth)</a> ⇒ <code>void</code></dt>
<dd><p>Handles clicks on the extended item type selection screen when there are only two options</p>
</dd>
<dt><a href="#ExtendedItemClickGrid">ExtendedItemClickGrid(Options, IsSelfBondage, IsCloth)</a> ⇒ <code>void</code></dt>
<dd><p>Handles clicks on the extended item type selection screen when there are more than two options</p>
</dd>
<dt><a href="#ExtendedItemHandleOptionClick">ExtendedItemHandleOptionClick(Options, Option, IsSelfBondage, IsCloth)</a> ⇒ <code>void</code></dt>
<dd><p>Handler function called when an option on the type selection screen is clicked</p>
</dd>
<dt><a href="#ExtendedItemRequirementCheckMessage">ExtendedItemRequirementCheckMessage(Option, IsSelfBondage)</a> ⇒ <code>string</code> | <code>null</code></dt>
<dd><p>Checks whether the player meets the requirements for an extended type option. This will check against their Bondage
skill if applying the item to another character, or their Self Bondage skill if applying the item to themselves.</p>
</dd>
<dt><a href="#ExtendedItemFunctionPrefix">ExtendedItemFunctionPrefix()</a> ⇒ <code>string</code></dt>
<dd><p>Simple getter for the function prefix used for the currently focused extended item - used for calling standard
extended item functions (e.g. if the currently focused it is the hemp rope arm restraint, this will return
&quot;InventoryItemArmsHempRope&quot;, allowing functions like InventoryItemArmsHempRopeLoad to be called)</p>
</dd>
<dt><a href="#ExtendedItemOffsetKey">ExtendedItemOffsetKey()</a> ⇒ <code>string</code></dt>
<dd><p>Simple getter for the key of the currently focused extended item in the ExtendedItemOffsets lookup</p>
</dd>
<dt><a href="#ExtendedItemGetOffset">ExtendedItemGetOffset()</a> ⇒ <code>number</code></dt>
<dd><p>Gets the pagination offset of the currently focused extended item</p>
</dd>
<dt><a href="#ExtendedItemSetOffset">ExtendedItemSetOffset(Offset)</a> ⇒ <code>void</code></dt>
<dd><p>Sets the pagination offset for the currently focused extended item</p>
</dd>
<dt><a href="#ExtendedItemNextPage">ExtendedItemNextPage(Options)</a> ⇒ <code>void</code></dt>
<dd><p>Switches the pagination offset to the next page for the currently focused extended item. If the new offset is greater
than the number of available options, the offset will be reset to zero, wrapping back to the first page.</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#ExtendedItemOption">ExtendedItemOption</a> : <code>Object</code></dt>
<dd><p>Defines a single extended item option</p>
</dd>
</dl>

<a name="ExtendedItemOffsets"></a>

## ExtendedItemOffsets : <code>Object.&lt;string, number&gt;</code>
A lookup for the current pagination offset for all extended item options. Offsets are only recorded if the extended item requires
pagination.
Example format:
```json
{
    "ItemArms/HempRope": 4,
    "ItemArms/Web": 0
}
```

**Kind**: global constant  
<a name="ExtendedItemLoad"></a>

## ExtendedItemLoad(Options, DialogKey) ⇒ <code>void</code>
Loads the item extension properties

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| DialogKey | <code>string</code> | The dialog key for the message to display prompting the player to select an extended type |

<a name="ExtendedItemDraw"></a>

## ExtendedItemDraw(Options, DialogPrefix) ⇒ <code>void</code>
Draws the extended item type selection screen

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| DialogPrefix | <code>string</code> | The prefix to the dialog keys for the display strings describing each extended type.     The full dialog key will be <Prefix><Option.Name> |

<a name="ExtendedItemClick"></a>

## ExtendedItemClick(Options, IsCloth) ⇒ <code>void</code>
Handles clicks on the extended item type selection screen

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| IsCloth | <code>boolean</code> | Whether or not the click is performed on a clothing item. |

<a name="ExtendedItemSetType"></a>

## ExtendedItemSetType(Options, Option, IsCloth) ⇒ <code>void</code>
Handler function for setting the type of an extended item

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| Option | [<code>ExtendedItemOption</code>](#ExtendedItemOption) | The selected type definition |
| IsCloth | <code>boolean</code> | Whether or not the click is performed on a clothing item. |

<a name="ExtendedItemDrawTwo"></a>

## ExtendedItemDrawTwo(Options, DialogPrefix, IsSelfBondage) ⇒ <code>void</code>
Draws the extended item type selection screen when there are only two options

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| DialogPrefix | <code>string</code> | The prefix to the dialog keys for the display strings describing each extended type.     The full dialog key will be <Prefix><Option.Name> |
| IsSelfBondage | <code>boolean</code> | Whether or not the player is applying the item to themselves |

<a name="ExtendedItemDrawGrid"></a>

## ExtendedItemDrawGrid(Options, DialogPrefix, IsSelfBondage) ⇒ <code>void</code>
Draws the extended item type selection screen when there are more than two options. Options will be paginated if necessary, with four
options drawn per page in a 2x2 grid

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| DialogPrefix | <code>string</code> | The prefix to the dialog keys for the display strings describing each extended type.     The full dialog key will be <Prefix><Option.Name> |
| IsSelfBondage | <code>boolean</code> | Whether or not the player is applying the item to themselves |

<a name="ExtendedItemClickTwo"></a>

## ExtendedItemClickTwo(Options, IsSelfBondage, IsCloth) ⇒ <code>void</code>
Handles clicks on the extended item type selection screen when there are only two options

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| IsSelfBondage | <code>boolean</code> | Whether or not the player is applying the item to themselves |
| IsCloth | <code>boolean</code> | Whether or not the click is performed on a clothing item. |

<a name="ExtendedItemClickGrid"></a>

## ExtendedItemClickGrid(Options, IsSelfBondage, IsCloth) ⇒ <code>void</code>
Handles clicks on the extended item type selection screen when there are more than two options

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| IsSelfBondage | <code>boolean</code> | Whether or not the player is applying the item to themselves |
| IsCloth | <code>boolean</code> | Whether or not the click is performed on a clothing item. |

<a name="ExtendedItemHandleOptionClick"></a>

## ExtendedItemHandleOptionClick(Options, Option, IsSelfBondage, IsCloth) ⇒ <code>void</code>
Handler function called when an option on the type selection screen is clicked

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |
| Option | [<code>ExtendedItemOption</code>](#ExtendedItemOption) | The selected type definition |
| IsSelfBondage | <code>boolean</code> | Whether or not the player is applying the item to themselves |
| IsCloth | <code>boolean</code> | Whether or not the click is performed on a clothing item. |

<a name="ExtendedItemRequirementCheckMessage"></a>

## ExtendedItemRequirementCheckMessage(Option, IsSelfBondage) ⇒ <code>string</code> \| <code>null</code>
Checks whether the player meets the requirements for an extended type option. This will check against their Bondage
skill if applying the item to another character, or their Self Bondage skill if applying the item to themselves.

**Kind**: global function  
**Returns**: <code>string</code> \| <code>null</code> - null if the player meets the option requirements. Otherwise a string message informing them
of the requirements they do not meet  

| Param | Type | Description |
| --- | --- | --- |
| Option | [<code>ExtendedItemOption</code>](#ExtendedItemOption) | The selected type definition |
| IsSelfBondage | <code>boolean</code> | Whether or not the player is applying the item to themselves |

<a name="ExtendedItemFunctionPrefix"></a>

## ExtendedItemFunctionPrefix() ⇒ <code>string</code>
Simple getter for the function prefix used for the currently focused extended item - used for calling standard
extended item functions (e.g. if the currently focused it is the hemp rope arm restraint, this will return
"InventoryItemArmsHempRope", allowing functions like InventoryItemArmsHempRopeLoad to be called)

**Kind**: global function  
**Returns**: <code>string</code> - The extended item function prefix for the currently focused item  
<a name="ExtendedItemOffsetKey"></a>

## ExtendedItemOffsetKey() ⇒ <code>string</code>
Simple getter for the key of the currently focused extended item in the ExtendedItemOffsets lookup

**Kind**: global function  
**Returns**: <code>string</code> - The offset lookup key for the currently focused extended item  
<a name="ExtendedItemGetOffset"></a>

## ExtendedItemGetOffset() ⇒ <code>number</code>
Gets the pagination offset of the currently focused extended item

**Kind**: global function  
**Returns**: <code>number</code> - The pagination offset for the currently focused extended item  
<a name="ExtendedItemSetOffset"></a>

## ExtendedItemSetOffset(Offset) ⇒ <code>void</code>
Sets the pagination offset for the currently focused extended item

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Offset | <code>number</code> | The new offset to set |

<a name="ExtendedItemNextPage"></a>

## ExtendedItemNextPage(Options) ⇒ <code>void</code>
Switches the pagination offset to the next page for the currently focused extended item. If the new offset is greater
than the number of available options, the offset will be reset to zero, wrapping back to the first page.

**Kind**: global function  
**Returns**: <code>void</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Options | [<code>Array.&lt;ExtendedItemOption&gt;</code>](#ExtendedItemOption) | An Array of type definitions for each allowed extended type. The first item in the array should     be the default option. |

<a name="ExtendedItemOption"></a>

## ExtendedItemOption : <code>Object</code>
Defines a single extended item option

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| Name | <code>string</code> | The name of the type - used for the preview icon and the translation key in the CSV |
| [BondageLevel] | <code>number</code> | The required bondage skill level for this type (optional) |
| [SelfBondageLevel] | <code>number</code> | The required self-bondage skill level for this type when using it on yourself (optional) |
| Property | <code>Property</code> | The Property object to be applied when this option is used |
