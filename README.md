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

Your `md` file will look like this:

```md
# Your Deck title

##

Front of the card

%

Back of the card

[#my-tag-1]()[#my-tag-2]()

##

Front of the next card

%

Back of the next card

[#my-tag-3]()[#my-tag-4]()
```

- The `#` line at the top is the optional deck title, you can use it to specify to what deck to add the cards
- A new `##` indicates the start of a new card
- Whatever you add in between `##` and `%` is the front of the card
- After `%` comes the back of the card
- The thing inside `[#__here__]()` is a tag, and MUST be preceded by `#`
- If you want to add code to a card, see the examples in [anki-example](./anki-example.md)
- Auto-format the file: `ctrl+shift+P`, type `format` and select `Format Document`
- Once you have your set of cards, `ctrl+shift+P`, then type `Deck`. Select `Anki: Send to Own Deck`.
- Your cards should be now in Anki ready to study

## Quickly add cards

To quicky add a card to a markdown file, type `anki`, and from the autosuggestions, select either `anki-new-card` or `anki-new-card-with-code`.

## Tips

- Format cards with: `ctrl+shift+P`, type `format` and select `Format Document`. I've configured the line width to fit anki card, so text will autowrap on format.
  - You can change this configuration in the file `.vscode/settings.json`
- Leave a blank line in between lines of text that should not merge on formatting. See the example in [anki-example.md](./anki-example.md)
- Open a Markdown preview to the side, to see how cards will look (`ctrl+K, V` on Linux and Windows)
- Don't use `##` or `%` in an empty line inside a card
- Wrap any code in ` for inline code, or in ``` for a code block. See the example in [anki-example.md](./anki-example.md)
- Leave an empty line before and after `%` so autoformatting doesn't mess up with it