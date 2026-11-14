# Markdown Viewer

<p align="center">
  <strong>A clean, security-first Markdown viewer and editor in a single HTML file.</strong><br>
  Open, read, edit, check and export Markdown entirely on your device: no install, no server, no uploads.
</p>

**One file. Works offline. Nothing leaves your computer.**

**Version 1.14.0** · released 2026-11-14 · 817 KB

---

## 🚀 Get started

1. Download **[`markdown-viewer.html`](markdown-viewer.html)** (version 1.14.0). On GitHub, open the file and choose **Download raw file**.
2. Double-click it to open it in your browser. It works straight from disk; you need no internet connection.
3. Click **Open** to choose a Markdown file or **Folder** to open a whole folder, or drag files onto the window.

That's all. You can also put the file on any web host, USB stick or shared drive. It needs nothing else.

To update, download the new `markdown-viewer.html` and replace your old copy with it.

---

## ✨ Features

### Reads every common Markdown flavour
- **GitHub (GFM):** tables, task lists, footnotes, alerts (`> [!NOTE]`), emoji shortcodes, math and Mermaid diagrams, with GitHub's own heading-anchor rules.
- **README-style HTML:** `<p align="center">`, `<details>`, `<kbd>`, image widths and HTML tables, rebuilt from a strict allowlist.
- **Obsidian:** `[[wikilinks]]`, `![[embeds]]`, `%%comments%%`, `#tags` and every callout type.
- **MkDocs, Docusaurus, VitePress, Pandoc, GitLab and Hugo:** admonitions, `:::` containers, `[[_TOC_]]`, and YAML or TOML front matter.
- **Math:** TeX drawn as native MathML, including numbered equations with `\label`, `\eqref` and `\tag`.
- **Diagrams:** every Mermaid 12 diagram type plus ZenUML (flowchart, swimlanes, sequence, ZenUML, class, state, ER, journey, Gantt, pie, quadrant, requirement, use case, git graph, C4, mind map, timeline, sankey, XY chart, block, packet, kanban, architecture, radar, event modeling, treemap, Venn, Ishikawa, Wardley, Cynefin and TreeView), drawn as SVG by a built-in engine, with colours from `classDef`, `style` and `linkStyle`.
- **Syntax highlighting** for about 30 languages.

### Works on your files
- Open a **whole folder** with a file tree. Links between notes, wikilinks and relative images all work.
- **Save in place** (Chrome and Edge) and reload live when a file changes on disk.
- Opens `.md`, `.markdown`, `.mdown`, `.mkd`, `.Rmd`, `.qmd`, `.txt` and more, in UTF-8, UTF-16 or Windows-1252.

### Writing and editing
- **Split editor** with live preview and scroll sync. Double-click the preview to jump to that line in the source.
- **Syntax highlighting and line numbers**, a **formatting bar**, **`/` commands** for blocks and every diagram type, and **smart typing** that closes brackets, wraps selections and finishes code blocks.
- **Problems panel:** broken heading links, missing references and footnotes, images without alt text, heading jumps, table mistakes, unclosed code blocks and diagrams that cannot be drawn, each one click away from its line.
- **Shortcuts** for formatting, lists, tables, moving lines and moving sections; **find and replace** with regex.
- **Autocomplete** for emoji, note names, headings and paths.
- **Insert menu**, **templates** and **daily notes**.
- **Paste as Markdown** from web pages, Google Docs and Word. **Paste images** into a folder note.
- **Never lose work:** unsaved edits are kept as local drafts and offered back after a crash.
- **Review changes** and **compare** with another file as a line diff.
- **Focus mode** and typewriter scrolling.

### Reading and organising
- **Contents** sidebar that follows your scrolling, with folding, word count and reading time.
- **Backlinks**, a folder-wide **tag** index and a **note graph**.
- **Rename a note** and update every link to it.
- **Search** in the document or across the whole folder; a **command palette** (Ctrl/Cmd+P).
- **Link checker** and **document health** suggestions (headings, alt text, link text).
- **Hover previews**, image and diagram **zoom**, **presentation mode** and **read aloud** (local voices only).
- **Dark mode**, reading preferences, responsive layout and full keyboard access.

### Sharing
- **Export** to a self-contained web page (.html), **Word (.docx)**, **Markdown + images (.zip)** or **PDF**, with print options.
- Copy as rich text, copy tables as CSV/TSV/Markdown, and download diagrams as SVG or PNG.

---

## 🔒 Privacy and security

- **Offline by design.** Your documents are read in the browser and never uploaded. The page's security policy blocks every network request from the app.
- **Inert documents.** Markdown and HTML are rebuilt from an allowlist, and an extra sanitizer runs under the browser's Trusted Types. Links never navigate the page; external links only copy their address.
- **Safety check.** Every document is scanned for risky patterns: deceptive links, hidden or text-direction characters ("Trojan Source"), unsafe link schemes. Each finding comes with an explanation.
- **Online media is opt-in,** for each document and each host. Images from private networks and `localhost` are always refused.
- **Optional JavaScript runs isolated.** Only code blocks marked `js run` can run, after a per-document switch *and* a confirmation. They run in a sandboxed background worker with no network, no navigation and a 4-second watchdog.
- **Safe file handling.** Binary files are refused by their content, not their name, and size limits stop oversized or crafted documents from freezing the tab.

The browser keeps a little data locally: drafts of unsaved edits, your preferences and, only if you turn it on, a list of recent files. All of it can be cleared in settings.

### Runnable JavaScript example

````markdown
```js run
root.textContent = 'Hello from the isolated preview';
```
````

Open settings, turn on **Isolated JS**, then press **Run**. Snippets build their output with familiar DOM calls on `root` (`createElement`, `append`, `innerHTML`, events, `<canvas>`), and `console.log` output is shown below the result.

---

## 🌐 Browser support

Recent versions of **Chrome, Edge, Firefox and Safari**. Opening folders, saving in place and pasting images into folders need the File System Access API, which Chrome and Edge provide. Other browsers download a copy when you save.

This single-file edition doesn't include the installable offline app, which needs a service worker and separate files. Everything else is included.

---

## 📜 License

Copyright © 2026 Shintomon Mathew.

Markdown Viewer is free software under the [GNU General Public License v3.0](LICENSE).

It contains no third-party libraries. Its Markdown lexer, document styles and emoji table are its own, adapted from [Marked](https://github.com/markedjs/marked), [github-markdown-css](https://github.com/sindresorhus/github-markdown-css) and [gemoji](https://github.com/github/gemoji) (all MIT). Their license texts are included in `markdown-viewer.html`.
