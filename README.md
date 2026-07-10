# cvoya-com.github.io

The source of <https://cvoya-com.github.io/> — an index of the code [CVOYA](https://cvoya.com) publishes.

It is a static page: `index.html`, `styles.css`, and `images/`. There is no build step. GitHub Pages
serves `main` at the repository root, so a merge to `main` is a deploy.

## Local development

```bash
npx http-server . -p 8765 -c-1     # then open http://localhost:8765/
```

## Validation

CI runs the same two checks on every push and pull request. Run them locally before pushing:

```bash
npm install
npm run validate                   # html-validate + stylelint
```

Both are bugs-only rulesets — structural HTML errors and real CSS faults, not formatting.

## Conventions

- **Design comes from [cvoya.com](https://cvoya.com).** Same tokens (navy `#0b1e3f` on white, Inter,
  hairline rules), same restraint. The wider design system and the other CVOYA sites live in the
  `cvoya-com/web` repository.
- **Name each licence.** Only CVOYA Graph is open source (Apache 2.0). Spring Voyage is
  *source-available* under BSL 1.1 and converts to Apache 2.0 on 2030-04-10. Do not call the pair
  "open source" collectively.
- **No trademark notices.** No ™, no ®, no trademark sections.
- `.nojekyll` is deliberate — it stops Pages running the files through Jekyll.
