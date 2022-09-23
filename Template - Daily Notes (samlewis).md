---
aliases:
  - Today's Tasks
tags: 
created: 2022-07-26T13:40:38-07:00
updated: 2022-07-29T02:50:24-07:00
title: Today's Tasks
linter-yaml-title-alias: Today's Tasks
date created: Tuesday, July 26th 2022, 1:39:20 pm
date modified: Thursday, July 28th 2022, 6:32:59 pm
---
```dataviewjs
const {DvTasks} = customJS
DvTasks.getOverdueTasks({app, dv, luxon, that:this, date:'2021-08-25'})
```

```dataviewjs
const {DvTasks} = customJS
DvTasks.getTasksNoDueDate({app, dv, luxon, that:this})
```

# Today's Tasks

```dataviewjs
const {DvTasks} = customJS
DvTasks.getTodayTasks({app, dv, luxon, that:this, date:'2021-08-25'}) 
```

# Daily Journal
