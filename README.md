# Personal Blog Posts

Source-of-truth repository for blog posts authored by Sam Jafari. One folder per post. Each folder contains the markdown source, a Medium-ready HTML version (with absolute image URLs so Medium's import-from-URL feature can fetch images directly), and an `images/` subfolder.

## Posts

| Post | Folder | Status |
|---|---|---|
| Raising AI: What Human Moral Development Can Teach Us About AI Safety and Alignment | [`raising-ai/`](raising-ai/) | Draft |

## Publishing to Medium

Each post folder includes an `index.html` with absolute image URLs pointing to this repository's `raw.githubusercontent.com` paths. To publish:

1. Open Medium and use **Stories → Import a story**
2. Paste the raw HTML URL: `https://raw.githubusercontent.com/Sam-Jafari/Personal-Blog-Posts/main/<post-folder>/index.html`
3. Medium fetches the HTML, parses it, and imports text + images automatically
4. Review and publish from Medium
