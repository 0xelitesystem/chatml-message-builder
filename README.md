# ChatML Message Builder

Visually build a chat messages array and export it in OpenAI-style and Anthropic-style JSON. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/chatml-message-builder/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

- Add a message row, pick its role (system, user, or assistant), and type the content.
- Reorder rows with the Up and Down buttons, or remove any row.
- The tool exports two outputs side by side: an OpenAI-style `messages` array and an Anthropic-style object where system turns are lifted into a top-level `system` field.
- Validation flags empty content, missing messages, and system turns that appear after the first position.
- A rough token estimate (about 4 characters per token) and character count update as you type.
- Copy buttons put either output on your clipboard.

## Why this exists

Hand-writing a messages array in JSON is fiddly: you miscount brackets, forget a role, or paste a system message in the wrong spot. This is a visual builder that keeps the JSON valid and shows both common formats at once, in a single file with no dependencies.

## Privacy

Everything runs in your browser. The messages you type and the JSON you export never leave your machine. Verify by viewing the page source or by opening DevTools and watching the network tab, no requests are made.

## Run locally

```bash
git clone https://github.com/0xelitesystem/chatml-message-builder
cd chatml-message-builder
# Open index.html in your browser, or:
python -m http.server 8000
```

## Build

There is no build. It's a single HTML file.

## License

MIT.

## Related

- [prompt-cost-calculator](https://github.com/0xelitesystem/prompt-cost-calculator)
- [prompt-token-meter](https://github.com/0xelitesystem/prompt-token-meter)
- [claude-md-generator](https://github.com/0xelitesystem/claude-md-generator)
