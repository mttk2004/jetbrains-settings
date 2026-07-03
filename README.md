# JetBrains Settings

This repository contains my personal JetBrains IDE settings export. It is intentionally tuned for a very clean, keyboard-first workflow with minimal on-screen noise, fast file search, and rapid command access.

## Philosophy

*   **Visually Quiet:** Keep the editor as clean as possible (no line numbers, no breadcrumbs, no toolbars, minimal scrollbar warnings) so attention remains strictly on code.
*   **Keyboard First:** Prefer keyboard navigation and shortcuts over mouse interaction for almost every action.
*   **Layered Shortcuts:** Use mnemonic chord shortcuts (`Alt+<Key>`) and a dedicated `F19` modifier key to keep keys easy to hit and collision-free.
*   **Noise Reduction:** Disable spell checking, duplicate code warnings, and redundant context bulb suggestions to eliminate visual clutter.
*   **Zero-Overhead Search:** Exclude dependencies and build folders globally to keep indexing fast and file search (`Double Shift`) accurate.

---

## Core Customizations

### 1. Keymap & Layered Shortcuts
The custom keymap is defined in [keymaps/kiet.xml](file:///home/kiet/projects/settings/keymaps/kiet.xml) and inherits from the `VSCode` base keymap. 

#### Layer prefixes:
*   `Alt+K`: Workspace, layouts, and tool windows.
*   `Alt+G`: Version control and Git actions.
*   `Alt+F`: Code folding.
*   `Alt+S`: Caret clones and selection helpers.
*   `Alt+R`: Refactoring and formatting.
*   `Alt+T`: Running tests and build configurations.
*   `F19` (Caps Lock mapped to `F19` on Arch Linux): Acts as a fast direct trigger layer.

#### Custom Quick Lists (Gated Shortcuts):
To avoid cluttering the keymap, less common commands are grouped into popup menus triggered by a single shortcut:
*   **Focus & View Modes** (`Alt+K` + `Alt+Z` or `F19` + `Z`): Toggle Zen mode, Distraction-Free mode, Presentation mode, status bar, navigation bar, and tool buttons.
*   **Git Extended Operations** (`Alt+G` + `Alt+E`): Perform less frequent VCS actions like Stash, Unstash, Merge, Rebase, Resolve Conflicts, and Cherry-Pick.

---

### 2. Live Templates
Custom templates are split by language/framework group to automate boilerplate code.

#### Go (`templates/Go.xml`)
*   `errn`: Checks if `err != nil` and returns a default value with the error:
    ```go
    if err != nil {
        return nil, err
    }
    ```
*   `json`: Quick JSON struct tag insertion: `` `json:"$NAME$"` ``
*   `tf`: Quick unit test function boilerplate: `func Test$NAME$(t *testing.T) { ... }`

#### Java & Spring Boot (`templates/Java.xml`)
*   `inj`: Constructor injection boilerplate (preferred over `@Autowired` field injection):
    ```java
    private final $CLASS$ $VAR$;

    @Autowired
    public $CURRENT_CLASS$($CLASS$ $VAR$) {
        this.$VAR$ = $VAR$;
    }
    ```
*   `getm`: Generates `@GetMapping` endpoint returning `ResponseEntity.ok(...)`.
*   `postm`: Generates `@PostMapping` endpoint with a `@RequestBody`.

#### JavaScript, TypeScript & React (`templates/JavaScript.xml`, `templates/React.xml`, `templates/user.xml`)
*   `cssm`: Imports a CSS module automatically named after the current file: `import styles from './$FILENAME$.module.css'`.
*   `cl`: Quick `console.log($c$)` insert.
*   `rsf`: React functional component boilerplate.

---

### 3. Noise Reduction (Inspections & Intentions)
To keep the editor visually clean, the following rules are applied:
*   **Spelling Checks Disabled:** `SpellCheckingInspection` is turned off. Green wavy underlines for typos/abbreviations are hidden.
*   **Duplicate Code Alerts Disabled:** `DuplicatedCode` is disabled to prevent warning lines during active code refactoring or prototyping.
*   **Intention Bulbs Ignored:** Disabled standard IDE popup recommendations (`Alt+Enter` suggestions) that trigger clutter, such as:
    *   Converting quotes to template strings.
    *   Merging nested `if` statements.
    *   Converting `if` statements to `switch`.
    *   HTML/CSS tagging suggestions (e.g. wrap with tag, convert to XML tag).

---

### 4. Global Index Exclusions
The file manager ([options/filetypes.xml](file:///home/kiet/projects/settings/options/filetypes.xml)) globally ignores build and package manager directories:
*   **Ignored folders:** `node_modules`, `vendor`, `venv`, `.venv`, `dist`, `build`, `.next`, `.nuxt`, `.yarn`, `target`.
*   **Result:** Faster project indexing times, less CPU consumption, and clean `Search Everywhere` results.

---

### 5. Project Default Templates
The [options/project.default.xml](file:///home/kiet/projects/settings/options/project.default.xml) file stores configurations applied automatically to all new projects:
*   **Annotation Processing Enabled:** Automatically enabled globally to support Lombok annotations (such as `@Data`, `@Getter`, `@Setter` in Spring Boot) out-of-the-box, removing IDE highlight errors.

---

## Directory Structure

```text
├── codestyles/
│   └── Default.xml             # Formatter rules (JS, TS, PHP, CSS, HTML, etc.)
├── keymaps/
│   └── kiet.xml                # Custom shortcut bindings (VSCode parent, F19 / Alt chord layers)
├── inspection/
│   └── Default.xml             # Inspection profiles (Disables Spelling & Duplicated code)
├── templates/
│   ├── Go.xml                  # Go Live Templates (err checks, json tags, tests)
│   ├── Java.xml                # Java/Spring Boot templates (DI, mappings)
│   ├── JavaScript.xml          # JS/TS log and query templates
│   ├── React.xml               # React functional components
│   └── user.xml                # Custom cssm templates
└── options/
    ├── editor.xml              # Minimal UI editor behaviors (No line numbers, block caret, soft wraps)
    ├── filetypes.xml           # Global directory ignore lists
    ├── quicklists.xml          # Custom Quick List definitions (VCS, Focus modes)
    └── project.default.xml     # Annotation processing enabled by default
```

---

## Importing Settings

To apply this setup to your IDE:

1.  Close your JetBrains IDE.
2.  Copy these directories into your IDE's global configuration path.
    *   **Linux:** `~/.config/JetBrains/<Product><Version>/` (e.g., `~/.config/JetBrains/IntelliJIdea2026.1/`)
    *   **macOS:** `~/Library/Application Support/JetBrains/<Product><Version>/`
    *   **Windows:** `%APPDATA%\JetBrains\<Product><Version>\`
3.  Open the IDE. Go to **Settings | Keymap** and select the **kiet** keymap.

---

## Recommended Local Configs (Not versioned in repository)

Since JetBrains saves workspace actions locally inside `.idea/workspace.xml`, configure the following settings in your IDE UI under **File | New Projects Setup | Settings for New Projects**:
1.  **Actions on Save:** Enable **Reformat code** and **Optimize imports** to automatically format files (runs `gofmt` and `goimports` for Go) on save.
2.  **Inlay Hints:** Go to **Editor | Inlay Hints** and uncheck parameter name hints for Go and Java to keep code layouts neat and compact.
