# Introduction
Drawing hooks are a way to incorporate code that happens during character rendering without adding special cases to other drawing functions. To understand them you must first understand the drawing order:
1. The player sprite is rendered whenever there is a change that requires updating the canvas. It is not redrawn every frame, but it is redrawn whenever a new hook is added or removed.
2. The function in which the drawing happens is CharacterLoadCanvas(C) in Character.js
3. The first thing to note is that as of May 2021, the drawing code refers to two variables which store character appearance and code (DrawAppearance and DrawPose). These are copies of the Appearance and Pose array that are used to allow drawing hooks to change rendering without changing the items or pose on a character. The copies are made at the start of CharacterLoadCanvas(C)
4. Hooks labelled as BeforeSortLayers are run here.
5. The appearance is then sorted into an array of layers using CharacterAppearanceSortLayers(C). These layers are separate from the item, they consist of the layers that are then drawn by the canvas drawing functions. The game code for hiding layers and items happens at this step.
6. Hooks labelled as AfterLoadCanvas are run here.
7. CharacterAppearanceSetHeightModifiers is run to set modifiers based on character height
8. The character canvas is rendered

## BeforeSortLayers
Hooks at this step are usually hooks that modify the DrawAppearance and DrawPose array before the appearance is sorted into layers. Here you can, for example, modify (or hide) an item or change its properties without actually affecting the item. This is useful if you want to hide certain items dynamically, such as with the VR headset's virtual avatar mode.

## AfterLoadCanvas
Hooks at this step are used to modify appearance layers after they have been rendered. For example, you can use this to remove a lid layer that has been drawn over a player character while the character is in a box.

# Creating a hook
Creating a hook has a couple of simple steps:
1. Decide on a condition for the hook to be added to the character
2. Add the hook to CharacterCheckHooks(C, IgnoreHooks), which is run once every drawing frame
3. Unregister the hooks in CharacterCheckHooks(C, IgnoreHooks) when it is no longer relevant

Most hooks are tied to effects. For example, the VR headset uses the HideRestraints effect. Adding this effect to any item will cause it to hide restraints.