# BrandOptions

The four brand options. A company picks one and sets it on the page root with the `data-brand` attribute: `<html data-theme="light" data-brand="petrol">`. For a company color that is not in the list, make a fifth option with the same seven tokens and check the same contrast pairs.

Each option sets `--brand`, `--brand-hover`, `--brand-pressed`, `--brand-subtle`, `--on-brand`, `--link` and `--focus` together, for each theme (rules at the end of `components/bundle.css`). Do not set `--brand` alone.

| option | light fill | white label | dark fill | white label | dark link on canvas |
|---|---|---|---|---|---|
| navy (default) | #0e447f | 9.8:1 | #2e68ad | 5.7:1 | #7fa9da, 7.8:1 |
| petrol | #00636b | 7.0:1 | #0e7880 | 5.2:1 | #5ec4cb, 9.2:1 |
| crimson | #a3122e | 7.8:1 | #b8253f | 6.2:1 | #f28b9a, 8.1:1 |
| graphite | #2b3138 | 13.1:1 | #4a5563 | 7.6:1 | #c3cbd5, 11.6:1 |

In the light theme the link color is the brand fill. In the dark theme the fill stays dark enough for a white label and the link uses a lighter tint. With crimson, errors keep their icon and text, so they do not look like brand.
