# Asset Creation 1 - The Basics

## The Asset Drawing System - Key Concepts

Before we dive into creating assets, it's important to understand how they're structure, and how the game's rendering system draws them. There are a few key concepts we're going to look at in this section:
* Groups
* Assets
* Layers
* Priority

### Groups

Every character in the game is made up of several asset groups (or slots as a lot of players refer to them). These are a lot like item slots in traditional RPGs and other games - each group is able to accommodate a single item, or it can be empty (some groups aren't allowed to be empty). Even the character's body parts have their own asset groups (there's one for the upper body, the lower body, the hands, etc.).

### Assets

Assets are the individual items that characters can wear or equip. Each item of clothing, or piece of bondage equipment, or character body part, is an asset. Every asset is assigned to a single asset group. It's quite easy to see how assets map to groups through the game. In the wardrobe, for example:

[TODO: Image of wardrobe screen]

Each row corresponds to a group, and each piece of clothing is a single asset within that group.

### Layers

Every asset is composed of one or more layers. Layers represent the actual images that get drawn When an asset is rendered, and allow asset creators a lot of flexibility and control over how their asset gets rendered, as well as allowing features like multi-coloring (being able to color different parts of an item differently). Each layer represents a single image that will be drawn onto the final character canvas.

[TODO: Image of asset layer breakdown]

### Priority

When the game draws a character, it does this by finding all of the assets equipped on the character, and then drawing every layer for each of those assets on top of each other onto a character canvas. But to do that, we need to know which order to draw them in. Should we draw the panties layer on top of the dress layer? Probably not.

[TODO: Layer breakdown diagram]

In order to tell the game how to correctly order layers, every layer is assigned a _priority_, which is a number telling the game when a layer should be drawn. Layers with higher priorities are drawn later, and therefore appear to render on top of layers with lower priorities.

[TODO: Layer priority example image]

## Summary

In this section, we've learned about groups, assets, layers and priorities, and how they all fit together on the character canvas when the game draws a character. Now that we have a bit of knowledge about how the drawing system works, we're ready to get started and create some assets of our own.

***

| Previous Guide | Next Guide |
|---|---|
| - | [[Part 2: Getting Started\|Asset-Creation-2:-Getting-Started]] |