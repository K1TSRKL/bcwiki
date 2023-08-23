## Getting started with adding an asset

### Asset definitions and related files

The assets used by BC are defined in the *huge* [Female3DCG.js](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/Female3DCG.js) file, which contains everything from group configuration, asset definitions, poses, and activities, though the part that's most useful to add an asset is obviously the group/asset definitions, a.k.a [AssetFemale3DCG](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/Female3DCG.js#L35). Another file that will be useful (or might already be, depending on your IDE) is the [Typescript definitions](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/Female3DCG_Types.d.ts) for `Female3DCG.js`, where we've tried to document as much properties and their advanced usage as possible to make that available through your IDE's Intellisense.

All of an assets' layers are stored in a hierarchy that starts next to the `Female3DCG.js` file, which goes like this:
`$GROUP/$POSE/$ASSET_$LAYER.png`, with `$POSE` and `_$LAYER` being optional for the base pose and no layer definitions respectively. You'll have to be cautious about getting the case right; BC is served from a case-sensitive server, hence `.PNG` and `.png` is *not* the same thing in that context (even though locally you can get away with it).

Other files that you might need to edit are:
- the human-readable names for asset and group names in [Female3DCG.csv](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/Female3DCG.csv).
- the human-readable names for layer names in [LayerNames.csv](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/LayerNames.csv), which are needed if your asset has any layers.
- the human-readable names for color groups in [ColorGroups.csv](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/ColorGroups.csv), which are needed if your asset's layers use color groups.
- the dialog used for the player character in [Dialog_Player.csv](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Screens/Character/Player/Dialog_Player.csv), which should contain translations for any of the messages your asset might want to display in chat — though a simple asset should not need any.
- lastly, the extended definitions for assets can be found in [Female3DCGExtended.js](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/Female3DCGExtended.js), though depending on your asset you might not need it.

### "Simple" assets

We're gonna go into the steps of creating a new asset, starting with the basics and slowly building up until we get to see most of the features they have. For now, we'll only consider a single-layer, non-extended asset, since the base setup is the same for every sort.

BC classifies assets into three "types": body parts, clothing, and restraints, though the meaning of the last one is fuzzy. To clarify, restraints are anything you can use on a character directly from the chat room. Clothing and body parts are usually only ever changed from the wardrobe screen.

The first thing you'll need to do is find the position of the group you want your asset to go in; this will depend on what type of asset you're working on (clothing, body part, or restraint), and where you want the asset to appear — its group, in other words. Since the defininition file is so big, a good way to orient yourself in it is to search for `Group: "$GROUPNAME"`, replacing `$GROUPNAME` with the name of the group you're looking for, so `ItemArms`, `Cloth`, `ItemDevices`.

Once you've located the group definition, you'll see something like this:
```js
{
    Group: "ItemBreast",
    ParentGroup: "BodyUpper",
    Category: "Item",
    Priority: 16,
    Default: false,
    Left: 150,
    Top: 200,
    AllowPose: ["AllFours"],
    Zone: [[300, 270, 100, 70]],
    Asset: [
        /* snip */
    ],
}
```

This is the definition for the `ItemBreast` group, which is not terribly impressive but it contains a few properties that are inherited by any assets it contains (most notably `Priority`, `Left`/`Top`, and `AllowPose` but there are more), and which you'll have to keep in mind while writing your asset.

Now scroll down until you reach the end of that group's `Asset` array, and add a new entry for your asset. As an example, here's the bare minimum needed to get BC to register your asset:

```js
{
    Name: "$MYASSET", Value: 0,
}
```

`Name` in this context is the asset's internal identifier, which must be unique, and `Value` is how much it costs in the shop. Setting it at 0 has the side-effect of making it available to everyone, which is useful when starting though you might want to assign it an appropriate value once you're done building. But that should be enough to get your asset to show up in BC, and get it applied (though it most likely won't have any graphics at that point).

There are a lot of properties you can use at that point to customize how your asset should behave. I'll go over some of the more usual categories, but you can look at the documentation in [Female3DCG_Types.d.ts](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Assets/Female3DCG/Female3DCG_Types.d.ts) for the full list.

#### Poses

There are a few properties related to pose support (which would impact how many layers you have to provide and where to save them), but `AllowPose` is the main one. This property is inherited from the asset's group, so you might need to redefine it entirely if it conflicts with your plans. BC will use that list to know that it must load alternative files if the character is in a given pose; by default it'll use the base version always.

Another property would be `AllowActivePose`, which isn't often used but allows to keep some poses available for switching around once the asset is worn — since generally BC will consider an asset to prevent pose changes. The petsuit uses it to give players the ability to move on all fours and back on her knees. The opposite of that would be `FreezeActivePose`, which blocks changes to the specified pose "categories" (mostly upper & lower body pose).

#### Hides

You can hide whole groups using `Hide`, which is useful for things like hoods if you want to make hair vanish, but can be used to bend the rules a bit (like hiding the whole upper body if your asset fully covers it). There's a more finer-grained variant that takes specific items, which is usually reserved for special clipping issues an asset might have when used along with yours, but you can't afford to hide the whole group its in.

#### Blocks

These define which groups get blocked when your asset is applied, preventing other assets to be added and removed from another group. Note that you can only block restraint groups; clothing and body groups don't use that system at all.

#### Prerequisites

Those go into a `Prerequisite` property, which contains a list of identifiers BC uses to prevent your asset from being added to someone (like, the character must wear cuffs, or must be able to spread their legs, or kneel, or be in a bed, etc…). Sadly we don't yet have a full documented list of those, but they're all defined in [InventoryPrerequisiteMessage](https://gitgud.io/BondageProjects/Bondage-College/-/blob/master/BondageClub/Scripts/Inventory.js#L184).

#### Layers

WIP

### Extended assets

WIP

### Caveats

* Be very careful about case-sensitivity and layer files. This can cause failures once your asset gets merged and the beta start, as any discrepancy will cause 404 errors and missing layers.

* When BC loads, it will go through that array and build its own runtime representation of assets which is usually the same but has some slight differences, like `Priority` in your definition becomes `DrawPriority` once loaded. If you're playing around in the console trying to find appropriate values, a discrepancy like that could explain why it's not working as intended.

| Previous Guide | Next Guide |
|---|---|
| [[Part 1 - The Basics\|Asset-Creation-1---The-Basics]] | - |
