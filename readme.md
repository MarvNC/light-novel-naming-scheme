# Light Novel Naming Scheme <!-- omit from toc -->

Inspired by the standard
[Daiz/manga-naming-scheme](https://github.com/Daiz/manga-naming-scheme), this
document provides a naming scheme for light novel releases.

- [Goals](#goals)
- [Naming Scheme](#naming-scheme)
  - [Components](#components)
  - [Other](#other)
- [Folder Naming Scheme](#folder-naming-scheme)
  - [Special Cases](#special-cases)

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
- Filenames should be easily machine-generated from information easily fetched.

## Naming Scheme

```
[Author] yymmdd - Title (Publisher - Label) [Extra Information] {Revision}
```

<!-- prettier-ignore -->
> [!NOTE] 
> Optional components:
> - ` - Label`
> - `[Extra Information]`
> - `{Revision}`

- `[白石定規] 241013 - 魔女の旅々２３ (SBクリエイティブ - ＧＡノベル)` -
  [Source](https://bookwalker.jp/de7da18c80-136c-4cfc-9a6a-68566ece1a8f/)
  - Not
    `[白石定規] 241013 - 魔女の旅々２３【ドラマＣＤ音源付き】 (SBクリエイティブ - ＧＡノベル)`
    because the drama CD is not included in the volume.
- `[香月美夜] 150227 - 本好きの下剋上～司書になるためには手段を選んでいられません～第一部「兵士の娘I」 (TOブックス - TOブックスノベル)` -
  [Source](https://bookwalker.jp/dedc74df88-0644-445b-a652-ae1f60d999db/)
- `[大木戸 いずみ] 241015 - 歴史に残る悪女になるぞ ７　悪役令嬢になるほど王子の溺愛は加速するようです！【電子特典付き】 (KADOKAWA - ビーズログ文庫)` -
  [Source](https://bookwalker.jp/de541ef160-e044-44df-a389-64768d8fb1d2/)
  - Note that `【電子特典付き】` is included in the title because it is included
    in the volume.
- `[屋久ユウキ] 200417 - 弱キャラ友崎くん　Ｌｖ．８．５ (小学館 - ガガガ文庫)` -
  [Source](https://bookwalker.jp/dedbb7209b-836f-42c0-95b8-449e81992bae/)
- `[Natsu Hyuuga] 241014 - The Apothecary Diaries: Volume 12 (J-Novel Club)` -
  [Source](https://global.bookwalker.jp/dea3f62d46-0815-450b-b2dc-249da3b961d7/)
- `[Ｉｎｏｒｉ] 200924 - I'm in Love with the Villainess Vol. 1 (Seven Seas Entertainment - Airship) {v2}` -
  [Source](https://global.bookwalker.jp/dec453048a-1a86-41f6-be72-7e938d495fc2/)
  |
  [Source](https://sevenseasentertainment.com/books/im-in-love-with-the-villainess-light-novel-vol-1/)
- `[Satou Kazuma] 251212 - Some Light Novel Volume 5 Chapters 1-4 (Random Fan TL Group)`
  - The `Some Generic Light Novel Volume 5 Chapters 1-4` portion can be named at
    the discretion of the release group, since as long as the date is included,
    the release will sort correctly.

### Components

- `[Author]`
  - The author of the light novel. If the release is in Japanese, the author's
    name should be in Japanese name order and spelled as originally published.
    In English, the author's name should be in English name order.
- `yymmdd`
  - The earliest known release date of the light novel in the format `yymmdd`.
    For example, `241014` would be October 14, 2024. This is done to ensure
    consistent chronological sorting of releases and to bypass any confusion
    about volume numbers, which should be provided in the official title.
- `Title`
  - The title of the light novel. This should be **unmodified and copied as-is
    from an official retail/publisher listing**, without changing the whitespace
    used or the formatting of volume numbers.
    - The only exception is to remove characters not valid in file paths, such
      as `?`, `*`, etc. These should not be replaced with other characters when
      removed.
    - If there are bonuses included with the volume, these should be left in the
      title if they are included in the release.
      - `【電子特典付き】` (with digital tokuten) should be included if the
        tokuten is included in the release. If it is a separate `.pdf` file that
        should be released separately.
      - `【ドラマＣＤ音源付き】` (with Drama CD audio) should not be included as
        a drama CD will not be included in an `.epub`.
- `(Publisher - Label)`
  - The publisher and label that published the light novel release. The label is
    optional.
- `[Extra Information]`
  - Any extra information such as the name of the ripper.
- `{Revision}`
  - The revision number of the release. This is optional and should be
    incremented starting from 2 when a release is updated.

### Other

- The spaces used to separate these components should be regular English
  half-width spaces. However, full-width spaces present in the original title
  should be left as is.

## Folder Naming Scheme

```
[Author] - Title (Publisher - Label)
```

<!-- prettier-ignore -->
> [!NOTE] 
> Optional components:
> - `(Publisher - Label)`

- `[白石定規] - 魔女の旅々 (SBクリエイティブ - ＧＡノベル)`
- `[香月美夜] - 本好きの下剋上～司書になるためには手段を選んでいられません～ (TOブックス - TOブックスノベル)`
- `[Natsu Hyuuga] - The Apothecary Diaries (J-Novel Club)`
- `[Ｉｎｏｒｉ] - I'm in Love with the Villainess (Seven Seas Entertainment - Airship)`

### Special Cases

- **Multiple Titles within a Series**:

  - If a series has subtitles or multiple arcs that affect the folder
    organization (e.g., divided into multiple "books" or "parts"), the overall
    series name can be chosen at your discretion. However, usually retail sites
    like Bookwalker will provide an overall series name.

- **Multiple Publishers/Labels**:
  - If there are multiple publishers or release groups for a series, you may
    remove the publisher/label from the folder name.
