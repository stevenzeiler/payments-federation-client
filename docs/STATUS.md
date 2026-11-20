# Status

Last reviewed: 2026-11-20 (pass 02 of the GitHub audit; docs only, nothing was run).

## What works
- `src/index.js` defines `RippleFederationClient` with `lookup(address, domain)` and two error classes. By reading, it builds `?type=federation&destination=..&domain=..` and maps `success`, `error` and other responses to resolve/reject.
- `build/index.js` is a committed Babel 5 compile of `src/index.js` and is the package `main`.

## Known broken or unverified
- Not run in this pass; no tests exist (`npm test` is the placeholder).
- Dependencies date from 2015 (gulp 3, gulp-babel 5, superagent 1, bluebird 2); gulp 3 is known not to run on modern Node **(inference)**.
- `gulp`, `gulp-babel` are in `dependencies`, not `devDependencies`; `description` is empty.
- A debug `console.log` prints every request URL.
- Network errors are reported as "name not found".

## Next
1. Add a build script and a test against a stub endpoint.
2. Move build tooling to devDependencies; fill in description.
3. Decide on a LICENSE file (ISC is declared in package.json).

## Not yet from the standard
CONTRIBUTING.md, docs/ARCHITECTURE.md, docs/RELEASING.md, docs/decisions/, events/CATALOG.md, CHANGELOG.md, SECURITY.md, LICENSE, .github/.
