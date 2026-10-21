# Cyberpunk HUD V2 — VS Code

VS Code port of the **Cyberpunk HUD V2** Obsidian theme from *The City of the Dark Future* vault.

Same palette: hot red `#ff1f4b` HUD accents, mint `#a9f2e6` readouts, near-black panels, gray frames.

## Install
**One command**, from any folder.

macOS / Linux:
```sh
curl -L -o /tmp/cyberpunk-hud-v2.vsix https://github.com/Natkiio/cyberpunk-hud-v2/releases/latest/download/cyberpunk-hud-v2-2.0.0.vsix && code --install-extension /tmp/cyberpunk-hud-v2.vsix
```

Windows (PowerShell):
```powershell
Invoke-WebRequest https://github.com/Natkiio/cyberpunk-hud-v2/releases/latest/download/cyberpunk-hud-v2-2.0.0.vsix -OutFile "$env:TEMP\cyberpunk-hud-v2.vsix"; code --install-extension "$env:TEMP\cyberpunk-hud-v2.vsix"
```
If `code` isn't recognised, use the by-hand steps below.

**Or by hand:**
1. Download `cyberpunk-hud-v2-2.0.0.vsix` from the [latest release](https://github.com/Natkiio/cyberpunk-hud-v2/releases/latest).
2. In VS Code: Extensions view → `…` menu → **Install from VSIX…** and pick the file.
   On the command line, give the full path, e.g. `code --install-extension ~/Downloads/cyberpunk-hud-v2-2.0.0.vsix`
   (a bare filename only works from the folder it's in).

Then: Command Palette → **Preferences: Color Theme** → **Cyberpunk HUD V2**.

## Syntax mapping
| Token | Color |
|---|---|
| Keywords, HTML/Svelte tags, Markdown H1 | red `#ff1f4b` |
| Numbers, constants, operators, links | soft red `#ff4d6d` |
| Strings, inline code, Markdown italics | mint `#a9f2e6` |
| Types, classes, attributes | dim mint `#5f9e95` |
| Functions, Markdown bold | white |
| Properties, params, other headings | label gray `#c4cccc` |
| Comments | muted `#7d8787` italic |

## Recommended settings
```jsonc
"workbench.colorTheme": "Cyberpunk HUD V2",
"editor.fontFamily": "'Share Tech Mono', Menlo, monospace",
"editor.cursorStyle": "block",
"editor.cursorBlinking": "phase"
```

## Optional HUD extras (glow, scanlines, Michroma labels)
A color theme can't do glow or scanlines. `hud.css` adds them through the
**Apc Customize UI++** extension:
```jsonc
"apc.imports": ["file:///path/to/hud.css"]  // wherever you saved hud.css from this repo
// Windows example: "file:///C:/Users/you/Documents/hud.css"
```
Install the Michroma font (Google Fonts) for the label typeface.
