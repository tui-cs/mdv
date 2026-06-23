# mdv - A Terminal.Gui-based Markdown viewer

Opens an interactive TUI markdown viewer with rendered Markdown with auto scrollbars (vertical + horizontal), a **StatusBar** with Quit, Content Width control, line count, file size, status, and spinner, and a **File selector** dropdown when viewing multiple files.

![mdv](mdv.gif)

When run with the `--print` option, it renders the markdown to the terminal and exits, without launching the interactive viewer.

Wildcards are supported: `mdv *.md`, `mdv docs/*.md`.

Built with [Terminal.Gui](https://tui-cs.github.io/Terminal.Gui/).

## Supported Markdown Features

- Headings (`#`, `##`, etc.)
- Paragraphs and line breaks
- Emphasis (`*italic*`, `**bold**`, `~~strikethrough~~`)
- Links (`[text](url)`)
- Images (`![alt](url)`)
- Code blocks (fenced with ```` ``` ````)
- Inline code (`` `code` ``)
- Blockquotes (`> quote`)
- Lists (ordered and unordered)
- Tables
- Horizontal rules (`---`)
- Syntax highlighting for code blocks (using ColorCode with various themes)

## Install

```
dotnet tool install -g Terminal.Gui.mdv
```

## Usage

```
mdv <file.md> [file2.md ...]              # Full-screen interactive mode (default)
mdv --print <file.md> [file2.md ...]      # Print mode: renders to terminal and exits
mdv -t <ThemeName> <file.md> [file2.md ...] # Specify syntax-highlighting theme
mdv --help                               # Show this help message (Renders this README as formatted markdown)
```

### Examples

```bash
# View a single file in full-screen mode (default)
mdv README.md
```

```bash
# Print rendered markdown to terminal and exit
mdv --print README.md
```

```bash
# View multiple files with a file selector dropdown
mdv *.md
```

```bash
# Print with a specific theme
mdv -p -t Monokai README.md
```

## Supported Themes (use -t or --theme)

`AtomOneDark`, `AtomOneLight`, `Dark`, `DarkPlus` (Default), `DimmedMonokai`, `Dracula`, `HighContrastDark`, `HighContrastLight`, `KimbieDark`, `Light`, `LightPlus`, `Monokai`, `OneDark`, `QuietLight`, `Red`, `SolarizedDark`, `SolarizedLight`, `TomorrowNightBlue`, `VisualStudioDark`, `VisualStudioLight`

## Building

```bash
dotnet build
```

## Running

```bash
dotnet run -- README.md
```

