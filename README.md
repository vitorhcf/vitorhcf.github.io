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
- `link_text`
- `link_url`

## GIFs and assets

If you want project GIFs, add them anywhere in the repo and point each `gif` field to that path. Example:

```yml
gif: docs/assets/projects/chatrex.gif
```

If `gif` is empty, the card shows a placeholder instead of a broken image.
