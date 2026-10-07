# Nirca Mini in your browser

Chat with Nirca Mini, a 109M-parameter byte-level language model with ternary weights, 32 experts and
adaptive recurrence, running entirely on your GPU with WebGPU. Nothing you type leaves the page.

Open https://tg-techie-agents.github.io/nirca-mini-webgpu/mini/, click **Load model** (a 33 MB
download, cached after the first time), and chat. You need a browser with WebGPU, such as a recent
Chrome or Edge.

## Layout

- `mini/`: Nirca Mini's pages.
  - `index.html`: the chat, one self-contained file.
  - `overview.html`: about the model, how it was trained, and its charter.
  - `slides.html`: a five-minute lightning talk (arrow keys or click to advance, F for fullscreen,
    N for speaker notes).
  - `nirca-mini-charter-6.md`: the charter, as a plain file.
  - `backup.html`: a frozen copy of the chat.
- `weights/`: the model the chat loads by default (`config.json` and `model.safetensors`). Every copy
  of the chat, including one saved and opened from disk, loads from this absolute URL, so it stays
  here. To load other weights, open `mini/?weights=URL`, where `URL` is a folder holding those two
  files.
- At the root, `index.html`, `overview.html`, `slides.html` and `backup.html` redirect to their
  `mini/` pages, keeping the query and the `#` part. The root is free for other things later.

Decoding is greedy, so the same conversation always gives the same reply. Nirca Mini is a small
research model: expect odd answers.

Code: MIT, see `LICENSE`. The weights are not covered by that license.
