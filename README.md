# t3bingo-data
This is a repository with data files powering t3bingo.

The data files have the following structure:

```typst
// Imports small() and a couple of other utilities.
#import "./_lib.typ": *

// The date when this objective unlocks, either none or a valid datetime.
// If filled out and the date at the time of the build is earlier, the
// cell will be displayed as faded out.
// see https://typst.app/docs/reference/foundations/datetime/
#let unlockDate = none

// The description of the objective. Avoid making a way too long
// description, as this can get trimmed. You can use small[...] to make
// the text smaller. If filled out, highlights the cell with blue color.
#let description = []

// The official name (1st-level hint of the objective). If filled out
// and the description is missing, highlights the cell with pink color.
#let officialName = []

// If objective hiding is applied, hides the cell
#let hidden = false

// Overrides the color of the cell highlight. Usually, this is used when
// marking objectives as having an uncertain solution.
// If set to none or omitted, default highlighting rules are used.
// As of writing, the following colors are accepted:
// "default", "uncertain", "errata", "locked", "hintless"
#let colorType = none
```

## Contributing
Contributions are welcome. Make sure to follow a couple rules of thumb:
- Keep the solutions short (roughly 100-120 characters). If you really must make it longer, use the `small[]` function where appropriate. Your solution may be reworded if it doesn't.
- Images go into the `images/` directory.

## License
See the [LICENSE](LICENSE) file.
