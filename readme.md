# Light Novel Naming Scheme <!-- omit from toc -->

Inspired by the standard
[Daiz/manga-naming-scheme](https://github.com/Daiz/manga-naming-scheme), this
document is a naming scheme for light novels, with a focus on Japanese releases.

- [Goals](#goals)
- [Naming Scheme](#naming-scheme)
  - [Components](#components)
  - [Other](#other)

## Goals

Copied from the manga naming scheme:

> - Filenames should always sort properly in chronological chapter order under
>   any and all circumstances.
> - Filenames should never have to be renamed after release to ensure proper
>   sorting.
> - No guessing should ever be necessary when naming files.
> - All filenames should be machine-parseable in a reasonable manner.

**Additional goals:**

- Filenames should respect the original title of the light novel, even when the
  title/subtitle changes between volumes.

## Naming Scheme

```
[Author] v00x1 - Title (Publisher-Label) [Extra Information] {Revision}
```

<!-- prettier-ignore -->
> [!NOTE] 
> Optional components:
> - `x1`
> - `-Label`
> - `[Extra Information]`
> - `{Revision}`

- `[白石定規] v23 - 魔女の旅々２３ (SBクリエイティブ-ＧＡノベル)` -
  [Source](https://bookwalker.jp/de7da18c80-136c-4cfc-9a6a-68566ece1a8f/)
  - Not `[白石定規] v23 - 魔女の旅々２３【ドラマＣＤ音源付き】 (ＧＡノベル)`
    because the drama CD is not included in the volume.
- `[香月美夜] v01 - 本好きの下剋上～司書になるためには手段を選んでいられません～第一部「兵士の娘I」 (TOブックス-TOブックスノベル)` -
  [Source](https://bookwalker.jp/dedc74df88-0644-445b-a652-ae1f60d999db/)
- `[大木戸 いずみ] v07 - 歴史に残る悪女になるぞ ７　悪役令嬢になるほど王子の溺愛は加速するようです！【電子特典付き】 (KADOKAWA-ビーズログ文庫)` -
  [Source](https://bookwalker.jp/de541ef160-e044-44df-a389-64768d8fb1d2/)
  - Note that `【電子特典付き】` is included in the title because it is included
    in the volume.
- `[屋久ユウキ] v08x1 - 弱キャラ友崎くん　Ｌｖ．８．５ (小学館-ガガガ文庫)` -
  [Source](https://bookwalker.jp/dedbb7209b-836f-42c0-95b8-449e81992bae/)
  - Note that it starts at `x1` and not `x5`.

### Components

- `[Author]` - The author of the light novel. If the release is in Japanese, the
  author's name should be in Japanese name order and spelled as originally
  published.
- `v00` - The volume number, padded with zeroes to two digits. As with the manga
  naming scheme, if the volume number goes above 100 then continue with `w100`,
  `w101`, etc.
  - The numbers should be regular ANSI numbers and not full-width.
  - If there is only one volume, the volume number is **still required** as
    `v01` because with light novels the publishing status is often unknown.
- `x1` - Used when a 0.5 volume or otherwise in-between volume exists. This is
  used to ensure proper sorting and should start at `x1`, `x2`, etc. regardless
  of the number used in the original title.
  - If it somehow rolls over past `x9`, use `y1`, `y2`, etc.
- `Title` - The title of the light novel. This should be **unmodified and copied
  as-is from an official retail/publisher source**, without omitting
  Arabic/Roman numerals included in the original title or changing the
  whitespace used.
  - The only exception is to remove characters not valid in filenames, such as
    `?`, `*`, etc. These should not be replaced with other characters when
    removed.
  - If there are bonuses included with the volume, these should be left in the
    title if they are included in the release.
    - `【電子特典付き】` (with digital tokuten) should be included if the
      tokuten is included in the release. If it is a separate `.pdf` file that
      should be released separately.
    - `【ドラマＣＤ音源付き】` (with Drama CD audio) should not be included a
      drama CD will not be included in an `.epub`.
- `(Publisher-Label)` - The publisher and label that published the light novel
  release. The label is optional.
- `[Extra Information]` - Any extra information such as the name of the ripper.
- `{Revision}` - The revision number of the release. This is optional and should
  be incremented starting from 2 when a release is updated.

### Other

- The spaces used to separate these components should be regular English
  half-width spaces. However, full-width spaces present in the original title
  should be left as is.
