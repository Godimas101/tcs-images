# AGENTS.md — tcs-images

**Article images hard-linked from published WordPress posts. UNDER GODIMAS101, NOT under The-Canadian-Space. Intentional — do not migrate.**

> **First-time context:** start with the top-level [AGENTS.md](../AGENTS.md) in the working directory. This file is repo-specific.

## Why this repo stays under Godimas101

Every image in this repo is referenced by a live WordPress post via a `raw.githubusercontent.com/Godimas101/tcs-images/...` URL. If this repo moves to another org, all those URLs break — GitHub's 301 redirect covers repo pages but **`raw.githubusercontent.com` does not follow transfer redirects**.

Result: the URLs in every published TCS article would 404. Not acceptable.

**Decision locked in during the 2026-07-12 org migration.** Every other TCS repo moved to `The-Canadian-Space`; this one stays.

## Working principles

1. **Never rename, move, or delete an image once it's committed.** Even if a post referencing it is later updated — the old post URL might be indexed, archived, or embedded elsewhere.
2. **Uploads go through the n8n Social Posts / image workflows** typically, not manual commits. If you're pushing manually, make sure the filename is stable + descriptive.
3. **Filenames should include the article context** (slug + date + purpose) so future-you knows what an image is for without reading commit messages.
4. **Do not add binary content here that isn't an article image.** No screenshots for debugging, no downloaded reference material — those go in the scratchpad or a local folder.

## Related docs

- [Docs site](https://the-canadian-space.github.io/tcs-docs/)
- Top-level [AGENTS.md](../AGENTS.md) for env access
