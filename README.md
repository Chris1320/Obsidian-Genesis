# Genesis (Obsidian Template)

 An [Obsidian](https://obsidian.md/) journal template that I use for Project Genesis.

![image](https://github.com/Chris1320/Obsidian-Genesis/assets/74256376/99469987-f311-44ea-a36c-9b30724e2b5a)

![image](https://github.com/Chris1320/Obsidian-Genesis/assets/74256376/1257b9d3-ef42-473e-8d13-8bee06c80be1)

![image](https://github.com/Chris1320/Obsidian-Genesis/assets/74256376/d316a38a-425c-4dab-9e4c-5d9c755a33cd)

 ## Template Usage

 1. Go to the [Releases](https://github.com/Chris1320/Obsidian-Genesis/releases) page and download the latest `.zip` file.
 2. Unzip the archive and copy the `Genesis/` directory to wherever you want to store your journal.
 3. Open the directory as a vault in [Obsidian](https://obsidian.md/).

## Hotkeys

| Keybind            | Action                                                                |
| ------------------ | --------------------------------------------------------------------- |
| `CTRL+ENTER`       | Go to today's entry.                                                  |
| `CTRL+N`           | Add a new note, dream, or person.                                     |
| `CTRL+O`           | Open an existing note, dream, or person.                              |
| `CTRL+R`           | Open a random note, dream, or person.                                 |
| `CTRL+ALT+H`       | Change workspace view between Default, Graph View, or Genealogy Tree. |
| `CTRL+ALT+SHIFT+D` | Delete currently open file. (Be careful!)                             |

## Structure

```plaintext
Genesis/
├───Entries/
├───Media/
├───Meta/
│   ├───Mood/
│   │   └───Data/
│   └───Templates/
│       └───Archived/
└───People/
```

### Entries

This directory contains your daily notes, dreams, and entries. It is organized in this template:

```plaintext
Entries/
└───<year>/
    └───<xx> - <month>/
        ├───<YYYY-MM-DD>E.md
        └───<YYYY-MM-DD>/
            └───<YYYY-MM-DD>/
                ├───Notes/
                │   └───<YY-MM-DD_HH-MM-SS>N.md
                └───Dreams/
                    └───<YY-MM-DD_HH-MM-SS>D.md
```

Every date is linked to one **Entry**. Each entry can contain multiple **Notes** (things you want to write in your journal) and/or multiple **Dreams** (dreams you had that day).

### Media

When you attach an image, a video, an audio recording, or a document in your notes, it will be placed in this directory.

### Meta

This directory contains data about your journal, including templates and your mood data.

### People

When you add a person in your journal, their files are added here.

## Plugins

### Core

- Audio Recorder
- Backlinks
- Canvas
- Command Palette
- Daily Notes
- File Recovery
- Files
- Graph View
- Outgoing Links
- Page Preview
- Properties View
- Quick Switcher
- Random Note
- Search
- Tags View
- Word Count
- Workspaces

### Community

- [Advanced Tables](https://github.com/tgrosinger/advanced-tables-obsidian)
- [At People](https://github.com/saibotsivad/obsidian-at-people)
- [Auto Link Title](https://github.com/zolrath/obsidian-auto-link-title)
- [Blur](https://github.com/gapmiss/blur) (modified to not replace content when redacting)
- [Calendar](https://github.com/liamcain/obsidian-calendar-plugin)
- [Dataview](https://github.com/blacksmithgu/obsidian-dataview)
- [Homepage](https://github.com/mirnovov/obsidian-homepage)
- [Journal Review](https://github.com/Kageetai/obsidian-plugin-journal-review)
- [Mood Tracker](https://github.com/dartungar/obsidian-mood-tracker)
- [Natural Language Dates](https://github.com/argenos/nldates-obsidian)
- [Omnisearch](https://github.com/scambier/obsidian-omnisearch)
- [QuickAdd](https://github.com/chhoumann/quickadd)
- [Style Settings](https://github.com/mgmeyers/obsidian-style-settings)
- [Tag Wrangler](https://github.com/pjeby/tag-wrangler)
- [Templater](https://github.com/SilentVoid13/Templater)
- [Text Extractor](https://github.com/scambier/obsidian-text-extractor)
