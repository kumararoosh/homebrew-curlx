# homebrew-curlx

Homebrew tap for [curlx](https://github.com/kumararoosh/curlx) — a keyboard-driven terminal UI for exploring and executing APIs.

---

## What is curlx?

curlx is a TUI (terminal user interface) API client that lets you import OpenAPI specs, manage auth contexts, cache request bodies, and fire HTTP requests — all from your terminal without touching a mouse.

Think of it as Postman, but keyboard-driven and living in your terminal.

---

## Install

Add the tap and install in one step:

```bash
brew install kumararoosh/curlx/curlx
```

Or add the tap separately first:

```bash
brew tap kumararoosh/curlx
brew install curlx
```

---

## Usage

Launch curlx:

```bash
curlx
```

### Basic workflow

**1. Load an OpenAPI spec**

Press `l`, then enter a path or URL:
```
./path/to/openapi.yaml
```
or from a git repository:
```
https://github.com/org/repo path/to/spec.yaml
```

Specs are saved and auto-reloaded on next launch. Load as many as you want — each appears as a collapsible group.

**2. Select an endpoint**

Use `↑` / `↓` to navigate, `enter` to expand folders and load an endpoint into the request pane.

**3. Set authentication**

Press `a` to open the auth switcher. Press `A` to add a new context:
- **bearer** — sends `Authorization: Bearer <token>`
- **apikey** — sends a custom header with your token
- **basic** — sends `Authorization: Basic ...` (`user:password` as token)

Select `(no auth)` to clear authentication.

**4. Edit and send**

Press `Tab` to move to the request pane, `enter` to edit the URL, `i` to edit the body, then `ctrl+r` to send.

**5. View the response**

The response pane shows the status, duration, and pretty-printed JSON. Press `m` to disable mouse capture so you can drag-select and copy text from the response.

### Key reference

| Key | Action |
|-----|--------|
| `l` | Load OpenAPI spec |
| `a` | Auth context switcher |
| `b` | Request body cache |
| `s` | Save current body |
| `m` | Toggle mouse (scrolling ↔ text selection) |
| `Tab` | Switch panes |
| `enter` | Expand folder / load endpoint / enter typing mode |
| `i` | Edit body (typing mode) |
| `ctrl+r` | Send request |
| `esc` | Exit typing mode / close overlay |
| `q` | Quit / close overlay |

---

## Upgrade

```bash
brew upgrade curlx
```

## Uninstall

```bash
brew uninstall curlx
brew untap kumararoosh/curlx
```

---

## Links

- **Source**: https://github.com/kumararoosh/curlx
- **Issues**: https://github.com/kumararoosh/curlx/issues
- **Releases**: https://github.com/kumararoosh/curlx/releases
