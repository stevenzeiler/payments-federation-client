# AGENTS.md

## Stack
JavaScript (ES6 source, Babel 5 via gulp-babel), superagent, qs, bluebird. Dormant since 2015.

## Layout
- `src/index.js` - the client (source of truth)
- `build/index.js` - committed compiled output, `main` in package.json; regenerate with `node_modules/.bin/gulp`
- `gulpfile.js` - default task compiles `src/**` to `build/`
- `docs/STATUS.md` - current state

## Commands
- `npm install`
- `node_modules/.bin/gulp` - build
- No working test command yet.

## Rules
- Never commit secrets or credentials.
- Use Conventional Commits (`docs:`, `fix:`, `feat:`).
- Edit `src/`, then rebuild `build/`; do not hand-edit `build/`.
- Keep `docs/STATUS.md` current when behaviour or state changes.
