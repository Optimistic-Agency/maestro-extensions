# Maestro extensions

The canonical examples of custom panels for [Maestro](https://optimisticagency.com/developers), each one self-contained HTML file.

| Panel | What it does | Source |
| --- | --- | --- |
| Table Lens | Sort, filter and page through any CSV in your project. Each pane keeps its own file and view. | [`panels/table-lens.html`](panels/table-lens.html) |
| Chart Lens | Turn a numeric CSV column into bars, largest first. | [`panels/chart-lens.html`](panels/chart-lens.html) |

`panels/sample-inventory.csv` is a small CSV to try them on.

## Use one

In a Maestro project, open **+ Panel → Manage panels…**. Both examples are listed under **Examples**; choose **Install**. To install a copy you changed, save the file in your project and choose **Install from a project file…**.

## Write your own

The guide is at [optimisticagency.com/docs/panels](https://optimisticagency.com/docs/panels); agents can read it as plain Markdown at [optimisticagency.com/docs/panels.md](https://optimisticagency.com/docs/panels.md). Custom tools, which let agents call functions you define, are coming next: [optimisticagency.com/docs/tools](https://optimisticagency.com/docs/tools).

The files here are the same bytes Maestro serves at `optimisticagency.com/panels/`.
