# Tale of Talagron

![Scrolling story text](/static/concepts/talagron.jpg)

Maybe you want to introduce your game with a text story line that slowly scrolls so the player can read multiple sentences of your game saga. The game dialogs provide a way display short interactive messages but for text with effects you need something else.

By creating an image, or possibly images for multiple paragraphs, you can have a text object that will scroll on the screen.

This example shows story text prior to the start of gameplay. The text scrolls from the bottom of the screen to the top. Button **A** will pause and resume scrolling. The up and down buttons will scroll the story one line at a time. The sprite containing the text is destroyed when it scrolls off the screen which triggers the start of the game.


```typescript
namespace SpriteKind {
    export const Star = SpriteKind.create();
}

let ship: Sprite = null
let hyper = false
let star: Sprite = null
let scroll = false
let lineAdjust = 0
let sagaSprite: Sprite = null
let sagaImage: Image = null
let storyLines = [
    "TALE OF TALAGRON",
    "",
    "Once upon a time,",
    "like really long ago,",
    "a peaceful people lived",
    "happily on Planet Talagron.",
    "",
    "They used the rare mineral",
    "Xelantium for energy to",
    "power their planet.",
    "",
    "Dobanites raided Talagron",
    "and took all the known",
    "Xelantium from them. Not",
    "nice! Ugh! Err!",
    "",
    "Your mission is to help",
    "protect Talagron from the",
    "greedy Dobanites. So, on",
    "your way now and good luck!"
]
scroll = true
