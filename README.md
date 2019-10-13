# Zim templates

Zim-wiki templates for exporting notebooks into another formats, beside websites. The procedure to export a notebook is decribed in the appropriate section of the [Zim manual](https://zim-wiki.org/manual/Help/Export.html).

## How to use these templates
The templates must be placed in a convenient place in the local computer and then Zim must be told do use one of them during an [export operation](https://zim-wiki.org/manual/Help/Export.html).
### Where to save the templates?
Zim will by default search for templates in the following directories:
- `/usr/share/zim/templates/`
- `~/.local/share/zim/templates`

The template can also be specified in the command line.

At least until 0.68, the GUI shows only five formats to choose: HTML, MHTML (Web Page Archive), LaTeX, Markdown (pandoc) and RST (sphinx). Creating an unexpected directory in  `~/.local/share/zim/templates` has no effect in the dropdown list. Therefore, in order to see the templates on the GUI, the unconventional formats must be copied to one of the expected places. I've chosen `markdown` because it was the least polluted in my installation, but you can save it in any of the others (just remark that some of them may not have been created under `~/.local`, so you'll need to create the corresponding dirs).

### How to export my Zim notebook?

#### From the GUI:
1. In the GUI, select <kbd>File</kbd>`>`<kbd>Export</kbd> in the main menu 
1. Choose the contents of the export and click <kbd>Forward</kbd>
1. In the following dialog, choose the format under wich the templates were saved
    1. Choose the template in the <kbd>Model</kbd> list; or
    1. Choos "Another..." and click <kbd>Browse</kbd> to select the template directly
1. Click <kbd>Forward</kbd>
1. In the third dialog, choose whether export each page to a separate file or all into just one
    - Keep in mind that some templates are **intended** to be exported into a single file. E.g. Headings.yaml.

#### From command line

    zim --export --singlefile --recursive [--overwrite] --output=OUT_PATH --format=SEE_ABOVE --template=NAME_OR_PATH_TO_TEMPLATE Notebook
