# Post-Rendering

A small client-side demo that implements basic post rendering features similar to a simple social feed. The project demonstrates DOM manipulation, event handling, and working with in-memory JSON-like data to add posts, like posts, and add comments.

## Features

- Render a list of posts (author, image, caption, likes, comments)
- Like a post (single like per session)
- Add comments to a post
- Create a new post with an uploaded image (uses URL.createObjectURL)
- Toggle to show/hide comments for each post

## Files

- `indexSolution.html` — Minimal HTML UI with a posts container and a sidebar to create posts.
- `solution.js` — Main JavaScript that holds `postsData`, renders posts, and handles likes, comments, and post submission.
- `Stylesolution.css` — Styling for the feed and sidebar.
- `README.md` — This file.

## How to run

No build tools required — this is a static demo.

1. Clone or download the repository.
2. Open `indexSolution.html` in your browser (double-click or use `File -> Open` in the browser).

Alternatively, run a simple HTTP server in the project directory (recommended for some browsers when using file uploads):

- Python 3: `python -m http.server 8000` then open `http://localhost:8000/indexSolution.html`

## Notes and suggestions

- The demo stores posts in memory (`postsData`), so data is lost when the page reloads.
- Image uploads use `URL.createObjectURL` so the image preview is available only locally and while the page is open.
- The current like/comment logic lives in `solution.js`. You may want to:
  - Persist data to localStorage or a backend API to keep posts between reloads.
  - Prevent adding empty comments by validating and trimming input before pushing.
  - Improve accessibility (add alt text handling, keyboard support) and fix any edge cases in the like-button logic.

## Contributing

Contributions or improvements are welcome — open an issue or submit a PR with the change.

## License

This repository is provided without an explicit license. Add a LICENSE file if you want to specify one.
