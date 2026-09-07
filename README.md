<p>
  Moonfly is a dark charcoal colour scheme with muted, low-saturation accents —
  originally a Vim and Neovim theme by
  <a href="https://github.com/bluz71">bluz71</a>. This is the lich port.
</p>

Upstream theme repo: [bluz71/vim-moonfly-colors](https://github.com/bluz71/vim-moonfly-colors)

### Installation

[lich](https://github.com/omartelo/lich) installs a theme repository from its
URL — nothing to download or copy by hand:

1. Open lich and go to **Settings → Appearance**.
2. Next to **Theme**, click **Import**.
3. Paste `https://github.com/omartelo/moonfly-lich` and click **Install**.
4. Pick **Moonfly** in the theme picker. The terminal picker defaults to
   **Match app**, so one pick dresses the interface and the terminal panes
   alike.

Later releases are taken with **Update** on the theme's row.

### How the palette maps

Moonfly builds its chrome out of a charcoal-grey ladder rather than tinted
surfaces, so lich's surface tokens take the greys upstream uses for the same
roles — `#080808` stays the canvas and nothing drifts to mid-grey:

| Moonfly | lich |
|---|---|
| `black` `#080808` | `background` — the app ground, and `Normal` upstream |
| `grey7` `#121212` | `sidebar` — upstream's `TablineSel` / `ColorColumn` rung |
| `grey11` `#1c1c1c` | `card` — tabs, footer, dock; upstream's `CursorLine` / `StatusLine` |
| `grey13` `#212121` | `popover`, `muted` — upstream's `Pmenu` |
| `grey16` `#292929` | `secondary` — upstream's `Tabline` |
| `grey18` `#2e2e2e` | `border` — hairline seams, upstream's `FloatBorder` |
| `grey27` `#444444` | `input` — control edges, a step stronger than `border` |
| `grey0` `#323437` | `accent` — hover and selected fills, upstream's `Visual` |
| `grey58` `#949494` | `muted-foreground` — secondary text, paths, resting icons; upstream's `Comment` |
| `white` `#c6c6c6` | `foreground` |
| `blue` `#80a0ff` | `primary` — the one high-emphasis fill; upstream's active tab and `CursorLineNr` |
| `red` `#ff5d5d` | `destructive` |
| `turquoise` `#79dac8` | `ring` — the focus ring; kept off `primary` so a focused blue button still shows one |

The terminal palette is the upstream
[kitty port](https://github.com/bluz71/vim-moonfly-colors/blob/master/extras/moonfly-kitty.conf)
verbatim, cursor and selection included.

### Thanks to

- [bluz71](https://github.com/bluz71) — original palette
- [omartelo](https://github.com/omartelo) — lich port

### Contributing

The theme is one file, `moonfly.json`, beside the `lich-theme.json` manifest that
carries the pack's version. There is no generator: colors are edited directly in
the theme file.

To propose a tweak:

1. Fork the repo.
2. Edit `moonfly.json`.
3. Validate the **whole directory** — a repository installs all or nothing:
   `node validate.mjs .` (ships with the lich `theme` skill).
4. Bump `version` in `lich-theme.json` in the same commit. An unbumped version
   ships nothing: **Update** compares only that number.
5. Open a PR.

### License

[MIT](./LICENSE)
