<%*
const title = await tp.system.prompt("Title", null, true);
const date = tp.date.now("YYYY/MM/DD");
const template = `---
title: "${title}"
tags: ["draft", "${date}"]
created_at: "${date}"
authors: ["cheedah"]
---`;
const uuid_uppercase = await tp.user.uuid();
const uuid = uuid_uppercase.toLowerCase();
const folder = app.vault.getAbstractFileByPath("Notes");
await tp.file.create_new(template, uuid, true, folder);
%>