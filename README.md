# reviv-sites

The live website files for **whiskwhere.com**, **reviv.online**, and **carrylantern.com**, one folder per domain.

## How publishing works

1. Blip edits files here and pushes to this repo.
2. Each site's folder on the Opalstack server is a checkout of its folder here; a cron job on the server pulls every few minutes.
3. A push is live within minutes of the pull. No manual uploads.

## What is NOT in this repo

Image binaries (PNG/JPG: `logo.png`, the founder photo, the delete-account step screenshots) are not synced — the push tool only carries text files. Those images already live on the server and the pull leaves them untouched. SVG logos ARE text and are included. If a PNG/JPG ever needs to change, it is handled as a one-off.

Also excluded: design variants and previews (e.g. `index-left-variant.html`, preview renders) — only files that belong on the live sites are here.

## First-pull note

The first server checkout also deploys the staged Google fix pack (robots.txt, sitemap.xml, canonical tags, carrylantern OG tags) and the shared favicon/footer pass on whiskwhere.com — those changes were staged in these files before the repo was created.
