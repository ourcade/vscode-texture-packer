# Texture Packer for VS Code

Easily create texture atlases for Phaser, Pixi, and more by grouping images into a folder!

[Get it on the VS Code Marketplace here](https://marketplace.visualstudio.com/items?itemName=Ourcade.vscode-texture-packer).

*This repository is mainly used as an issue tracker.

## How it works

Right click on a folder with images and then select `Create Texture Atlas` to pack them into 1 or more atlases.

![create-gif](https://media.giphy.com/media/fBOZNZp60fJ4J6UvnW/giphy.gif)

The `atlas.config.json` created in that folder is used for configuration options. The atlas format is automatically detected based on your project. (Currently works with Phaser 3 or Pixi projects.)

If `prettier` is installed then the JSON files will be formatted like everything else in your project!

## Requirements

This extension only works on desktop versions of VS Code and cannot be run in the browser.

## Atlas Configuration Options

**name**: `string`

_default_: `atlas`

The file name of the generated texture atlases.

---

**format**: `'phaser3' | 'pixi' | 'phaser-hash' | 'json-hash'`

_default_: `json-hash`

This value is automatically detected for Phaser 3 or Pixi projects.

---

**maxWidth**: `number`

_default_: `2048`

The maximum width of an atlas.

---

**maxHeight**: `number`

_default_: `2048`

The maximum height of an atlas.

---

**fixedSize**: `boolean`

_default_: `false`

Will make atlas `maxWidth` x `maxHeight` when set to `true`.

---

**pot**: `boolean`

_default_: `false`

Force atlases to be power of two.

---

**padding**: `number`

_default_: `0`

---

**extrude**: `number`

_default_: `0`

---

**allowRotation**: `boolean`

_default_: `true`

Allow textures to be rotated in the atlas.

---

**shareIdentical**: `boolean`

_default_: `true`

Textures that are the same but have different filenames will only be packed once to optimize atlas size.

---

**allowTrim**: `boolean`

_default_: `true`

Trim empty whitespace to optimize atlas size.

---

**trimMode**: `'trim' | 'crop'`

_default_: `'trim'`

---

**keepExtensions**: `boolean`

_default_: `false`

Keep file extensions in texture frame keys otherwise only the filename will be used.

---

**textureFormat**: `'png' | 'jpg'`

_default_: `png`

---

**algorithm**: `'max-rects' | 'max-rects-bin' | 'optimal'`

_default_: `max-rects-bin`

---

**maxRectsMethod**: `'smart' | 'square' | 'smart-square' | 'smart-area' | 'square-area' | 'smart-square-area'`

_default_: `smart`

---

**maxRectsBinMethod**: `'best-short-side-fit' | 'best-long-side-fit' | 'best-area-fit' | 'bottom-left-rule' | 'contact-point-rule'`

_default_: `best-short-side-fit`

## Got an issue?

This extension is very new and not yet tested in a wide variety of projects or workflows so let us know if something's not working or if there's a use-case that you'd love to see!

Reach out on Twitter [@iamsupertommy](https://twitter.com/iamsupertommy) or [@ourcadehq](https://twitter.com/ourcadehq)

Join the Ourcade Discord: https://discord.gg/p3vfese

## Release Notes

### v0.0.2

##### October 26th, 2022

Initial release with basic texture packing functionality.
