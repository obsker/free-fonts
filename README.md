# Obsker Type Foundry

Six original typeface families by **Obsker**, supplied as web-ready WOFF and
WOFF2 files. Each family is licensed under the MIT License; see [LICENSE](LICENSE)
for the full terms.

## Font files

| File | Family | Format | Styles and variation axes | First release |
| --- | --- | --- | --- |
| `obsker-fable.woff` | Obsker Fable | WOFF | Variable weight (`wght`: 100–900; default 500) | 2025-03-14 |
| `obsker-kestrel.woff2` | Obsker Kestrel | WOFF2 | Variable weight (`wght`: 100–900) and italic (`ital`: 0–1) | 2025-06-22 |
| `obsker-parallax.woff2` | Obsker Parallax | WOFF2 | Variable weight (`wght`: 300–900), italic (`ital`: 0–10), and `MONO` (`0–100`) | 2025-09-07 |
| `obsker-morrow.woff2` | Obsker Morrow | WOFF2 | Static | 2026-01-18 |
| `obsker-rift.woff2` | Obsker Rift | WOFF2 | Static | 2026-05-11 |
| `obsker-trellis.woff2` | Obsker Trellis | WOFF2 | Variable weight (`wght`: 100–900) | 2026-10-23 |

Axis ranges are read from each file's OpenType `fvar` table. The `ital` axis
uses `0` for upright and `1` for italic in Kestrel. Parallax uses `0` for
upright and `10` for italic, preserving that family's existing interpolation
range. This differs from the usual `ital` range of `0` to `1`. `MONO` is a
custom axis ranging from proportional (`0`) to monospaced (`100`); applications
can control it with `font-variation-settings`.

## Web use

Declare the family and supported weight range in CSS so browsers can select
intermediate weights:

```css
@font-face {
  font-family: "Obsker Kestrel";
  src: url("./obsker-kestrel.woff2") format("woff2");
  font-style: normal;
  font-weight: 100 900;
  font-display: swap;
}

body {
  font-family: "Obsker Kestrel", sans-serif;
  font-weight: 450;
}
```

For `Obsker Parallax`, set the custom axis when needed:

```css
.obsker-parallax-mono {
  font-variation-settings: "MONO" 100;
}
```

## Attribution and license

Designed and published by **Obsker**. Copyright © 2025–2026 Obsker. The font
software is licensed under the MIT License. Redistribution must include the
copyright and permission notice in [LICENSE](LICENSE).

## Metadata and versioning

The OpenType family, designer, manufacturer, license, axis, and named-instance
metadata identifies Obsker and matches the files in this collection. All six
families are at their first release: OpenType version `1.000` (font revision
`1.0`). Nonstandard named weights retain their numeric value alongside the
nearest conventional style name, so instance labels stay clear without
changing the font's design space.
