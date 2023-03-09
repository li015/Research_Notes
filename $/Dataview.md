```dataview
TABLE file.name AS "File", rating AS "Rating" FROM #book
```
We are on page `= this.file.name`.
```dataviewjs
dv.taskList(dv.pages().file.tasks.where(t => !t.completed));
```
This page was last modified at `$= dv.current().file.mtime`.

```dataview
table time-played, length, rating
from "games"
sort rating desc
```
```dataview
list from #game/moba or #game/crpg
```
```dataviewjs
for (let group of dv.pages("#book").where(p => p["time-read"].year == 2021).groupBy(p => p.genre)) {
	dv.header(3, group.key);
	dv.table(["Name", "Time Read", "Rating"],
		group.rows
			.sort(k => k.rating, 'desc')
			.map(k => [k.file.link, k["time-read"], k.rating]))
}
```

