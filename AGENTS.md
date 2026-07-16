# AGENTS.md — tcs-images

**Article images hard-linked from published WordPress posts. Now under `The-Canadian-Space` — moved 2026-07-16 from `Godimas101`.**

> **First-time context:** start with the top-level [AGENTS.md](../AGENTS.md) in the working directory. This file is repo-specific.

## History note — the 2026-07-16 move

Originally kept under `Godimas101/tcs-images` because we thought `raw.githubusercontent.com` did NOT follow transfer redirects — moving would 404 every image referenced by every live WordPress post.

Chris tested this on 2026-07-16 and it turned out **the raw URLs DO redirect**. Old links continue to resolve transparently. So the "URL stability exception" was retired and this repo moved home to where it belongs — inside the TCS org.

**Still true:** hundreds of live WP articles reference images by their exact path. Never rename, move, or delete an image once it's been committed. The redirect handles the OWNER swap; it does NOT handle path or filename changes.

## Working principles

1. **Never rename, move, or delete an image once it's committed.** Even if a post referencing it is later updated — the old post URL might be indexed, archived, or embedded elsewhere.
2. **Uploads go through the n8n Social Posts / image workflows** typically, not manual commits. If you're pushing manually, make sure the filename is stable + descriptive.
3. **Filenames should include the article context** (slug + date + purpose) so future-you knows what an image is for without reading commit messages.
4. **Do not add binary content here that isn't an article image.** No screenshots for debugging, no downloaded reference material — those go in the scratchpad or a local folder.

## How to verify (before flagging In QA or closing)

- **Filename is descriptive.** `spacex-launch-2026-02.png` beats `image123.png`. Rename before commit if needed.
- **File size is reasonable.** If it's over 5 MB, compress before commit — this repo is linked from published WP posts and load time matters.
- **Format matches use.** PNG for graphics with transparency, JPG for photos, SVG for logos, GIF only when static won't do.
- **URL test.** Before closing, copy the raw.githubusercontent.com URL and paste it into a browser. If it doesn't load, the commit hasn't pushed or the path is wrong.
- **Never move or rename existing files.** Published WP posts link to specific paths; renaming breaks live articles.

## Related docs

- [Docs site](https://docs.thecanadian.space/)
- Top-level [AGENTS.md](../AGENTS.md) for env access
