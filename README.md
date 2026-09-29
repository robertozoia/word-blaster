# Word Blaster

A Roblox-style 3D vocabulary game (German / English / Spanish). Shoot the noob carrying the right translation before it catches you.

Play: open `word-blaster.html` (or the GitHub Pages link). Works with keyboard + mouse and with touch on iPad.

## Play styles

- **Shoot** (default): aim at the noob carrying the right translation and shoot it.
- **Type**: the noobs still carry the candidate words, but you type the translation of the prompt and press Enter. A correct entry blasts the matching noob. Typing the text of a *wrong* sign costs a heart, exactly like shooting the wrong noob; text that matches no sign just shakes the box and resets the combo. Arrow keys move, Esc pauses. On iPad, tap the box to open the keyboard and use the left-half joystick to move.

Matching is lenient: case and accents are ignored (`Staedte` counts for `Städte`), the plural part after the comma and notes like `(Sg.)` are dropped, any alternative separated by `/` is accepted, and a leading article or particle (`der/die/das`, `el/la/los/las`, `the`, `to`, `sich`) is optional. Records are stored separately per play style.

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
