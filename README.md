# LPD-107678 · Project tasks with lazy-loaded subtasks

**Live prototype:** https://mariaarcevich.github.io/LPD-107678-Tasks-Subtasks-Data-Set/

Prototype for **LPD-107678 – Support Subtasks to CMP Tasks**, built to agree with the data set (FDS) team on how the project Tasks table should behave once tasks have subtasks.

## What it shows

- **Tree view, no pagination:** top-level tasks load in batches on scroll, with a loading indicator under the last row.
- **Lazy-loaded subtasks:** same pattern as Clay Table "Async Load" ([Storybook](https://storybook.clayui.com/?path=/story/design-system-components-table--async-load)). The chevron turns into a spinner and the row opens when its subtasks arrive; children are cached.
- **Search and filters → flat list** with a Parent column; clearing returns to the tree.
- **Sorting** keeps the hierarchy (subtasks sorted within their parent).
- **Selection:** header checkbox = loaded rows; "Select All" in the active bar selects the whole result set. Selecting a task doesn't select its subtasks.
- **Summary cards:** counts of tasks + subtasks from the server, with a skeleton while loading; each card is also a filter.
- **Prototype controls** (bottom right): Fast/Slow response time and Reset.

## Figma

- [Collapsed](https://www.figma.com/design/9fQQlDIl9xDTOy68rlU0wK/LPD-107678-EPIC-%7C-Support-Subtasks-to-CMP-tasks?node-id=79-20011)
- [Expanded](https://www.figma.com/design/9fQQlDIl9xDTOy68rlU0wK/LPD-107678-EPIC-%7C-Support-Subtasks-to-CMP-tasks?node-id=105-54927)

Built with Lexicon Vanilla (plain HTML + CSS, no build).
