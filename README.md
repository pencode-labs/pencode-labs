<div align="center">

# Pencode Labs

**A Go-native code editor and its extension ecosystem.**

Local · SSH · WebSocket — one workbench, anywhere your project lives.

</div>

---

## 🧭 Projects

### [Pencode](https://github.com/pencode-labs/pencode) — the editor

A code editor written in Go, with an Onix-powered desktop interface and a shared backend for local, SSH, and WebSocket workspaces.

```text
Desktop workbench (Onix)
        │  CS v7: local pipes · SSH stdio · WebSocket
        ▼
Pencode server
        ├── Files, documents, indexing, syntax parsing
        ├── Git and terminal processes
        ├── Language servers (LSP)
        └── Extension processes (peb v13)
```

| Area | Highlights |
| --- | --- |
| Editing | Tabs, undo/redo, find & replace, piece-tree buffer |
| Language tools | Incremental syntax highlighting, full LSP integration |
| Terminal | Multi-session PTY / ConPTY, true color, scrollback |
| Debugger | DAP sessions, breakpoints, stepping, variable inspection |
| Git | Staging, commits, history, diffs, three-way merge |
| Remote | OpenSSH or token-authenticated WebSocket workspaces |
| Extensions | Custom editors, language servers, themes, icons, UI |

**Status: early development** — extracted from [Onix](https://github.com/diiyw/onix). Requires Go 1.27+ and an Onix checkout beside it. See the [development setup](https://github.com/pencode-labs/pencode#development-setup).

### [Extensions registry](https://github.com/pencode-labs/extensions)

The official extension catalog. Install with Pencode's extension manager from a local directory — no online catalog yet. [Add your own extension via PR.](https://github.com/pencode-labs/extensions#adding-an-extension)

## 🧩 Official extensions

| Extension | What it does |
| --- | --- |
| [**Go**](https://github.com/pencode-labs/go) | Go language and debug support; auto-installs `gopls` and Delve |
| [**PHP**](https://github.com/pencode-labs/php) | PHP & Blade language servers, automatic install, Xdebug adapter |
| [**Codex**](https://github.com/pencode-labs/codex) | Codex Agent extension for AI-assisted coding |
| [**Markdown preview**](https://github.com/pencode-labs/markdown-preview) | Read-only preview with native source editing and split layout |
| [**Material icons**](https://github.com/pencode-labs/material-icons) | Material Design file icon theme |
| [**UI demo**](https://github.com/pencode-labs/ui-demo) | Reference examples: actions, dialogs, menus, popups, panels |

Extensions are standalone executables talking to the server over **peb v13**, a binary protocol on stdin/stdout — so they run with full power on any workspace host, remote included.

## 📚 Documentation

| Document | Language |
| --- | --- |
| [CS protocol](https://github.com/pencode-labs/pencode/blob/main/protocol/README.md) | 中文 |
| [Extension protocol & SDK (peb)](https://github.com/pencode-labs/pencode/blob/main/peb/README.md) | 中文 |
| [LSP support](https://github.com/pencode-labs/pencode/blob/main/lsp/README.md) | 中文 |
| [Debugger guide](https://github.com/pencode-labs/pencode/blob/main/debugger/README.md) | English |
| [Historical implementation notes](https://github.com/pencode-labs/pencode/blob/main/docs/implementation-notes.zh-CN.md) | 中文 |

English translations of the technical guides are welcome — see [contributing](https://github.com/pencode-labs/pencode#contributing).

## 🤝 Contribute

- 🐛 [Report bugs](https://github.com/pencode-labs/pencode/issues) — include OS, Go version, Pencode/Onix revisions, and reproduction steps
- 🔌 [Build an extension](https://github.com/pencode-labs/extensions#adding-an-extension) — every extension is its own Go module
- 🌐 Help translate the technical guides to English
- 💡 Discuss substantial protocol or architecture changes in an issue first

---

<div align="center">

**MIT licensed** · Built on [Onix](https://github.com/diiyw/onix), gotreesitter, and Go

</div>
