<%*
const title = await tp.system.prompt("Title", null, true);
const date = tp.date.now("YYYY/MM/DD");
const template = `---
title: "${title}"
tags: ["draft", "${date}"]
created_at: "${date}"
authors: ["cheedah"]
---;
## TL;DR
- 
## Background & Claims
- 
## Core concept
- 
## Experiments
- 
## Discussion
- 
## References
- `;
const uuid_uppercase = await tp.user.uuid();
const uuid = uuid_uppercase.toLowerCase();
const folder = app.vault.getAbstractFileByPath("Notes");
await tp.file.create_new(template, uuid, true, folder);
%>

東京都立東部地域病院　葛飾区亀有5-14-1 035608
東京慈恵会医科大学葛飾医療センター　葛飾青砥6-41-2 0336032111
平成か正式病院0336922121
