# Snapmarket docs

Client-facing documentation for Snapmarket partnerships. Deploys to
[docs.snapmarket.co](https://docs.snapmarket.co) via Mintlify on every push to `main`.

## What this is

The client-facing translation of the Snapmarket operations repo. It explains the
Story, System, Send, Scale methodology, what a partnership looks like chapter by
chapter, and what we ask of a partner at each stage.

It deliberately does not contain internal production detail. No pricing, no hour
estimates, no skill files, no rate floors. Clients get the shape of the work and
the rhythm of it, never the machinery.

## Structure

- `docs.json` — site config and navigation
- `index.mdx` — welcome page
- `method/` — the methodology, the thesis, the coordinate system, the Prologue
- `story/`, `system/`, `send/` — the three chapters, each with section subfolders
- `scale/` — the measurement layer
- `epilogue.mdx` — offboarding
- `logo/`, `favicon.svg` — brand assets
- `fonts/` — Novela web fonts, not yet wired up (see below)

## Editing

Edit the `.mdx` files directly. Pushing to `main` deploys. Mintlify opens preview
deployments for pull requests.

Voice and formatting follow `STANDARDS.md` in the Snapmarket ops repo: prose over
bullets for anything that is an argument, sentence case headings, no semicolons,
Oxford comma, em dashes without spaces.

## Switching the heading font to Novela

Headings use Fraunces, a stand-in. The Novela web fonts are in `fonts/` but are not
referenced, pending confirmation that the licence permits self-hosting on a public
site. Once confirmed, replace the `fonts` block in `docs.json` with:

```json
"fonts": {
  "heading": {
    "family": "Novela",
    "source": "https://docs.snapmarket.co/fonts/novela-regular.woff2",
    "format": "woff2"
  },
  "body": { "family": "Besley" }
}
```

## Source of truth

The operations repo is canonical for how the work is actually done. This repo is
canonical for how it is explained to clients. When the method changes, both need
updating.
