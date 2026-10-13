# obsidian-mod

Appearance customisations for my Obsidian vault.

## Graph focus

[`snippets/graph-focus.css`](snippets/graph-focus.css) makes the active note vivid
pink and reduces the prominence of ordinary nodes and links. It includes colours
for light and dark themes and applies to the global and local graph views.

The active note is the file Obsidian identifies as currently focused, not simply
the node under the mouse. Keep a note open beside the graph to see the effect.
Graph group colours and special tag/attachment colours remain in use, so those
nodes can still be colourful.

### Install

1. In Obsidian, open **Settings → Appearance → CSS snippets** and click the
   folder icon.
2. Copy `snippets/graph-focus.css` from this repository into that folder
   (normally `<vault>/.obsidian/snippets/`).
3. Click **Reload snippets** and enable **graph-focus**.
4. Open a note beside the graph, then switch notes to check the highlight moves.
   If the graph keeps its previous colours, close and reopen the graph pane.

To undo the change, disable **graph-focus** in CSS snippets.

### Adjust the colours

Edit `--obsidian-mod-graph-focus` in the dark or light theme block to change the
active-note colour. The `node` and `line` values control ordinary nodes and links.
Custom themes or other snippets with stronger CSS overrides may take precedence.

### CSS-only limitation

This snippet changes colour, not size. Obsidian draws graph nodes in a canvas and
calculates their sizes internally from link counts and the graph's Node size
setting. Individual nodes are not HTML elements that CSS can scale or add a glow
to. Enlarging only the active note would require a plugin; that is outside the
scope of this CSS-only change.

### Verification

The selectors and size limitation were checked against the installed Obsidian
app's stylesheet and graph renderer. The snippet has not yet been visually tested
in the target vault. After installation, check both light and dark mode, global
and local graphs, and switching between two open notes.

References: [CSS snippets](https://obsidian.md/help/snippets) and
[Graph view](https://obsidian.md/help/plugins/graph).
