## Functions

<dl>
<dt><a href="#AssetBuildLayer">AssetBuildLayer(AssetDefinition, A)</a> ⇒ <code><a href="#Layer">Array.&lt;Layer&gt;</a></code></dt>
<dd><p>Builds the layer array for an asset based on the asset definition. One layer is created for each drawable part of the asset (excluding
the lock). If the asset definition contains no layer definitions, a default layer definition will be created.</p>
</dd>
<dt><a href="#AssetMapLayer">AssetMapLayer(Layer, AssetDefinition, A, I)</a> ⇒ <code><a href="#Layer">Layer</a></code></dt>
<dd><p>Maps a layer definition to a drawable layer object</p>
</dd>
<dt><a href="#AssetLayerAllowColorize">AssetLayerAllowColorize(Layer, NewAsset)</a> ⇒ <code>boolean</code></dt>
<dd><p>Determines whether a layer can be colorized, based on the layer definition and its parent asset/group definitions</p>
</dd>
<dt><a href="#AssetLayerAlpha">AssetLayerAlpha(Layer, NewAsset, I)</a> ⇒ <code><a href="#AlphaDefinition">Array.&lt;AlphaDefinition&gt;</a></code></dt>
<dd><p>Builds the alpha mask definitions for a layer, based on the</p>
</dd>
<dt><a href="#AssetCleanArray">AssetCleanArray(AssetArray)</a> ⇒ <code>Array.&lt;{Name: string, Group: string}&gt;</code></dt>
<dd><p>Cleans the given array of assets of any items that no longer exists</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#Layer">Layer</a> : <code>Object</code></dt>
<dd><p>An object defining a drawable layer of an asset</p>
</dd>
<dt><a href="#AlphaDefinition">AlphaDefinition</a></dt>
<dd><p>An object defining a group of alpha masks to be applied when drawing an asset layer</p>
</dd>
</dl>

<a name="AssetBuildLayer"></a>

## AssetBuildLayer(AssetDefinition, A) ⇒ [<code>Array.&lt;Layer&gt;</code>](#Layer)
Builds the layer array for an asset based on the asset definition. One layer is created for each drawable part of the asset (excluding
the lock). If the asset definition contains no layer definitions, a default layer definition will be created.

**Kind**: global function  
**Returns**: [<code>Array.&lt;Layer&gt;</code>](#Layer) - - An array of layer objects representing the drawable layers of the asset  

| Param | Type | Description |
| --- | --- | --- |
| AssetDefinition | <code>Object</code> | The raw asset definition |
| A | <code>Asset</code> | The built asset |

<a name="AssetMapLayer"></a>

## AssetMapLayer(Layer, AssetDefinition, A, I) ⇒ [<code>Layer</code>](#Layer)
Maps a layer definition to a drawable layer object

**Kind**: global function  
**Returns**: [<code>Layer</code>](#Layer) - - A Layer object representing the drawable properties of the given layer  

| Param | Type | Description |
| --- | --- | --- |
| Layer | <code>Object</code> | The raw layer definition |
| AssetDefinition | <code>Object</code> | The raw asset definition |
| A | <code>Asset</code> | The built asset |
| I | <code>number</code> | The index of the layer within the asset |

<a name="AssetLayerAllowColorize"></a>

## AssetLayerAllowColorize(Layer, NewAsset) ⇒ <code>boolean</code>
Determines whether a layer can be colorized, based on the layer definition and its parent asset/group definitions

**Kind**: global function  
**Returns**: <code>boolean</code> - - Whether or not the layer should be permit colors  

| Param | Type | Description |
| --- | --- | --- |
| Layer | <code>Object</code> | The raw layer definition |
| NewAsset | <code>Object</code> | The raw asset definition |

<a name="AssetLayerAlpha"></a>

## AssetLayerAlpha(Layer, NewAsset, I) ⇒ [<code>Array.&lt;AlphaDefinition&gt;</code>](#AlphaDefinition)
Builds the alpha mask definitions for a layer, based on the

**Kind**: global function  
**Returns**: [<code>Array.&lt;AlphaDefinition&gt;</code>](#AlphaDefinition) - - a list of alpha mask definitions for the layer  

| Param | Type | Description |
| --- | --- | --- |
| Layer | <code>Object</code> | The raw layer definition |
| NewAsset | <code>Object</code> | The raw asset definition |
| I | <code>number</code> | The index of the layer within its asset |

<a name="AssetCleanArray"></a>

## AssetCleanArray(AssetArray) ⇒ <code>Array.&lt;{Name: string, Group: string}&gt;</code>
Cleans the given array of assets of any items that no longer exists

**Kind**: global function  
**Returns**: <code>Array.&lt;{Name: string, Group: string}&gt;</code> - - The cleaned up array  

| Param | Type | Description |
| --- | --- | --- |
| AssetArray | <code>Array.&lt;{Name: string, Group: string}&gt;</code> | The arrays of items to clean |

<a name="Layer"></a>

## Layer : <code>Object</code>
An object defining a drawable layer of an asset

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| Name | <code>string</code> \| <code>null</code> | the name of the layer - may be null if the asset only contains a single default layer |
| AllowColorize | <code>boolean</code> | whether or not this layer can be colored |
| AllowTypes | <code>Array.&lt;string&gt;</code> \| <code>null</code> | A list of allowed extended item types that this layer permits - the layer will only be drawn if the item type matches one of these types. If null, the layer is considered to permit all extended types. |
| HasType | <code>boolean</code> | whether or not the layer has separate assets per type. If not, the extended type will not be included in the URL when fetching the layer's image |
| [ParentGroupName] | <code>string</code> \| <code>null</code> | The name of the parent group for this layer. If null, the layer has no parent group. If undefined, the layer inherits its parent group from it's asset/group. |
| OverrideAllowPose | <code>Array.&lt;string&gt;</code> \| <code>null</code> | An array of poses that this layer permits. If set, it will override the poses permitted by the parent asset/group. |
| Priority | <code>number</code> | The drawing priority of this layer. Inherited from the parent asset/group if not specified in the layer     definition. |
| Asset | <code>Asset</code> | The asset that this layer belongs to |

<a name="AlphaDefinition"></a>

## AlphaDefinition
An object defining a group of alpha masks to be applied when drawing an asset layer

**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| [Group] | <code>Array.&lt;string&gt;</code> | A list of the group names that the given alpha masks should be applied to. If empty or not present, the alpha masks will be applied to every layer underneath the present one. |
| [Pose] | <code>Array.&lt;string&gt;</code> | A list of the poses that the given alpha masks should be applied to. If empty or not present, the alpha masks will be applied regardless of character pose. |
| Masks | <code>Array.&lt;Array.&lt;number&gt;&gt;</code> | A list of alpha mask definitions. A definition is a 4-tuple of numbers defining the top left coordinate of a rectangle and the rectangle's width and height - e.g. [left, top, width, height] |
