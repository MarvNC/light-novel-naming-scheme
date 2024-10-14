# Light Novel Naming Scheme <!-- omit from toc -->

Inspired by the standard
[Daiz/manga-naming-scheme](https://github.com/Daiz/manga-naming-scheme), this
document is a naming scheme for light novels, with a focus on Japanese releases.

- [Goals](#goals)
- [Naming Scheme](#naming-scheme)
  - [Components](#components)
  - [Other](#other)
- [Examples](#examples)

## Goals

Copied from the manga naming scheme:

> - Filenames should always sort properly in chronological chapter order under
>   any and all circumstances.
> - Filenames should never have to be renamed after release to ensure proper
>   sorting.
> - No guessing should ever be necessary when naming files.
> - All filenames should be machine-parseable in a reasonable manner.
> - One should be able to repack multiple archives together.
> - One should be able to repack compilation archives back into separate
>   archives.
> - In other words, repacking should always be a lossless operation
>   information-wise.

**Additional goals:**

- Filenames should respect the original title of the light novel, even when the
  title/subtitle changes between volumes.

## Naming Scheme

```
[Author] v00 - Title (Label)
```

### Components

- `[Author]` - The author of the light novel. If the release is in Japanese, the
  author's name should be in Japanese name order and spelled as originally
  published.
- `v00` - The volume number, padded with zeroes to two digits. As with the manga
  naming scheme, if the volume number goes above 100 then continue with `w100`,
  `w101`, etc.
  - If there is only one volume, the volume number is **still required** as
    `v01` because with light novels the publishing status is often unknown.
- `Title` - The title of the light novel. This should be **untouched from the
  official spelling**, without omitting Arabic/Roman numerals included in the
  original title.
  - If there are bonuses included with the volume, these should be left in the
    title if they are included in the release.
    - `【電子特典付き】` (with digital tokuten) should be included if the
      tokuten is included in the release. If it is a separate `.pdf` file that
      should be released separately.
    - `【ドラマＣＤ音源付き】` (with Drama CD audio) should not be included a
      drama CD will not be included in an `.epub`.
- `(Label)` - The label that published the light novel release. Keep in mind
  this is not always the same as the publisher. For example, `TOブックス` is a
  label of Kadokawa, and J-Novel Heart is a label of J-Novel Club.

### Other

- The spaces used to separate these components should be regular English
  half-width spaces. However, full-width spaces present in the original title
  should be left as is.

## Examples

- `[白石定規] v23 - 魔女の旅々２３ (ＧＡノベル)`
- `[香月美夜] v01 - 本好きの下剋上～司書になるためには手段を選んでいられません～第一部「兵士の娘I」 (TOブックス)`
- `[大木戸 いずみ] v07 - 歴史に残る悪女になるぞ ７ 悪役令嬢になるほど王子の溺愛は加速するようです！【電子特典付き】 (ビーズログ文庫)`
