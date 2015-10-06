Table Editor
===

This is a web component that provides an editor for tabular data. This is a totally experimental thing that's goal is to enable power users to edit data as quickly as possible. It will be experimenting with a few crazy ideas.

The editor will be a client side widget that will do as much work as possible on the client end, leaving it simple to hook up to various servers (or possibly just local storage).



Ideas
===

Simple Data Publish
---
The simple publisher of data will simply dump the entire dataset to the server. This will be the easiest to configure, but the least flexible or performant.


Key-Based Data Publish
---

With this publisher it'll only send the records that have been edited, making it more efficient especially on large sparsely edited datasets.

History Data Publish
---
With this one, rather than sending the updated records it will send the history of changes (potentially with optimization to avoid redundant changes). This would be useful when only certain fields want to be modified, when auditing is desired or to empower other features (like merge).

Automatic 3-way merge
---
When multiple users are editing the same dataset it is sometimes problematic when saving about who's edits take effect. This tool will provide a way to automatically merge changes.



SQL-like querying
---
Many times the default table isn't useful and a user would like a different set of columns etc. Rather than require the user to rearrange the UI we can allow power users to enter a SQL like query, which can be copied, shared, saved etc.