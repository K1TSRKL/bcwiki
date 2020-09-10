## Constants

<dl>
<dt><a href="#TranslationDictionary">TranslationDictionary</a></dt>
<dd><p>Dictionary for all supported languages and their files</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#TranslationAvailable">TranslationAvailable(FullPath)</a> ⇒ <code>boolean</code></dt>
<dd><p>Checks if a file can be translated in the selected language</p>
</dd>
<dt><a href="#TranslationParseTXT">TranslationParseTXT(str)</a> ⇒ <code>Array.&lt;string&gt;</code></dt>
<dd><p>Parse a TXT translation file and returns it as an array</p>
</dd>
<dt><a href="#TranslationString">TranslationString(S, T, CharacterName)</a> ⇒ <code>string</code></dt>
<dd><p>Translates a string to another language from the array, the translation is always the one right after the english line</p>
</dd>
<dt><a href="#TranslationDialogArray">TranslationDialogArray(C, T)</a> ⇒ <code>void</code></dt>
<dd><p>Translates a character dialog from the specified array</p>
</dd>
<dt><a href="#TranslationTextArray">TranslationTextArray(S, T)</a> ⇒ <code>void</code></dt>
<dd><p>Translates a set of tags. Rerenders the login message when on the login page.</p>
</dd>
<dt><a href="#TranslationDialog">TranslationDialog(C)</a> ⇒ <code>void</code></dt>
<dd><p>Translate a character dialog if the file is in the dictionary</p>
</dd>
<dt><a href="#TranslationText">TranslationText(Text)</a> ⇒ <code>void</code></dt>
<dd><p>Translate an array of tags in the current selected language</p>
</dd>
<dt><a href="#TranslationAssetProcess">TranslationAssetProcess(T)</a> ⇒ <code>void</code></dt>
<dd><p>Translates the asset group and asset descriptions based on the given dictionary</p>
</dd>
<dt><a href="#TranslationAsset">TranslationAsset(Family)</a> ⇒ <code>void</code></dt>
<dd><p>Translates the description of the assets and groups of an asset family</p>
</dd>
<dt><a href="#TranslationNextLanguage">TranslationNextLanguage()</a> ⇒ <code>void</code></dt>
<dd><p>Changes the current language and save the new selected language to local storage</p>
</dd>
<dt><a href="#TranslationLoad">TranslationLoad()</a> ⇒ <code>void</code></dt>
<dd><p>Loads the previous translation language from local storage if it exists</p>
</dd>
</dl>

<a name="TranslationDictionary"></a>

## TranslationDictionary
Dictionary for all supported languages and their files

**Kind**: global constant  
<a name="TranslationAvailable"></a>

## TranslationAvailable(FullPath) ⇒ <code>boolean</code>
Checks if a file can be translated in the selected language

**Kind**: global function  
**Returns**: <code>boolean</code> - - Returns TRUE if a translation is available for the given file  

| Param | Type | Description |
| --- | --- | --- |
| FullPath | <code>string</code> | Full path of the file to check for a corresponding translation file |

<a name="TranslationParseTXT"></a>

## TranslationParseTXT(str) ⇒ <code>Array.&lt;string&gt;</code>
Parse a TXT translation file and returns it as an array

**Kind**: global function  
**Returns**: <code>Array.&lt;string&gt;</code> - - Array of strings with each line divided. For each translated line, the english string precedes the translated one in the array.  

| Param | Type | Description |
| --- | --- | --- |
| str | <code>string</code> | Content of the translation text file |

<a name="TranslationString"></a>

## TranslationString(S, T, CharacterName) ⇒ <code>string</code>
Translates a string to another language from the array, the translation is always the one right after the english line

**Kind**: global function  
**Returns**: <code>string</code> - - The translated string  

| Param | Type | Description |
| --- | --- | --- |
| S | <code>string</code> | The original english string to translate |
| T | <code>Array.&lt;string&gt;</code> | The active translation dictionary |
| CharacterName | <code>string</code> | Name of the character if it is required to replace it within the string. |

<a name="TranslationDialogArray"></a>

## TranslationDialogArray(C, T) ⇒ <code>void</code>
Translates a character dialog from the specified array

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for which we need to translate the dialog array. |
| T | <code>Array.&lt;string&gt;</code> | The active translation dictionary |

<a name="TranslationTextArray"></a>

## TranslationTextArray(S, T) ⇒ <code>void</code>
Translates a set of tags. Rerenders the login message when on the login page.

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| S | <code>Array.&lt;{Tag: string, Value: string}&gt;</code> | Array of current tag-value pairs |
| T | <code>Array.&lt;string&gt;</code> | The active translation dictionary |

<a name="TranslationDialog"></a>

## TranslationDialog(C) ⇒ <code>void</code>
Translate a character dialog if the file is in the dictionary

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| C | <code>Character</code> | The character for which we want to translate the dialog |

<a name="TranslationText"></a>

## TranslationText(Text) ⇒ <code>void</code>
Translate an array of tags in the current selected language

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Text | <code>Array.&lt;{Tag: string, Value: string}&gt;</code> | Array of current tag-value pairs |

<a name="TranslationAssetProcess"></a>

## TranslationAssetProcess(T) ⇒ <code>void</code>
Translates the asset group and asset descriptions based on the given dictionary

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| T | <code>Array.&lt;string&gt;</code> | The active translation dictionary |

<a name="TranslationAsset"></a>

## TranslationAsset(Family) ⇒ <code>void</code>
Translates the description of the assets and groups of an asset family

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| Family | <code>string</code> | Name of the asset family to translate |

<a name="TranslationNextLanguage"></a>

## TranslationNextLanguage() ⇒ <code>void</code>
Changes the current language and save the new selected language to local storage

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
<a name="TranslationLoad"></a>

## TranslationLoad() ⇒ <code>void</code>
Loads the previous translation language from local storage if it exists

**Kind**: global function  
**Returns**: <code>void</code> - - Nothing  
