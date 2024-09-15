# Documentation

This is the official doc for the GUICore library for EaglerForge by Oeildelynx.

## Classes

### GuiButton

```js
new GuiButton(id, posX, posY, text)
```

| Argument | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `id` | `integer` | **Required**. The unique button id. |
| `posX` | `integer` | **Required**. The position in the X axis, in Minecraft unit. |
| `posY` | `integer` | **Required**. The position in the X axis, in Minecraft unit. |
| `text` | `string` | **Required**. The text displayed. |

**Properties:**
| Property | Type     | Description                | Default |
| :-------- | :------- | :------------------------- | :-----|
| `id` | `integer` | The unique button id. | |
| `posX` | `integer` | The position in the X axis, in Minecraft unit. | |
| `posY` | `integer` | The position in the X axis, in Minecraft unit. | |
| `text` | `string` | The text displayed. | |
| `enabled` | `boolean` | If the button is enabled or disabled. If disabled, the button can't be clicked on. |`true` |
| `visible` | `boolean` | If the button is visible or not. |`true` |
| `height` | `integer` | Height of the button, in Minecraft unit. |`20` |
| `width` | `integer` | Height of the button, in Minecraft unit. |`200` |
| `onClick` | `function` | Defines what to do on button click. Has the button class as first parameter.|`200` |

**Functions:**

`isHovered()`, returns a boolean value.

`getRef()`, returns the button Java Object.

`drawToScreen(screen)`, draw the button on the screen if specified, or otherwise in the current screen.

**Example of use:**
```js
let button = new GuiButton(13, 50, 100, 'Click here');
button.width = 150; 
button.onClick = function (button) {
    alert("You clicked on the button with text '" + button.text + "'!");
}
button.drawToScreen() //draw button into the current screen

```
