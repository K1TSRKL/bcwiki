# Creating a new dialog

Dialogs are composed of a text line and one or multiple choices.

## Character

Dialogs are store in csv files which are loaded when a character is created.

When creating an NPC with CharacterLoadNPC("&lt;name&gt;"), the dialog file in the same screen directory named "Dialog_&lt;name&gt;.csv" is loaded.

The current dialog stage can be altered by code by setting the Stage value of the character object.

## Dialog files

Dialog files are csv spreadsheets, with coma as cell separator and double quotes as text delimiters. Each line represent an introduction text or a choice.

* [0] Column A: **stage name**. It is an identifier to make the dialog flow. When a character is created, it's Stage is 0, so all lines with a stage name of 0 are selected.
* [1] Column B: **next stage**. Used with an option, it holds the next stage name when this option is selected. This is an equivalent to "then go to X".
* [2] Column C: **option**. The option is the text that is written as a choice. Normal text are said, while text within parenthesis are mimed or represent actions.
* [3] Column D: **result**. The result is the text displayed on top when the option is selected. If option is blank, the text is shown as an introduction when the dialog is opened.
* [4] Column E: **function**. The function is a code call that is executed when the option is selected.
* [5] Column F: **prerequisite**. Sets a condition for the line to be active. It can either be a boolean or a function. If false, the line is skipped.
* [6] Column G: group
* [7] Column H: trait

### Stage name

You can define any stage name and go to them by referencing them in next stage cells or by code by setting the Stage value of the character. Some stages have a special meaning.

* **PlayerGagged**: the special stage when the player is gagged. It's result is picked even if other ones are defined for the current stage. There can be only one and prerequisites are ignored.
* **0**: this is the default stage


### Option

The options have predefined behaviours when the player is gagged. Speech is garbled and the option does nothing in that case, as the player fail to be understood. Actions are still processed and an option can mix speech and actions. In that case, the option is still processed when picked, even if only a part of the option is understandable.

Option can have placeholders for dynamic text. Outside predefined placeholders which are automatically replaced, they must be replaced by code with CurrentDialog.replace("placeholder name", "replacement text" on the character object. The default placeholders are:

* **DialogPlayerName** is replaced by the player name
* **DialogCharacterName** is replaced by the character name


### Result

Result is a plain text. As for options, results can contain placeholders.

When an option contains a result and goes to a stage that have a result without option, the text from the selected option is used, that is, it has an higher priority over the result without option of the next stage.

When multiple results without option are available for the same stage, because all the prerequisites are met, the first one is selected.

When the player is gagged, the result from the PlayerGagged stage is always picked if it is defined. Otherwise the regular result is picked.


### Function

Function can be either a game engine function, like DialogRemove(), a player function when prefixed by "Player.". Other functions will be prefixed with the screen name so you don't have to repeat it everytime and you can't directly call functions from other screens.


### Prerequisites

Each line of the current stage are read one after an other. If multiple results without options are matching, the first one is displayed.

Prerequisites can be a boolean or a function call. Like function, they are prefixed by the screen name. "Player." functions and "CurrentCharacter." functions will relate to the player object and the character running the dialog respectively.


### Sample

Extract from the maid in the maid head quarters, with only a few lines for better understanding. Some more lines are required for the dialog to handle every cases.

```
PlayerGagged,,,Lovely gag.  Do you need help with it?  Nod if you do.,,,
0,,,You've done a lot for the maid sorority.  You should apply to become a full sister.,,CanBecomeMaid,
0,,"Hello, I'm DialogPlayerName.  Pleased to meet you.","Pleased to meet you too.  I'm DialogCharacterName, I'm responsible to find work for maids.",DialogRemove(),"DialogReputationLess(""Maid"", 9)",
0,,(Nod yes.),(She removes your gag and smiles.)  Much better sweetie.  How can I help you?,MaidUngagPlayer(),CanUngag(),
```

The first line changes the maid's speech when the player is gagged. She will say that instead of any other text.

All other lines are for the stage 0, which is the default one, none have no prerequisites. So if none matches, she will say nothing.

For the first line of this stage, if MaidQuartersCanBecomeMaid (because the screen name is added as prefix) is set to true, she'll say that line. For the second one, the line is picked if DialogReputationLess("Maid", 9) returns true. If both lines would have their prerequisites met, the first line would be picked for the result because it is defined before the other.

This second option is removed when the player picks it, because DialogRemove() is called when this option is picked. It changes the maid's speech by "Please to meet you too.[...]", and has no other effect. If the player was gagged, DialogRemove would not be called even if this choice is picked because it contains no action in the option.

The last lines shows the option "(Nod yes.)", when MaitQuartersCanUngag() returns true. When the player picks that answer, MaidQuartersMaidUngagPlayer() is called. Because there is no next stage, it stays to 0 and check for an other line with the new situation (that is, the player is now not gagged). Because "(Nod yes.)" is between parenthesis, it stays clear even when gagged and has an effect.


## Translation files

Translation files are loaded automatically. Translation files are defined by language in /Scripts/Translation.js. To add a new translation file, you must add the new file in the TranslationDictionary for it to be loaded.

Those translation files are composed of translations grouped by couples of lines. The first line of a couple is the original text, as copied from the dialog csv file, and the following one is the translated one.

Lines starting by ### are comments and are ignored by the translation engine.