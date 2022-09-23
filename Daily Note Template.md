---
aliases:
  - <% tp.file.title %>
creation date: <% tp.file.creation_date() %>
tags: DailyNote <% tp.file.title.split('-')[0] %>
created: 2022-07-25T17:19:24-07:00
updated: 2022-07-29T02:46:57-07:00
title: <% tp.file.title %>
linter-yaml-title-alias: <% tp.file.title %>
date created: Monday, July 25th 2022, 5:15:14 pm
date modified: Thursday, July 28th 2022, 6:33:03 pm
---

modification date: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %> // This doesn't currently work in front matter, hoping that gets fixed.

# <% tp.file.title %>

<< [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>]] | [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>]]>>

## Tasks

### Over Due

```tasks
not done
due before <% tp.date.now("YYYY-MM-DD") %>
```

### Due Today

```tasks
not done
due on <% tp.date.now("YYYY-MM-DD") %>
```

### New Today

- [ ]

## Meeting Log

### 0000:

## Daily Log

### [[Project 1]]

### [[Project 2]]

### [[Project 3]]

## Daily Check List

### Start of Day

- [ ] Check Email
- [ ] Check Teams
- [ ] Check showing online
- [ ] Check Calendar - Time Block

### End of Day

- [ ] Show Offline
- [ ] Clean Unused Headings in Daily Log
- [ ] Check tomorrow's calendar

## Other Tasks

### No Due Date

```tasks
not done
no due date
```

### Done Today

```tasks
done on <% tp.date.now("YYYY-MM-DD") %>
```
