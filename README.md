# Nirca Mini in your browser

Chat with Nirca Mini, a 109M-parameter byte-level language model with ternary weights, 32 experts and
adaptive recurrence, running entirely on your GPU with WebGPU. Nothing you type leaves the page.

Open the page, click **Load model** (a 33 MB download, cached after the first time), and chat.
You need a browser with WebGPU, such as a recent Chrome or Edge.

- `index.html`: the page, one self-contained file.
- `overview.html`: about the model, how it was trained, and its charter.
- `nirca-mini-charter-6.md`: the charter, as a plain file.
- `slides.html`: a five-minute lightning talk (arrow keys or click to advance, F for fullscreen, N for speaker notes).
- `backup.html`: a frozen copy of the page.
- `weights/`: the model the page loads by default (`config.json` and `model.safetensors`). To load
  other weights, open `index.html?weights=URL`, where `URL` is a folder holding those two files.

Decoding is greedy, so the same conversation always gives the same reply. Nirca Mini is a small
research model: expect odd answers.

Code: MIT, see `LICENSE`. The weights are not covered by that license.
