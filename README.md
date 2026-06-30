# JetBrains Settings

This repository contains my JetBrains IDE settings export. It is intentionally tuned for a very clean, keyboard-first workflow with minimal on-screen noise and fast command access.

## Philosophy

- Keep the editor visually quiet so attention stays on code.
- Prefer keyboard navigation over mouse interaction.
- Make high-frequency actions available through short, mnemonic shortcuts.
- Optimize for power-user flow rather than beginner discoverability.

## What is customized

- Code style rules for JavaScript, TypeScript, PHP, HTML, CSS, SCSS, Blade, and JSP.
- Editor behavior such as soft wraps, breadcrumbs, line numbers, code vision, inlay hints, and folding.
- Custom keymap built around layered shortcuts.
- UI customization for a minimal toolbar layout.
- Color scheme and theme mapping.
- File templates and live templates.

## Keymap design

The custom keymap is defined in `keymaps/kiet.xml` and is based on the `VSCode` parent keymap.

### Structure

I use a layered shortcut model:

- `Alt+K` for workspace and layout controls.
- `Alt+G` for Git and VCS actions.
- `Alt+F` for folding.
- `Alt+S` for selection helpers.
- `Alt+R` for refactoring.
- `Alt+T` for run and test actions.
- `F19` as a second shortcut layer for fast direct access.

### Why F19

On Arch Linux, Caps Lock is remapped to `F19`. That gives me a dedicated modifier-like key with low collision risk and makes the second key layer easy to hit without competing with standard OS shortcuts.

### What this buys me

- Short, mnemonic chords for common IDE actions.
- Less hand travel than menu navigation.
- A consistent mental model across navigation, refactor, Git, and runtime actions.
- A setup that stays usable even in heavily customized Linux environments.

## Notes

- The settings are intentionally minimal and may hide UI elements that some users keep visible, such as line numbers, breadcrumbs, and code vision.
- This export is meant for my own workflow, so some choices are opinionated and not meant to be universal.

## Files of interest

- `codestyles/Default.xml` for code formatting rules.
- `keymaps/kiet.xml` for the custom shortcut map.
- `options/editor.xml` for editor behavior.
- `options/laf.xml` and `options/colors.scheme.xml` for theme setup.
- `options/customization.xml` for toolbar layout.

## Importing

Copy the exported files into the JetBrains configuration location for your IDE, or use the IDE settings import workflow if you want to apply the full profile.

## Conventions

- The repository is intended to stay close to the JetBrains export format.
- Preference is given to explicit XML rather than generated abstractions.
- Changes should preserve the keyboard-first workflow unless there is a strong reason to adjust it.
