# G.R.O.S.S. — Get Rid Of Slimy textS

An aspect-based sentiment analyzer that rewrites negative or harsh text into something more constructive — sentence by sentence.

Paste in some copy. Hit the button. Get back a version that says the same thing, but better.

**[Try it live →](https://jorgeantonio512.github.io/G.R.O.S.S.-Get-Rid-Of-Slimy-textS/)**

---

## What it does

G.R.O.S.S. splits your text into individual sentences, identifies what each one is about (the *aspect*) and how it sounds (the *sentiment*), then rewrites the slimy bits into something more positive and tactful — without losing the meaning.

**Example:**

| Before | After |
|--------|-------|
| "Boy, that play really sucked." | "I didn't think much of the play." |
| "But the food was good." | "But the food was outstanding." |
| "I don't know if we should go next time." | "Should we go next time?" |

Same information. Different tone.

---

## How to use it

G.R.O.S.S. is a single HTML file. No build step, no dependencies, no server.

1. Clone or download this repo
2. Open `index.html` in a browser
3. Enter your [Anthropic API key](https://console.anthropic.com/) — it stays in your browser tab and is never stored
4. Paste your text and hit **G.R.O.S.S. now!**

Or just use the [hosted version]([https://yourusername.github.io/gross](https://jorgeantonio512.github.io/G.R.O.S.S.-Get-Rid-Of-Slimy-textS/)) on GitHub Pages.

---

## Deploy your own

Since it's one file, GitHub Pages works perfectly:

1. Fork this repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Done — your version is live at `https://yourusername.github.io/gross`

---

## How it works

Each request sends your text to the [Anthropic API](https://docs.anthropic.com/) with a prompt that instructs Claude to:

1. Split the input into individual sentences
2. Identify the **aspect** (what each sentence is about) and **sentiment** (positive / neutral / negative)
3. Rewrite negative sentences to be more constructive — without being falsely cheerful
4. Return structured JSON that the UI renders sentence by sentence

The whole thing is client-side. Your API key goes directly to Anthropic — nothing passes through a third-party server.

---

## Contributing

Bug reports, improvements, and ideas welcome. Open an issue or submit a PR.

A few things worth improving if you want to dig in:

- Track-changes highlighting (show exactly what words changed)
- Editable output (tweak the AI's suggestions before copying)
- Tone dial (target tone: diplomatic / professional / casual)
- Live mode (analyze as you type)

---

## License

MIT — do whatever you want with it. See [LICENSE](LICENSE).

---

*Built in an afternoon. Named with love.*
