---
date: <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
day: <% moment(tp.file.title, "YYYY-MM-DD").format("dddd") %>
weather: [null]
version: 2
type: entry
---

# Journal Entry for <% moment(tp.file.title, "YYYY-MM-DD").format("Do of MMMM YYYY") %>

<< [[Entries/<% moment(tp.file.title, "YYYY-MM-DD").subtract(1, 'd').format("YYYY") %>/<% moment(tp.file.title, "YYYY-MM-DD").subtract(1, 'd').format("MM - MMMM") %>/<% moment(tp.file.title, "YYYY-MM-DD").subtract(1, 'd').format("YYYY-MM-DD") %>E|Previous]] | [[<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>E]] | [[Entries/<% moment(tp.file.title, "YYYY-MM-DD").add(1, 'd').format("YYYY") %>/<% moment(tp.file.title, "YYYY-MM-DD").add(1, 'd').format("MM - MMMM") %>/<% moment(tp.file.title, "YYYY-MM-DD").add(1, 'd').format("YYYY-MM-DD") %>E|Next]] >>

## Notes

```dataviewjs
const date = moment(dv.current().file.name, "YYYY-MM-DD");

// get a list of notes
let notes = dv.pages(`"Entries/${date.format("YYYY")}/${date.format("MM - MMMM")}/${date.format("YYYY-MM-DD")}/Notes"`).sort();

if (notes.length == 0) {
	dv.el("blockquote", dv.el("italic", "There are no notes recorded on this day."));
}

// loop through notes
for (let note of notes) {
    const data = await dv.io.load(note.file.path);
    const regex = /(?<=-----)\s*(.*)/s;  // remove frontmatter
    const content = regex.exec(data);

    if (content) {
        const datetime = new Date(note.file.frontmatter.time);
        const hours = datetime.getHours().toString().padStart(2, "0");
        const minutes = datetime.getMinutes().toString().padStart(2, "0");
        const seconds = datetime.getSeconds().toString().padStart(2, "0");
        const time = `${hours}:${minutes}:${seconds}`;

        dv.el("h3", `[[${note.file.name}|${time}]]`);
        dv.el("blockquote", content[1]);
    }
}
```

## Dreams

```dataviewjs
const date = moment(dv.current().file.name, "YYYY-MM-DD");

// get a list of notes
let notes = dv.pages(`"Entries/${date.format("YYYY")}/${date.format("MM - MMMM")}/${date.format("YYYY-MM-DD")}/Dreams"`).sort();

if (notes.length == 0) {
	dv.el("blockquote", dv.el("italic", "There are no dreams recorded on this day."));
}

// loop through notes
for (let note of notes) {
    const data = await dv.io.load(note.file.path);
    const regex = /(?<=-----)\s*(.*)/s;  // remove frontmatter
    const content = regex.exec(data);

    if (content) {
        const datetime = new Date(note.file.frontmatter.time);
        const hours = datetime.getHours().toString().padStart(2, "0");
        const minutes = datetime.getMinutes().toString().padStart(2, "0");
        const seconds = datetime.getSeconds().toString().padStart(2, "0");
        const time = `${hours}:${minutes}:${seconds}`;

        dv.el("h3", `[[${note.file.name}|${time}]]`);
        dv.el("blockquote", content[1]);
    }
}
```
