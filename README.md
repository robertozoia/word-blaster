# Word Blaster

A Roblox-style 3D vocabulary game (German / English / Spanish). Shoot the noob carrying the right translation before it catches you.

Play: open `word-blaster.html` (or the GitHub Pages link). Works with keyboard + mouse and with touch on iPad.

## Vocabulary sets

The word lists live in the `SETS` array at the top of the script in `word-blaster.html`. Each set is picked on the start menu and played on its own; records are saved per set. A set looks like this:

```js
{ id:'de-l37-38',                                   // stable id, used for saved records
  name:{ es:'Alemán · Lección 37+38', de:'…', en:'…' },  // button label per UI language
  langs:['de','es'],                                // language of each column of `words`
  modes:[ { prompt:[0], answer:1 },                 // columns shown as the prompt -> column on the signs
          { prompt:[1], answer:0 } ],
  words:[ ["feiern","celebrar"], … ] }
```

To add a new list, append another entry to `SETS`. The `.md` files in this folder are the source sheets for each set.
