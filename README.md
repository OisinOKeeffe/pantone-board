# Pantone Board

I had this idea of a color palette using Pantone cards.

Most color palette tools only allow up to 5 or 6 colors. Personally I don't have a clear idea of which colors I'd like to use, so I wanted a tool that allows me to throw a bunch of them on a blank canvas, move them around and pray for the better (no! I don't want to open Photoshop just to draw some colorful blobs!)

*Sigh*... ok... I admit not the most useful idea I've had. Maybe I just needed something to make me try React for once.

**Disclaimer** I'm not affiliated with Pantone LLC in any way.

## Features

- Built with `create-react-app`
- Unlimited colors

## Todos
- [ ] Each board is created on-the-fly from it's url
- [ ] Decide if duplicate colors are allowed
- [x] Color picker with Add Color button in a single component
- [ ] ColoPicker should keep the last picked color onClose even if the Add Color button was not pressed
- [ ] Newly created color should be placed on the top of the board
- [ ] Rework or design custom full page color picker with swatches or Pantone color grid
- [ ] On resize, constrain all cards to visible canvas

## Design & Implementation decisions

To drag the color cards around I use `react-draggable`. To always have the moving card on top of the others I just increment it's `z-index` value. According to [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/integer) unless you're planning to drag the cards more than 2<sup>15</sup>-1 times you won't have any issue. Either way, when the browser refreshes the cards will have `z-index: 0` but still show up stacking in the order they are defined (default html behavior).

## Third-party Libraries

- [Name That Color library](http://chir.ag/projects/ntc/) by [Chirag Mehta](http://chir.ag/about)
