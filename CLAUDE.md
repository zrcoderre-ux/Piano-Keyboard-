# Working notes for Claude

## Shipping changes

The live app deploys from `main` (Cloudflare Pages). A fix that sits only on a
working branch is not visible to the owner.

Standing instruction from the owner (2026-11-16): once a change is finished
and checked, merge it into `main` and push, without asking first and without
opening a pull request. Develop on the session's working branch as usual, then
fast-forward `main` to it.

When `index.html` or any other cached asset changes, bump the `CACHE` version
in `sw.js` in the same change, or installed copies keep serving the old files.
