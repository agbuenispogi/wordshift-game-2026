# Wordshift

An original word transformation game: solve three connected clues by changing and rearranging letters.

## Features

- 17 handcrafted three-step puzzle trails
- Daily rotation at midnight UTC; trails repeat every 17 days
- Practice collection, hints, reveals, and answer explanations
- Browser-local progress, streaks, statistics, and spoiler-free result sharing
- Responsive layout; no server, database, account, or API key required

## Deploy on Vercel

1. Import this GitHub repository into a new Vercel project.
2. Keep the repository root as the Root Directory.
3. Select Other for Framework Preset. The included vercel.json sets the output directory to dist and skips installation and build commands.
4. Click Deploy. No environment variables are needed.

Official documentation: https://vercel.com/docs/builds/configure-a-build

## Edit and run locally

The website files are dist/index.html, dist/style.css, and dist/app.js. These are authored source files, not generated build output. Edit the PUZZLES array in dist/app.js to change the trails; each has a starting word and three answer/clue/hint entries. Update the collection-count text when adding trails.

Serve locally with `python3 -m http.server 8000 --directory dist` and open http://localhost:8000.

Progress is stored in localStorage on each browser and origin. Progress from the original hosted site does not transfer automatically to a Vercel domain. Google Fonts is an external stylesheet dependency with system-font fallbacks.

## Contact and support

The footer includes a contact form for puzzle suggestions, promotions, feedback, and general messages, plus an optional support dialog. Set the owner-approved email and HTTPS donation URL in `dist/contact-config.js`.

The contact form validates inputs and opens the visitor's email application with a draft. The visitor must press Send in that application. There is no server-side mail delivery or storage of contact form details. Until an address is configured, submission stays disabled with an explicit notice. Until a donation URL is configured, the support dialog states that donations are not open.
