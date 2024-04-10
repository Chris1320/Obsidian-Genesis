> [!INFO]+ Welcome to **Genesis**.
>
> - Press `CTRL+ENTER` to go to today's entry.
> - Press `CTRL+N` to create a new item.
> - Press `CTRL+O` to open an existing item.
> - Press `CTRL+R` to open a random item.
> - Press `CTRL+ALT+H` to change your workspace.

> [!WARNING]- Notifications
>
> > [!QUESTION]- **People without set birthdays**:
> >
> > ```dataview
> > LIST
> > FROM "People"
> > WHERE birthdate = "0000-00-00"
> > SORT ASCENDING
> > ```
%% > 
> > [!QUESTION]- **Dangling Links**:
> > 
> > ```dataview
> > TABLE without id out AS "Uncreated files", file.link as "Origin"
> > FLATTEN file.outlinks as out
> > WHERE !(out.file) AND !contains(meta(out).path, "/")
> > SORT out ASC
> > ``` %%

%% TODO: Use Tracker here to provide summary about the project %%

## Entries

```dataview
TABLE day AS Day
FROM "Entries"
WHERE endswith(file.name, "E")
SORT file.name DESCENDING
LIMIT 14
```

> [!INFO]- Notable Events
>
> ```dataview
> LIST
> FROM #notable
> SORT file.name ASCENDING
> ```

## People

```dataview
TABLE relation AS Relation
FROM "People"
WHERE startswith(file.name, "@")
SORT file.name ASCENDING
LIMIT 25
```
