## Functions

<dl>
<dt><a href="#SkillChange">SkillChange(SkillType, SkillLevel, SkillProgress, [Push])</a> ⇒ <code>void</code></dt>
<dd><p>When the player progresses in a skill. Also validates the values to make sure they are within the proper ranges once changed. (level 0-10, progress 0-100)</p>
</dd>
<dt><a href="#SkillLoad">SkillLoad(NewSkill)</a> ⇒ <code>void</code></dt>
<dd><p>Loads the skill data from the server on login</p>
</dd>
<dt><a href="#SkillGetLevel">SkillGetLevel(C, SkillType)</a> ⇒ <code>number</code></dt>
<dd><p>Get a specific skill level from a character WITH the current modifier applied</p>
</dd>
<dt><a href="#SkillGetLevelReal">SkillGetLevelReal(C, SkillType)</a> ⇒ <code>number</code></dt>
<dd><p>Get a specific skill level from a character WITHOUT the modifier applied</p>
</dd>
<dt><a href="#SkillGetProgress">SkillGetProgress(C, SkillType)</a> ⇒ <code>number</code></dt>
<dd><p>Get a specific skill progress from a character</p>
</dd>
<dt><a href="#SkillProgress">SkillProgress(SkillType, SkillProgress)</a> ⇒ <code>void</code></dt>
<dd><p>Add progress to a skill, the skill progresses slower for each level, takes into account cheaters version.</p>
</dd>
<dt><a href="#SkillSetRatio">SkillSetRatio(SkillType, Ratio, [Push])</a></dt>
<dd><p>Sets the ratio % of a skill that&#39;s going to be used by the player</p>
</dd>
<dt><a href="#SkillGetRatio">SkillGetRatio(SkillType)</a> ⇒ <code>number</code></dt>
<dd><p>Gets the ratio % of effectiveness of a skill for the player</p>
</dd>
<dt><a href="#SkillGetWithRatio">SkillGetWithRatio(SkillType)</a> ⇒ <code>number</code></dt>
<dd><p>Gets a skill level with the current ratio applied to it, if the current skill has a % modifier.</p>
</dd>
<dt><a href="#SkillModifierChange">SkillModifierChange()</a> ⇒ <code>void</code></dt>
<dd><p>Alters the current skill modifier for the player (Stays within -10 to 10)</p>
</dd>
</dl>

<a name="SkillChange"></a>

## SkillChange(SkillType, SkillLevel, SkillProgress, [Push]) ⇒ <code>void</code>
When the player progresses in a skill. Also validates the values to make sure they are within the proper ranges once changed. (level 0-10, progress 0-100)

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| SkillType | <code>string</code> |  | Name of the skill to set the value for |
| SkillLevel | <code>number</code> |  | Level to set for the given skill |
| SkillProgress | <code>number</code> |  | Progress to set for the given skill |
| [Push] | <code>boolean</code> | <code>true</code> | Pushes the skills to the server if TRUE |

<a name="SkillLoad"></a>

## SkillLoad(NewSkill) ⇒ <code>void</code>
Loads the skill data from the server on login

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| NewSkill | <code>Array.&lt;{Type: string, Level: number, Progress: number}&gt;</code> | The player skills array sent by the server |

<a name="SkillGetLevel"></a>

## SkillGetLevel(C, SkillType) ⇒ <code>number</code>
Get a specific skill level from a character WITH the current modifier applied

**Kind**: global function  
**Returns**: <code>number</code> - - Current level for the given skill.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which we want to query a skill |
| SkillType | <code>string</code> | Name of the skill to get the value of |

<a name="SkillGetLevelReal"></a>

## SkillGetLevelReal(C, SkillType) ⇒ <code>number</code>
Get a specific skill level from a character WITHOUT the modifier applied

**Kind**: global function  
**Returns**: <code>number</code> - - Current real level for the given skill.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which we want to query a skill |
| SkillType | <code>string</code> | Name of the skill to get the value of |

<a name="SkillGetProgress"></a>

## SkillGetProgress(C, SkillType) ⇒ <code>number</code>
Get a specific skill progress from a character

**Kind**: global function  
**Returns**: <code>number</code> - - Current progress for the given skill.  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | Character for which we want to query a skill |
| SkillType | <code>string</code> | Name of the skill to get the progress of |

<a name="SkillProgress"></a>

## SkillProgress(SkillType, SkillProgress) ⇒ <code>void</code>
Add progress to a skill, the skill progresses slower for each level, takes into account cheaters version.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| SkillType | <code>string</code> | Name of the skill to add progress to |
| SkillProgress | <code>number</code> | Progress to be made before the ratios are applied |

<a name="SkillSetRatio"></a>

## SkillSetRatio(SkillType, Ratio, [Push])
Sets the ratio % of a skill that's going to be used by the player

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| SkillType | <code>string</code> |  | Name of the skill to get the value of |
| Ratio | <code>number</code> |  | The ratio to set for a given skill (0 to 1) |
| [Push] | <code>boolean</code> | <code>true</code> | Pushes the skills to the server if TRUE |

<a name="SkillGetRatio"></a>

## SkillGetRatio(SkillType) ⇒ <code>number</code>
Gets the ratio % of effectiveness of a skill for the player

**Kind**: global function  
**Returns**: <code>number</code> - - The current active ratio for the given skill  

| Param | Type | Description |
| --- | --- | --- |
| SkillType | <code>string</code> | Name of the skill to get the value of |

<a name="SkillGetWithRatio"></a>

## SkillGetWithRatio(SkillType) ⇒ <code>number</code>
Gets a skill level with the current ratio applied to it, if the current skill has a % modifier.

**Kind**: global function  
**Returns**: <code>number</code> - - The skill level with the ratio % applied  

| Param | Type | Description |
| --- | --- | --- |
| SkillType | <code>string</code> | Name of the skill to get the value of |

<a name="SkillModifierChange"></a>

## SkillModifierChange() ⇒ <code>void</code>
Alters the current skill modifier for the player (Stays within -10 to 10)

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
