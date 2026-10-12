# Maestro extensions

The canonical examples of custom panels for [Maestro](https://optimisticagency.com/developers), each one self-contained HTML file.

| Panel | What it does | Source |
| --- | --- | --- |
| Table Lens | Sort, filter and page through any CSV in your project. Each pane keeps its own file and view. | [`panels/table-lens.html`](panels/table-lens.html) |
| Chart Lens | Turn a numeric CSV column into bars, largest first. | [`panels/chart-lens.html`](panels/chart-lens.html) |

`panels/sample-inventory.csv` is a small CSV to try them on.

## Use one

In a Maestro project, open **+ Panel → Manage panels…**. Both examples are listed under **Examples**; choose **Install** or **Update** and review their file permission and declared tools. To install a copy you changed, save the file in your project and choose **Install from a project file…**.

## Let an agent use the panel

Ask: “Open sample-inventory.csv in Table Lens, filter to Shelf B and report the matching count using its custom tools.” The agent discovers the tool, reads its input schema, opens or reveals a pane, binds the authorized file and applies the filter. The pane shows two matching rows and the conversation receives the result. No manual file selection is needed.

Table Lens declares `get_rows` and `set_filter`. Chart Lens declares `get_chart` and `set_column`. Their handlers operate on the same file and view as the visible controls. Each pane keeps its own state; agents use a specific pane id when several instances are open.

Enable `search_extension_tools`, `describe_extension_tool`, `open_panel`, `call_extension_tool`, `open_file_for_user` and `list_panels` in the chosen agent's tool settings. Keep the desktop workspace and its conversation open, visible and expanded while tools run. After pressing **Stop** in the browser, send a new message there before submitting another terminal request to that conversation. A function that needs only its input can also run without an open pane, in a temporary instance of the same sandbox with no file and no persistent state.

## Write your own

The [custom panels guide](https://optimisticagency.com/docs/panels) covers the HTML file, manifest, theme, file and state API. The [custom tools guide](https://optimisticagency.com/docs/tools) covers declarations, `oa.tools.handle`, limits, cancellation and instructions for agents. Plain-Markdown versions are available at [panels.md](https://optimisticagency.com/docs/panels.md) and [tools.md](https://optimisticagency.com/docs/tools.md).

The files here are the same bytes Maestro serves at `optimisticagency.com/panels/`.
