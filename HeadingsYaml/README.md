# Export section headings as Yaml

**WARNING**:This template is intended to export all pages to a single file.

Exports a notebook or a section to a yaml document. Each page takes the
following form:

    "Page full name":
      "headings":
        - List of headings
      "links":
        - List of outgoing links
      "backlinks":
        - List of inbound links
      "attachments":
        - List of attachment names
      "meta":
        - List of meta attributes


## Usage

1. Choose a root for your export (may be all the notebook).
1. Choose "Single page" and check "Include subpages"
1. Choose the file where this template has been saved
    - Select the format and model, if the template was saved in
      a place that Zim recognizes; or
    - Select "Other..." as model and browse for the location
      of the template
1. Remember to change the extension to ".yaml" in the output filename.

## Caveats

### The zim export may end prematurely

The export ends abruptly in some cases:
- when encounters a page without headings or when there is any text before the first heading
- when there are regexp strings in an article body

### Wrong format name

The Zim 0.68 GUI doesn't recognize directory names as format names.
Therefore, this Yaml template must be placed inside one of the
already known formats (html, markdown, latex or rst) or
have its path given in the command line.

### No attachments
Although the attachments names are listed in the yaml file, their contents 
will be copied to a directory structure mirroring the original one in the Zim notebook
and not referenced directly.

If the attachments are relevant to your export, additional steps are 
necessary to take them into account.

