# VS Code Minimalist Customization

A highly minimal, distraction-free VS Code setup focused on centered elements, hidden bars, and subtle animations.

## ✨ Features

### 1. Core Layout
- **Centered Filename:** The active file name and path are perfectly centered horizontally in the window.
- **Hidden UI Elements:** Both the **Title Bar** and **Status Bar** are hidden to maximize screen real estate.
- **Hidden Activity Bar:** The left-side icon bar is hidden (access via keyboard shortcuts).
- **Clean Explorer:** Sidebar titles and folder expansion arrows are hidden (but arrows are still clickable).

### 2. Enhanced Interactivity
- **Hover-to-Show Actions:** Editor buttons (Play, Git, Split) only appear when you hover over the tab bar.
- **Centered Command Palette:** `Ctrl+Shift+P` opens the palette in the dead center of the screen.
- **Dynamic Background Blur:** Minimal `3px` blur and dimming applied to the editor when the Command Palette is open.

### 3. Editor Aesthetics
- **No Scrollbars:** Invisible scrollbars in both the editor and sidebar.
- **Distraction-Free Editor:** No line highlight and no markers (errors/search/etc.) in the overview ruler.
- **Relative Guides Removed:** Vertical indent guides in the tree view are hidden.
- **Typography:** Configured for **Dank Mono** with a clean line height.

---

## 🛠️ Required Extensions

1. **[Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)** (By be5invis) - *Required for all visual hacks.*
2. **[Aura Dracula Spirit](https://marketplace.visualstudio.com/items?itemName=josemurilloc.aura-spirit-dracula)** - The primary color theme.
3. **[Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=pkief.material-icon-theme)** - For consistent file/folder icons.

---

## 🚀 Setup Instructions

### 1. Copy Configuration
- Replace your `settings.json` content with the provided `settings.json`.
- Place `vsc-styles.css` in your home directory or a preferred path.

### 2. Update File Path
In your `settings.json`, ensure the `vscode_custom_css.imports` path points to the correct location of your `vsc-styles.css` file:
```json
"vscode_custom_css.imports": ["file:///path/to/vsc-styles.css"]
```

### 3. Activate Custom CSS
1. Open the Command Palette: `Ctrl + Shift + P`.
2. Run: **`Enable Custom CSS and JS`**.
3. **Restart VS Code.**

### 🐧 Linux Manual Patching (If extension fails)
If the extension fails to apply styles (common after updates), you can manually patch your `workbench.html`:
```bash
sed -i 's/<\/html>/<!-- vscode-custom-css-start --><link rel="stylesheet" href="file:\/\/\/home\/YOUR_USER\/.vscode-custom-styles.css"><!-- vscode-custom-css-end --><\/html>/' /opt/visual-studio-code/resources/app/out/vs/code/electron-browser/workbench/workbench.html
```

---

## ⌨️ Useful Shortcuts
- `Ctrl + B`: Toggle Sidebar (since Activity Bar is hidden).
- `Ctrl + Shift + P`: Command Palette (Centered with Blur).
- `Alt`: Show Menu Bar temporarily.
