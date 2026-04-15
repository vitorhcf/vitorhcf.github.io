# vitorhcf.github.io

Personal Jekyll homepage for `vitorhcf.github.io`.

## Content editing

The homepage pulls its main content from [_config.yml](/mnt/ssd/programs/vitorhcf.github.io/_config.yml):

- `title`: your name at the top
- `logo`: your profile photo
- `description`: the paragraph below your name
- `projects`: the five stacked project sections

Each project supports:

- `title`
- `description`
- `gif`
- `media`
- `link_url`

## GIFs and assets

If you want a single preview, keep using `gif`:

```yml
gif: docs/assets/projects/chatrex.gif
```

If you want multiple previews in the same project card, use `media` with one or more image/GIF paths. Each preview opens in a new tab when clicked.

```yml
media:
  - docs/assets/projects/chatrex-1.png
  - docs/assets/projects/chatrex-2.png
  - docs/assets/projects/chatrex-demo.gif
```

If `media` is present, it takes priority over `gif`. If `link_url` is set, the card shows a "More information" link below the description. If both `media` and `gif` are empty, the card shows a placeholder instead of a broken image.
