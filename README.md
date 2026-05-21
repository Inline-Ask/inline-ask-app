# Inline Ask

<p>
  <img src="https://img.shields.io/badge/macOS-12.0+-blue?style=flat" alt="macOS 12+">
  <img src="https://img.shields.io/badge/Windows-10%2F11%20x64-blue?style=flat" alt="Windows 10/11 x64">
  <img src="https://img.shields.io/badge/License-Proprietary-red?style=flat" alt="Proprietary License">
</p>

**Inline Ask** is a global-hotkey AI assistant (Spotlight-style popup) for macOS and Windows. Press the hotkey anywhere, type or select text, get a streamed AI response, then press **Cmd+Enter** (macOS) / **Ctrl+Enter** (Windows) to paste the result directly into whatever app you were using — no copy/paste dance.

Works with local models via **Ollama** and cloud providers: **OpenAI**, **Anthropic**, **Google Gemini**, **Mistral**, **Groq**, and more.

---

## Download

**[→ Latest Release](https://github.com/Inline-Ask/inline-ask-app/releases/latest)**

| Platform | File |
|---|---|
| macOS (Apple Silicon + Intel) | `Inline.Ask_x.y.z_universal.dmg` |
| Windows x64 (installer) | `Inline.Ask_x.y.z_x64-setup.exe` |
| Windows x64 (MSI) | `Inline.Ask_x.y.z_x64_en-US.msi` |

---

## macOS Installation

1. Download the `.dmg`, open it, and drag **Inline Ask.app** to `/Applications`.
2. **Gatekeeper quarantine** — because the app is ad-hoc signed (not notarized through Apple), macOS will show *"Inline Ask is damaged or can't be opened."* Remove the quarantine attribute before launching:

   ```bash
   xattr -dr com.apple.quarantine "/Applications/Inline Ask.app"
   ```

   Alternatively: right-click the app → **Open** → **Open** in the dialog.

3. **Accessibility permission** — the hotkey and text-selection capture require Accessibility access. On first launch the app will prompt you; if it doesn't, open:

   > System Settings → Privacy & Security → Accessibility → enable **Inline Ask**

4. Launch the app. It lives in the menu bar (no Dock icon). The default hotkey is **⌥ Space**.

---

## Windows Installation

1. Download `Inline.Ask_x.y.z_x64-setup.exe` and run it.
2. **Windows SmartScreen** may show a warning because the app isn't signed with an EV certificate. Click **More info → Run anyway**.
3. After installation, launch **Inline Ask** from the Start menu. The default hotkey is **Alt+Space**.

---

## First-time Setup

Open Settings with **Cmd+,** (macOS) or **Ctrl+,** (Windows):

- **Ollama (local, free, private):** Install [Ollama](https://ollama.com/download), pull a model (`ollama pull gemma3:4b`), then set the provider to **Ollama** and enter the model name.
- **Cloud providers:** Select your provider (OpenAI, Anthropic, Gemini, Mistral, Groq, etc.) and paste your API key.

---

## How it works

1. Press the hotkey (**⌥ Space** / **Alt+Space**) — the popup appears over your current app.
2. Type a prompt, or first select text in any app and then press the hotkey to send the selection as context.
3. The response streams in real time.
4. Press **Cmd+Enter** (macOS) / **Ctrl+Enter** (Windows) to paste the answer back into the app you were using.

---

## Auto-update

Inline Ask checks this repository for new releases and prompts you to update in-app. No manual downloads needed after the first install.

---

## System Requirements

| | Minimum |
|---|---|
| macOS | 12 Monterey — Apple Silicon or Intel |
| Windows | 10 / 11 (x64) |

---

## Feedback & Issues

Found a bug or want a feature? [Open an issue](https://github.com/Inline-Ask/inline-ask-app/issues/new).
