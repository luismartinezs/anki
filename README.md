# Anki card creator helper

## Setup

- Install VSCODE
- Install VSCODE extension https://marketplace.visualstudio.com/items?itemName=jasew.anki
- Install Anki if you haven't https://apps.ankiweb.net/
- Install Anki addon AnkiConnect https://ankiweb.net/shared/info/2055492159
  - You need Anki version 2.1.0 or above
  - Copy the code `2055492159` and paste it in Anki app > Tools > Add-ons > Get Add-ons...
- Open file called `anki.md`
- Read this to understand how cards are added:

# Your Deck title
##
Front of the card
%
Back of the card
[#my-tag-1]()[#my-tag-2]()

  - Whatever you add in between ## and % is the front of the card
  - After % is the back of the card
  - The thing inside [#__here__]() is a tag, and MUST be preceded by #
  - A new ## indicates the start of a new card
  - The # line is the optional deck title, you can use it to specific to what deck to add the cards
- If you want to add code to a card, do it like this example:

##
```js
let item = arr.____(
  el => el.id === 123
  );
```
%
```js
let item = arr.find(
  el => el.id === 123
  );
```
[#js]()

- Once you have your set of cards, `ctrl+shift+P`, then type `Deck`. Select `Anki: Send to Own Deck`.
- Your cards should be now in Anki ready to study

## Tips

- Format cards with `ctrl+shift+I` (Linux). I've configured the line width to fit anki card, so text will autowrap on format.
  - You can change this configuration in the file `.vscode/settings.json`
- Leave a blank line in between lines of text that should not merge on formatting. See the example in [anki-example.md](./anki-example.md)
- Open a preview side to side, to see how cards will look (`ctrl+K, V` on Linux)
- Don't use ## or % in an empty line inside a card
- Wrap any code in ` for inline code, or in ``` for a code block. See the example in [anki-example.md](./anki-example.md)